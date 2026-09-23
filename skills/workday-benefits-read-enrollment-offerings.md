---
name: workday-benefits-read-enrollment-offerings
description: >-
  Read a Workday worker's active benefit enrollment event and the healthcare and retirement-savings offerings
  inside it, including per-plan costs, coverage options, dependent elections and beneficiary allocations.
api: Workday Benefit Enrollment Event Offerings API
spec: openapi/workday-benefits-benefit-enrollment-event-offerings-openapi.json
operations:
  - GET /employeeEnrollmentEvent
  - GET /employeeEnrollmentEvent/{ID}
consequence: read
generated: '2026-09-17'
method: generated
source: openapi/workday-benefits-benefit-enrollment-event-offerings-openapi.json + conventions/workday-benefits-conventions.yml
---

# Read benefit enrollment offerings

Workday's contract declares no `operationId` for either operation, so identify them by method and path.

## Before you call

- **Auth is OAuth 2.0 only.** Get a token for the tenant; a token alone is not enough, because Workday also
  enforces security domains on the integration system user. A 403 means the domain was never granted — it is
  a customer configuration fix, not a retry.
- **Base path.** `https://{tenantHostname}/api/benefitEnrollmentEventOfferings/v1/{tenant}` for integrations,
  or `https://{apiGatewayBasePath}/benefitEnrollmentEventOfferings/v1` from Extend/Orchestrate.

## Steps

1. `GET /employeeEnrollmentEvent` — returns `{ total, data[] }`. Optional query parameters the contract
   declares: `enrollmentOfferingTypeWID` (Medical, Dental, Vision, 401(k), Basic Group Life …) and
   `onlyCurrentElections` (true = the offerings active as of the processing date; false = the most recent
   offerings, which may come from a future event that is finalized, not started, or in progress).
2. Page with `limit` and `offset`. Default `limit` is 20 and the ceiling is 100. Read `total` to size the
   walk. Do **not** set a tight HTTP timeout on the first page — Workday builds the result cache during that
   call. The cache holds 2 hours between pages and 30 minutes after the last page.
3. `GET /employeeEnrollmentEvent/{ID}` — `{ID}` accepts a 32-character Workday ID (WID) or a
   `Reference_ID=value` alternate. Use it to pull one event's full offering tree.
4. Walk the tree: `enrollmentOfferingsByType` → `healthcareEnrollmentOfferings` →
   `healthcareElectionsInEnrollmentOffering` (plan, currency, plan frequency, employee and employer cost per
   frequency, `coverageOptions[]`, `dependentElections[]`) and → `retirementSavingsEnrollmentOfferings` →
   `retirementSavingsElectionsForEnrollmentOffering` (contribution percentages and amounts with their minima
   and maxima, plus `beneficiaryAllocation[]` with primary and contingent percentages).

## Handling responses

- Empty fields are **omitted**, not null, and key order is not stable — never parse by position.
- Every object carries `id` (WID), `descriptor` (human label) and sometimes `href`.
- Errors use the Workday envelope `{ error, errors[{ error, code, field, path, severity, internalMessage }] }`
  — branch on `code`, never on the message string, which Workday says is subject to change. See
  `errors/workday-benefits-problem-types.yml`.
- A `429` means the tenant is shedding load. There is no `RateLimit-*` or `Retry-After` header to read, so
  back off exponentially.

## What this API does not do

It is read-only. Electing coverage, changing beneficiaries and adding dependents are on the
Benefits_Administration SOAP service (`wsdl/workday-benefits-benefits-administration-v47.wsdl`), where each
write runs through the tenant's business process with its approvals and audit trail.
