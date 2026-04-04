# Contributing to Open Operational State

Thank you for your interest in contributing to Open Operational State. This document explains how to participate effectively.

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

## Project Rules

Before making changes, please review the [PROJECT_RULES.md](PROJECT_RULES.md) for org-wide constraints. Individual repositories may have additional rules in their own `PROJECT_RULES.md`.

## How to Contribute

### Reporting Issues

- Use the appropriate issue template (bug report or feature request).
- Search existing issues before creating a new one.
- Provide as much context as possible.

### Proposing Changes

1. **Open an issue first** to discuss the change before writing code or prose.
2. **Fork the repository** and create a branch from `main`.
3. **Make your changes** following the project's conventions and constraints.
4. **Submit a pull request** referencing the issue it addresses.

### What We Accept

- Bug fixes and corrections
- Documentation improvements
- Test fixtures and conformance contributions
- Tooling enhancements (in `status-tooling-js`)
- Proposals for spec changes (via issues and design notes in `status-spec`)

### What We Do Not Accept Without Prior Discussion

- Changes to locked architectural decisions (six-layer model)
- Scope expansion beyond web services for v1
- New repositories
- New tooling packages

## Developer Certificate of Origin (DCO)

All contributions to this project must be signed off under the [Developer Certificate of Origin (DCO)](https://developercertificate.org/), version 1.1:

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.

Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

### How to Sign Off

Add a `Signed-off-by` line to each commit message:

```
Signed-off-by: Your Name <your.email@example.com>
```

You can do this automatically with `git commit -s`.

## Licensing

- **Specification and governance documents** are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **Code** (tooling, test runners, validators) is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

By contributing, you agree that your contributions will be licensed under the applicable license for the repository you are contributing to.

## Questions?

See [SUPPORT.md](SUPPORT.md) for support channels, or open a discussion on the relevant repository.
