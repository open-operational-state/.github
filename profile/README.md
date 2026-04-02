# Open Operational State

A vendor-neutral standard for machine-readable operational state of web services, enabling consistent interpretation across monitoring systems, platforms, and APIs.

---

**Open Operational State** defines how web services communicate their operational condition — health, readiness, liveness, status — in a machine-readable, interoperable way. Instead of requiring systems to change their existing health endpoints, it provides a canonical semantic model that existing formats can be mapped into.

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

## License

Specification and governance documents are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
