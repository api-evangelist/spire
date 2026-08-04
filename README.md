# SPIRE (spire)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SPIRE (SPIFFE Runtime Environment) is the reference implementation of the SPIFFE standard, providing a toolchain for establishing trust between software systems across a wide variety of hosting platforms through automated attestation and workload identity distribution. SPIRE manages a certificate authority, performs node and workload attestation, and issues SVIDs to workloads through the SPIFFE Workload API.

**APIs.json:** [https://spiffe.io/docs/latest/spire-about/](https://spiffe.io/docs/latest/spire-about/)

## Scope

- **Type:** Index

## Tags

- Authentication
- Cloud Native
- Graduated
- Identity
- Security
- Zero Trust

## Timestamps

- **Created:** 2025
- **Modified:** 2026-05-19

## APIs

### SPIRE Workload API

The SPIRE Agent exposes the SPIFFE Workload API as a Unix domain socket, allowing workloads running on the same node to request their X.509-SVIDs and JWT-SVIDs without requiring any credentials. The Workload API also delivers trust bundle updates so that workloads can verify the identity of other workloads.

- **Human URL:** [https://spiffe.io/docs/latest/spire-about/spire-concepts/](https://spiffe.io/docs/latest/spire-about/spire-concepts/)

#### Tags

- gRPC
- Identity
- JWT
- Workload
- X.509

#### Properties

- [Documentation](https://spiffe.io/docs/latest/spire-about/spire-concepts/)
- [Reference](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE_Workload_API.md)
- [AsyncAPI](asyncapi/spire-workload-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [GitHub Repository](https://github.com/spiffe/spire)
- [Postman Collection](collections/spire-health.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-health.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/spire-oidc-discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-oidc-discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPIRE Server API

The SPIRE Server exposes a gRPC API used by administrators and the SPIRE Agent to manage registration entries, node attestation, bundle federation, and server health. It allows creating and managing workload registration entries that define the SPIFFE IDs issued to workloads matching specified selectors, and supports federation with external SPIFFE trust domains.

- **Human URL:** [https://spiffe.io/docs/latest/deploying/spire_server/](https://spiffe.io/docs/latest/deploying/spire_server/)

#### Tags

- Administration
- Attestation
- gRPC
- Registration
- Server

#### Properties

- [Documentation](https://spiffe.io/docs/latest/deploying/spire_server/)
- [Reference](https://github.com/spiffe/spire-api-sdk)
- [JSON Schema](json-schema/spire-registration-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [GitHub Repository](https://github.com/spiffe/spire-api-sdk)
- [Postman Collection](collections/spire-health.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-health.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/spire-oidc-discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-oidc-discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPIRE Agent API

The SPIRE Agent runs on each node and handles workload attestation, caching SVIDs, and serving the Workload API. It exposes a health check endpoint and communicates with the SPIRE Server via node attestation to establish its own identity before issuing identities to workloads.

- **Human URL:** [https://spiffe.io/docs/latest/deploying/spire_agent/](https://spiffe.io/docs/latest/deploying/spire_agent/)

#### Tags

- Agent
- Attestation
- Identity
- Node
- Security

#### Properties

- [Documentation](https://spiffe.io/docs/latest/deploying/spire_agent/)
- [Reference](https://spiffe.io/docs/latest/deploying/spire_agent/)
- [GitHub Repository](https://github.com/spiffe/spire)
- [OpenAPI](openapi/spire-health-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spire-health.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-health.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Structure](json-structure/spire-registration-structure.json)

### SPIRE OIDC Discovery API

SPIRE includes an OIDC Discovery Provider that serves an OpenID Connect discovery document and JSON Web Key Set (JWKS) endpoint, enabling workloads to present JWT-SVIDs to systems that support standard OIDC token validation. This allows SPIRE-issued identities to be used with cloud provider IAM systems such as AWS, GCP, and Azure.

- **Human URL:** [https://spiffe.io/docs/latest/keyless/oidc-federation-aws/](https://spiffe.io/docs/latest/keyless/oidc-federation-aws/)

#### Tags

- Cloud
- Federation
- Identity
- JWT
- OIDC

#### Properties

- [Documentation](https://spiffe.io/docs/latest/keyless/oidc-federation-aws/)
- [GitHub Repository](https://github.com/spiffe/spire/tree/main/support/oidc-discovery-provider)
- [OpenAPI](openapi/spire-oidc-discovery-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spire-oidc-discovery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spire-oidc-discovery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Structure](json-structure/spire-svid-structure.json)

## Common Properties

- [Website](https://spiffe.io/)
- [Documentation](https://spiffe.io/docs/latest/)
- [Getting Started](https://spiffe.io/docs/latest/try/getting-started-k8s/)
- [GitHub Organization](https://github.com/spiffe)
- [GitHub Repository](https://github.com/spiffe/spire)
- [Community](https://spiffe.io/community/)
- [Slack](https://slack.spiffe.io)
- [Blog](https://spiffe.io/blog/)
- [Changelog](https://github.com/spiffe/spire/blob/main/CHANGELOG.md)
- [Security](https://github.com/spiffe/spire/blob/main/SECURITY.md)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/spiffe)
- [JSON Schema](json-schema/spire-svid-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/spire-registration-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/spire-svid-structure.json)
- [JSON Structure](json-structure/spire-registration-structure.json)
- [JSON-LD](json-ld/spire-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/spire-rules.yml)
- [Capabilities](capabilities/workload-identity.yaml)
- [Vocabulary](vocabulary/spire-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
