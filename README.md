# Workday Benefits (workday-benefits)
APIs for managing employee benefits, enrollments, and benefits administration in Workday.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/workday-benefits/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Benefits, Employee Benefits, Enrollments, Enterprise, HCM, Health Insurance, Human Resources, Retirement, Workday

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-05-03

## APIs

### Workday Benefits API
Comprehensive RESTful API for managing employee benefits including health insurance, dental, vision, life insurance, retirement plans, dependent management, qualifying life events, time off plans, and benefits administration in Workday.

**Human URL:** [https://www.workday.com/en-us/products/human-capital-management/benefits.html](https://www.workday.com/en-us/products/human-capital-management/benefits.html)


#### Tags:

 - Benefits, Employee Benefits, Enrollments, Health Insurance, Human Resources, Retirement

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Benefits/v40.2/Get_Benefits.html)
- [OpenAPI](https://community.workday.com/sites/default/files/file-hosting/productionapi/Benefits/v40.2/Benefits.json)
- [Authentication](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/bRN0dJVT1fKqLxCRjJCx6w)
- [Postman Collection](https://www.postman.com/workday/workspace/workday-rest-api)
- [Rate Limits](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/VNmXGO5eT8oGWtOQRPd46w)
- [Change Log](https://community.workday.com/api-versions)
- [Status Page](https://status.workday.com)
- [Terms of Service](https://www.workday.com/en-us/legal.html)
- [Support](https://community.workday.com/)
- [OpenAPI](openapi/workday-benefits-openapi.yml)
- [JSONSchema](json-schema/workday-benefits-benefit-plan-schema.json)
- [JSONSchema](json-schema/workday-benefits-benefit-enrollment-schema.json)
- [JSONSchema](json-schema/workday-benefits-dependent-schema.json)
- [JSONSchema](json-schema/workday-benefits-benefit-event-schema.json)
- [JSONSchema](json-schema/workday-benefits-time-off-plan-schema.json)
- [JSONSchema](json-schema/workday-benefits-employee-benefits-schema.json)
- [NaftikoCapability - Benefits Administration](capabilities/benefits-administration.yaml)
- [NaftikoCapability - Benefits (Shared)](capabilities/shared/benefits.yaml)

## Common Properties

- [Getting Started](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/_wTPrHlQFO6kuhPPQvXUdg)
- [Developer Portal](https://developer.workday.com)
- [Authentication Guide](https://doc.workday.com/reader/J1YvI9CYZUWl1U7_PSHyHA/bRN0dJVT1fKqLxCRjJCx6w)
- [SDKs](https://github.com/Workday)
- [Blog](https://blog.workday.com/en-us/technology.html)
- [Privacy Policy](https://www.workday.com/en-us/privacy.html)
- [JSON-LD](json-ld/workday-benefits-context.jsonld)
- [SpectralRules](rules/workday-benefits-spectral-rules.yml)
- [NaftikoCapability - Benefits Administration](capabilities/benefits-administration.yaml)
- [NaftikoCapability - Benefits (Shared)](capabilities/shared/benefits.yaml)
- [Vocabulary](vocabulary/workday-benefits-vocabulary.yml)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Workday Benefits API](openapi/workday-benefits-openapi.yml)

### JSON Schema

- [Benefit Plan](json-schema/workday-benefits-benefit-plan-schema.json)
- [Benefit Enrollment](json-schema/workday-benefits-benefit-enrollment-schema.json)
- [Benefit Enrollment Request](json-schema/workday-benefits-benefit-enrollment-request-schema.json)
- [Dependent](json-schema/workday-benefits-dependent-schema.json)
- [Benefit Event](json-schema/workday-benefits-benefit-event-schema.json)
- [Time Off Plan](json-schema/workday-benefits-time-off-plan-schema.json)
- [Employee Benefits](json-schema/workday-benefits-employee-benefits-schema.json)

### JSON Structure

- [Benefit Plan](json-structure/workday-benefits-benefit-plan-structure.json)
- [Benefit Enrollment](json-structure/workday-benefits-benefit-enrollment-structure.json)
- [Benefit Enrollment Request](json-structure/workday-benefits-benefit-enrollment-request-structure.json)
- [Dependent](json-structure/workday-benefits-dependent-structure.json)
- [Benefit Event](json-structure/workday-benefits-benefit-event-structure.json)
- [Time Off Plan](json-structure/workday-benefits-time-off-plan-structure.json)
- [Employee Benefits](json-structure/workday-benefits-employee-benefits-structure.json)

### JSON-LD

- [Workday Benefits Context](json-ld/workday-benefits-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Benefits](capabilities/shared/benefits.yaml) — 9 operations for benefit plan, enrollment, dependent, and employee benefits management

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Benefits Administration](capabilities/benefits-administration.yaml) | Workday Benefits API | 10 | Benefits Administrator, HR Business Partner, Employee Self-Service |

## Vocabulary

- [Workday Benefits Vocabulary](vocabulary/workday-benefits-vocabulary.yml) — Unified taxonomy mapping 6 resources, 3 actions, 1 workflow, and 4 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Workday Benefits Spectral Rules](rules/workday-benefits-spectral-rules.yml) — 40 rules across 14 categories enforcing Workday Benefits API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
