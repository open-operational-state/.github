# Open Operational State — Project Rules

This document is the canonical, org-wide set of constraints for all repositories under the `open-operational-state` organization. Individual repositories may include a `PROJECT_RULES.md` overlay with additional repo-specific constraints.

---

## Scope

- **v1 scope is locked to machine-readable operational state of web services only.**
- Do not broaden v1 scope beyond web services.
- Do not merge synthetic transaction coordination into v1.
- Do not start with final JSON field names or detailed wire schemas before architecture, scope, and terminology are stabilized.
- Internal architecture must remain extensible for non-web systems in future versions, but those are not part of v1.

## Architecture

- The six-layer architecture is locked and must not be collapsed or reordered:
  1. Core Model
  2. Profiles
  3. Serializations
  4. Adapters
  5. Discovery
  6. Capabilities / Negotiation

## Protocol

- HTTP is the primary protocol surface.
- DNS is optional — used only for bootstrap discovery and domain verification, not for primary operational-state semantics.

## Licensing

- Specification and governance documents: **CC BY 4.0**
- Code (tooling, conformance test runners): **Apache 2.0**
- Documentation-like fixtures: **CC BY 4.0**
- Code-like fixtures intended for direct use in software: **Apache 2.0**

## Contributions

- All contributions require DCO sign-off.
- Contributor Covenant v2.1 applies as the Code of Conduct.
- No CLA is required at this time.

## Neutrality

- All assets in this organization must maintain a vendor-neutral tone.
- No references to specific commercial products, commercial organizations, or proprietary product logic in any neutral-org content.
- If a tool or repository primarily exists to advance a commercial product, it does not belong in this organization.

## Repository Discipline

- Do not create new repositories without explicit approval.
- The current repository set is: `.github`, `governance`, `status-spec`, `status-conformance`, `status-tooling`.
- Deferred repositories (e.g., `status-site`, `status-schemas`, `synthetic-protocol`) must not be created prematurely.

## Standards References

- `draft-inadarei-api-health-check` and `draft-dallariva-web-service-status-json` are named as influences and compatibility targets, not as normative foundations.
- Do not copy their schemas or anchor the spec to their structure.
- Formal RFC or Internet-Draft work is not part of the immediate phase.
