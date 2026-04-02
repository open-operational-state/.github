# Open Operational State

A vendor-neutral effort to standardize machine-readable operational state for web services.

---

**Open Operational State** defines a standard for how web services communicate their operational condition — health, readiness, liveness, status — in a machine-readable, interoperable way.

The effort is built around a six-layer extensible architecture:

1. **Core Model** — stable, transport-agnostic semantics for operational state
2. **Profiles** — domain-specific specializations of the core model
3. **Serializations** — wire-level representations, decoupled from meaning
4. **Adapters** — bridges for existing and legacy formats
5. **Discovery** — how monitors locate operational-state resources
6. **Capabilities** — what a target supports and how to negotiate interaction

## Repositories

| Repository | Description |
|---|---|
| [governance](https://github.com/open-operational-state/governance) | Charter, governance model, terminology, roadmap |
| [status-spec](https://github.com/open-operational-state/status-spec) | Technical specification |
| [status-conformance](https://github.com/open-operational-state/status-conformance) | Conformance definitions, fixtures, and test taxonomy |
| [status-tooling](https://github.com/open-operational-state/status-tooling) | Vendor-neutral reference tooling |

## Get Involved

- Read the [Contributing Guide](https://github.com/open-operational-state/.github/blob/main/CONTRIBUTING.md)
- Review the [Code of Conduct](https://github.com/open-operational-state/.github/blob/main/CODE_OF_CONDUCT.md)
- See [Support](https://github.com/open-operational-state/.github/blob/main/SUPPORT.md) for help channels

## License

Specification and governance documents are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
