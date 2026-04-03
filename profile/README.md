# Open Operational State

A vendor-neutral standard for machine-readable operational state of web services.

---

## The Problem

Every web service exposes health checks differently. Spring Boot returns `{"status": "UP"}`. Kubernetes probes expect a 200. The IETF health check draft uses `{"status": "pass"}`. Your custom endpoint returns `{"healthy": true}`. Monitoring systems, load balancers, and orchestrators all interpret these differently — or don't interpret them at all.

There is no common model for what "operational state" means across systems.

## The Solution

**Open Operational State** provides a canonical semantic model that any health check, readiness probe, or status endpoint can be interpreted through — without requiring systems to change their existing endpoints.

```bash
npm install @open-operational-state/parser @open-operational-state/emitter
```

```js
import { parse } from '@open-operational-state/parser';

// Automatically detects Spring Boot, IETF draft, plain HTTP, or native format
const snapshot = parse( { contentType, body, url, httpStatus } );

console.log( snapshot.condition );  // 'operational' | 'degraded' | 'down'
console.log( snapshot.profiles );   // ['health']
```

Or validate a live endpoint from the command line:

```bash
npx @open-operational-state/validator probe https://your-api.com/health
```

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
| [status-tooling](https://github.com/open-operational-state/status-tooling) | Reference implementation — npm packages, CLI, and adapters |
| [governance](https://github.com/open-operational-state/governance) | Charter, governance model, terminology, roadmap |

## Get Involved

- Read the [Contributing Guide](https://github.com/open-operational-state/.github/blob/main/CONTRIBUTING.md)
- Review the [Code of Conduct](https://github.com/open-operational-state/.github/blob/main/CODE_OF_CONDUCT.md)
- See [Support](https://github.com/open-operational-state/.github/blob/main/SUPPORT.md) for help channels

## FAQ

### Is this a replacement for health check endpoints?

No. Open Operational State does not replace existing health check or status endpoints. It provides a model that can interpret and normalize responses from existing endpoints through adapters.

### Does this replace the IETF health check draft?

No. The project builds on prior work including the [Health Check Response Format for HTTP APIs](https://datatracker.ietf.org/doc/draft-inadarei-api-health-check/) (`draft-inadarei-api-health-check`) and the [Service Status Resource Format for Web Services](https://datatracker.ietf.org/doc/draft-dallariva-web-service-status-json/) (`draft-dallariva-web-service-status-json`). It is compatible with both and can normalize responses that follow either format. See [Prior Art](https://github.com/open-operational-state/status-spec/blob/main/PRIOR-ART.md) for details.

### Why not just use one JSON format?

Because existing systems already use different formats. This standard provides a unifying semantic layer that allows them to coexist while being interpretable through a common model.

### Is this related to Kubernetes health checks?

The standard can interpret Kubernetes liveness and readiness probe semantics. The condition vocabulary includes explicit mappings for Kubernetes concepts. However, the standard is not Kubernetes-specific — it applies to any web service.

## License

Specification and governance documents are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
