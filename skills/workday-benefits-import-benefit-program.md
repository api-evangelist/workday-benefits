---
name: workday-benefits-import-benefit-program
description: >-
  Import a benefit program card (announcement, wellbeing event, partner message) into a Workday tenant as a
  third-party benefit provider, validating the payload before it becomes visible to workers.
api: Workday Benefit Partner API
spec: openapi/workday-benefits-benefit-partner-openapi.json
operations:
  - POST /programs
consequence: write
generated: '2026-09-17'
method: generated
source: openapi/workday-benefits-benefit-partner-openapi.json + conventions/workday-benefits-conventions.yml
---

# Import a benefit program

One operation, `POST /programs`, and it is a **write with no undo on this API**. What it creates is a card
on the worker's home screen, so treat it as publishing, not staging.

## Before you call

- OAuth 2.0 against the tenant, plus access to the web service granted by the Workday customer. Error code
  `A1624` ("You don't have access to the web service. Request access from your Workday customer.") is the
  signal that this grant is missing.
- Base path `https://{tenantHostname}/api/benefitPartner/v1/{tenant}`.

## Steps

1. Build the `benefitProgramsView` body: `title` (40 characters or less), `description` (375 or less),
   `startDate` and `endDate` (end must be after start), optional `adminNotes` for Workday administrators,
   optional `image` (`benefitProgramImageData` + `contentType`; JPG, JPEG, PNG, BMP or TIFF, 5 MB maximum),
   and exactly one of `wellbeingInterest` or a wellbeing category — never both (`A1848`).
2. **Dry run first.** Re-send the same request with the header `x-validate-only: 1`. Workday runs operation
   security, field-level security, instance-set, prompt-resource, currency and header validations and returns
   `200` if the request would be accepted, or a `4xx` with the full error list if it would not — and persists
   nothing.
3. Send the real request without the header (or with `x-validate-only: 0`). A `201` returns the created
   `benefitProgramsView`.
4. Set `wd-external-request-id` (and `wd-external-application-id` / `wd-external-originator-id`) on every
   call. Workday does not log responses or unsuccessful requests, so these headers are your only correlation
   handle when something has to be traced later.

## Retry rules — read this before you retry anything

There is **no idempotency key anywhere in the Workday REST surface**. A retried `POST /programs` creates a
second program card. If a call times out, do not blind-retry: confirm state on the tenant side first. The
only safe pattern available is validate-then-send, with the external request id recorded for reconciliation.

## Known validation codes

`A1586` end date before start date · `A1587` required fields missing · `A1588` URL must start with http:// or
https:// · `A1624` no access to the web service · `A1625` unsupported image type · `A1626` image over 5 MB ·
`A1627` description over 120 characters · `A1655` missing alt text / title over 60 characters · `A1656` URL
alias over 24 characters · `A1848` wellbeing interest and category both supplied. Severity is `Critical` or
`Warning`; validation stops at the first critical failure, so fix and re-validate iteratively.
