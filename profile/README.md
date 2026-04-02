# Open Operational State

A vendor-neutral standard for machine-readable operational state of web services, enabling consistent interpretation across monitoring systems, platforms, and APIs.

---

**Open Operational State** defines how web services communicate their operational condition — health, readiness, liveness, status — in a machine-readable, interoperable way. It enables monitoring systems to interpret health check endpoints, readiness and liveness probes, and service status APIs through a common model — even when they use different formats.

Instead of requiring systems to change their existing endpoints, it provides a canonical semantic model that existing formats can be mapped into through adapters.

> The specification is a **complete, testable draft** with normative requirements, locked vocabulary values, JSON serializations, and conformance levels defined. Feedback is encouraged, especially on vocabulary, semantics, and real-world mapping.

The standard is built around a six-layer extensible architecture:

1. **Core Model** — stable, transport-agnostic semantics for operational state
2. **Profiles** — domain-specific specializations (Liveness, Readiness, Health, Status)
3. **Serializations** — wire-level JSON representations, decoupled from meaning
4. **Adapters** — bridges for existing formats (plain HTTP, draft-inadarei, Spring Boot)
5. **Discovery** — how monitors locate operational-state resources
6. **Capabilities** — what a target supports and how to negotiate interaction

## Start Here

New to the project? Read in this order:

1. **[Architecture](https://github.com/open-operational-state/status-spec/blob/main/ARCHITECTURE.md)** — the six-layer model explained
2. **[Core Model](https://github.com/open-operational-state/status-spec/blob/main/spec/core-model.md)** — the semantic foundation everything builds on
3. **[Condition Vocabularies](https://github.com/open-operational-state/status-spec/blob/main/spec/condition-vocabularies.md)** — the locked vocabulary values and ecosystem mapping

## Repositories

| Repository | Description |
|---|---|
| [status-spec](https://github.com/open-operational-state/status-spec) | Technical specification — the standard itself |
| [status-conformance](https://github.com/open-operational-state/status-conformance) | Conformance definitions, fixtures, and test taxonomy |
| [status-tooling](https://github.com/open-operational-state/status-tooling) | Vendor-neutral reference tooling (coming soon) |
| [governance](https://github.com/open-operational-state/governance) | Charter, governance model, terminology, roadmap |

## Get Involved

- Read the [Contributing Guide](https://github.com/open-operational-state/.github/blob/main/CONTRIBUTING.md)
- Review the [Code of Conduct](https://github.com/open-operational-state/.github/blob/main/CODE_OF_CONDUCT.md)
- See [Support](https://github.com/open-operational-state/.github/blob/main/SUPPORT.md) for help channels

## FAQ

### Is this a replacement for health check endpoints?

No. Open Operational State does not replace existing health check or status endpoints. It provides a model that can interpret and normalize responses from existing endpoints through adapters.

### Does this replace the IETF health check draft?

No. The project builds on prior work including the Health Check Response Format for HTTP APIs (`draft-inadarei-api-health-check`) and the Service Status Resource Format for Web Services (`draft-dallariva-web-service-status-json`). It is compatible with both and can normalize responses that follow either format. See [Prior Art](https://github.com/open-operational-state/status-spec/blob/main/PRIOR-ART.md) for details.

### Why not just use one JSON format?

Because existing systems already use different formats. This standard provides a unifying semantic layer that allows them to coexist while being interpretable through a common model.

### Is this related to Kubernetes health checks?

The standard can interpret Kubernetes liveness and readiness probe semantics. The condition vocabulary includes explicit mappings for Kubernetes concepts. However, the standard is not Kubernetes-specific — it applies to any web service.

## License

Specification and governance documents are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
