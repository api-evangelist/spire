# SPIRE (spire)
SPIRE (SPIFFE Runtime Environment) is the reference implementation of the SPIFFE standard, providing a toolchain for establishing trust between software systems across a wide variety of hosting platforms through automated attestation and workload identity distribution. SPIRE manages a certificate authority, performs node and workload attestation, and issues SVIDs to workloads through the SPIFFE Workload API.

**URL:** [Visit APIs.json URL](https://spiffe.io/docs/latest/spire-about/)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Authentication, Cloud Native, Graduated, Identity, Security, Zero Trust

## Timestamps

- **Created:** 2025
- **Modified:** 2026-05-02

## APIs

### SPIRE Workload API
The SPIRE Agent exposes the SPIFFE Workload API as a Unix domain socket, allowing workloads running on the same node to request their X.509-SVIDs and JWT-SVIDs without requiring any credentials. The Workload API also delivers trust bundle updates so that workloads can verify the identity of other workloads.

**Human URL:** [https://spiffe.io/docs/latest/spire-about/spire-concepts/](https://spiffe.io/docs/latest/spire-about/spire-concepts/)

#### Tags:

 - gRPC, Identity, JWT, Workload, X.509

#### Properties

- [Documentation](https://spiffe.io/docs/latest/spire-about/spire-concepts/)
- [Reference](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE_Workload_API.md)
- [AsyncAPI](asyncapi/spire-workload-asyncapi.yml)
- [GitHubRepository](https://github.com/spiffe/spire)

### SPIRE Server API
The SPIRE Server exposes a gRPC API used by administrators and the SPIRE Agent to manage registration entries, node attestation, bundle federation, and server health. It allows creating and managing workload registration entries that define the SPIFFE IDs issued to workloads matching specified selectors, and supports federation with external SPIFFE trust domains.

**Human URL:** [https://spiffe.io/docs/latest/deploying/spire_server/](https://spiffe.io/docs/latest/deploying/spire_server/)

#### Tags:

 - Administration, Attestation, gRPC, Registration, Server

#### Properties

- [Documentation](https://spiffe.io/docs/latest/deploying/spire_server/)
- [Reference](https://github.com/spiffe/spire-api-sdk)
- [JSONSchema](json-schema/spire-registration-schema.json)
- [JSONStructure](json-structure/spire-registration-structure.json)
- [GitHubRepository](https://github.com/spiffe/spire-api-sdk)

### SPIRE Agent API
The SPIRE Agent runs on each node and handles workload attestation, caching SVIDs, and serving the Workload API. It exposes a health check endpoint and communicates with the SPIRE Server via node attestation to establish its own identity before issuing identities to workloads.

**Human URL:** [https://spiffe.io/docs/latest/deploying/spire_agent/](https://spiffe.io/docs/latest/deploying/spire_agent/)

#### Tags:

 - Agent, Attestation, Identity, Node, Security

#### Properties

- [Documentation](https://spiffe.io/docs/latest/deploying/spire_agent/)
- [Reference](https://spiffe.io/docs/latest/deploying/spire_agent/)
- [GitHubRepository](https://github.com/spiffe/spire)
- [OpenAPI](openapi/spire-health-openapi.yml)
- [JSONStructure](json-structure/spire-registration-structure.json)

### SPIRE OIDC Discovery API
SPIRE includes an OIDC Discovery Provider that serves an OpenID Connect discovery document and JSON Web Key Set (JWKS) endpoint, enabling workloads to present JWT-SVIDs to systems that support standard OIDC token validation. This allows SPIRE-issued identities to be used with cloud provider IAM systems such as AWS, GCP, and Azure.

**Human URL:** [https://spiffe.io/docs/latest/keyless/oidc-federation-aws/](https://spiffe.io/docs/latest/keyless/oidc-federation-aws/)

#### Tags:

 - Cloud, Federation, Identity, JWT, OIDC

#### Properties

- [Documentation](https://spiffe.io/docs/latest/keyless/oidc-federation-aws/)
- [GitHubRepository](https://github.com/spiffe/spire/tree/main/support/oidc-discovery-provider)
- [OpenAPI](openapi/spire-oidc-discovery-openapi.yml)
- [JSONStructure](json-structure/spire-svid-structure.json)

## Common Properties

- [Website](https://spiffe.io/)
- [Documentation](https://spiffe.io/docs/latest/)
- [Getting Started](https://spiffe.io/docs/latest/try/getting-started-k8s/)
- [GitHub Organization](https://github.com/spiffe)
- [GitHubRepository](https://github.com/spiffe/spire)
- [Community](https://spiffe.io/community/)
- [Slack](https://slack.spiffe.io)
- [Blog](https://spiffe.io/blog/)
- [Change Log](https://github.com/spiffe/spire/blob/main/CHANGELOG.md)
- [Security](https://github.com/spiffe/spire/blob/main/SECURITY.md)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/spiffe)
- [JSONSchema](json-schema/spire-svid-schema.json)
- [JSONSchema](json-schema/spire-registration-schema.json)
- [JSONStructure](json-structure/spire-svid-structure.json)
- [JSONStructure](json-structure/spire-registration-structure.json)
- [JSON-LD](json-ld/spire-context.jsonld)
- [SpectralRules](rules/spire-rules.yml)
- [Vocabulary](vocabulary/spire-vocabulary.yml)

## Capabilities

### Shared Definitions

- [SPIRE Health Check API](capabilities/shared/spire-health.yaml)
- [SPIRE OIDC Discovery Provider API](capabilities/shared/spire-oidc-discovery.yaml)

### Workflow Capabilities

- [Workload Identity](capabilities/workload-identity.yaml) — Health monitoring and OIDC identity verification for SPIRE operators.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
