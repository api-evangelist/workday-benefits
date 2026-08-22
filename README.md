# Workday Benefits (workday-benefits)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

APIs for managing employee benefits, enrollments, and benefits administration in Workday.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/workday-benefits/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/workday-benefits/refs/heads/main/apis.yml)

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-05-19

## APIs

### Workday Benefits API

Comprehensive API for managing employee benefits including health insurance, retirement plans, time off, and other benefit programs.

- **Human URL:** [https://www.workday.com/en-us/products/human-capital-management/benefits.html](https://www.workday.com/en-us/products/human-capital-management/benefits.html)
- **Base URL:** `https://wd2-impl-services1.workday.com/ccx/service`

#### Tags

- Benefits
- Employee Benefits
- Enrollments
- Health Insurance
- Human Resources
- Retirement

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Benefits/v40.2/Get_Benefits.html)
- [OpenAPI](https://community.workday.com/sites/default/files/file-hosting/productionapi/Benefits/v40.2/Benefits.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Authentication](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/bRN0dJVT1fKqLxCRjJCx6w)
- [Postman  Collection](https://www.postman.com/workday/workspace/workday-rest-api)
- [Rate Limits](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/VNmXGO5eT8oGWtOQRPd46w)
- [Changelog](https://community.workday.com/api-versions)
- [Status Page](https://status.workday.com)
- [Terms of Service](https://www.workday.com/en-us/legal.html)
- [Support](https://community.workday.com/)
- [OpenAPI](openapi/workday-benefits-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/workday-benefits.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/workday-benefits.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/workday-benefits-benefit-plan-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-benefit-enrollment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-benefit-enrollment-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-dependent-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-benefit-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-time-off-plan-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workday-benefits-employee-benefits-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/workday-benefits-benefit-plan-structure.json)
- [JSON Structure](json-structure/workday-benefits-benefit-enrollment-structure.json)
- [JSON Structure](json-structure/workday-benefits-benefit-enrollment-request-structure.json)
- [JSON Structure](json-structure/workday-benefits-dependent-structure.json)
- [JSON Structure](json-structure/workday-benefits-benefit-event-structure.json)
- [JSON Structure](json-structure/workday-benefits-time-off-plan-structure.json)
- [JSON Structure](json-structure/workday-benefits-employee-benefits-structure.json)
- [JSON-LD](json-ld/workday-benefits-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/workday-benefits-spectral-rules.yml)
- [Naftiko Capability -  Benefits  Administration](capabilities/benefits-administration.yaml)
- [Naftiko Capability -  Benefits ( Shared)](capabilities/shared/benefits.yaml)
- [Vocabulary](vocabulary/workday-benefits-vocabulary.yml)

## Common Properties

- [Getting Started](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/_wTPrHlQFO6kuhPPQvXUdg)
- [Developer  Portal](https://developer.workday.com)
- [Authentication  Guide](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/bRN0dJVT1fKqLxCRjJCx6w)
- [S D Ks](https://github.com/Workday)
- [Blog](https://blog.workday.com/en-us/technology.html)
- [Privacy Policy](https://www.workday.com/en-us/privacy.html)
- [JSON-LD](json-ld/workday-benefits-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/workday-benefits-spectral-rules.yml)
- [Naftiko Capability -  Benefits  Administration](capabilities/benefits-administration.yaml)
- [Naftiko Capability -  Benefits ( Shared)](capabilities/shared/benefits.yaml)
- [Vocabulary](vocabulary/workday-benefits-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
