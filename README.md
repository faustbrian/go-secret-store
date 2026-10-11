# go-secret-store

> **Status: planned boundary only.** This repository does not currently
> provide an installable package, runtime API, implementation contract, tag,
> or released version.

`go-secret-store` records a reserved Golib repository identity. The frozen
cohesion review deliberately leaves its package responsibility, family,
dependencies, backends, lifecycle, ownership, error model, and sensitive-data
policy unclassified until separate repository authority defines them.

## Current boundary

The root module declaration gives repository tooling a stable identity for the
planning record. It does not establish a public package identifier or promise
that future implementation will use the inferred `secretstore` package name.

There is no production source, install command, runtime behavior, compatibility
contract, tag, or release. No consumer should import this module in its current
state.

## Planning and verification

The [repository goal](docs/goal.md) and `modules.json` retain the planning-only,
non-releasable state. The module intentionally has no cohesion classification,
because the frozen decisions withhold one for this boundary. That excludes it
from the installable consumer catalog while preserving it in engineering
inventory.

The local `make ci` target is the single source for the hosted planning
contract. It checks the repository, cohesion metadata, current online
specification authorities, and every manifest-selected module contract with the
checksum-pinned `go-library-tools` v1.4.0 release declared in `.golib.yaml`.

Passing those checks proves only that this planning scaffold and its explicit
absence claims are internally consistent. It does not prove a secret-store API
or behavior.

The [security policy](SECURITY.md) provides private reporting. The
[versioned planning threat model](docs/security/threat-model.md) covers
repository integrity and the risk of unsupported security claims; it does
not assign a future runtime responsibility or sensitive-data contract.

The prepared `make fast-check GOLIB=/path/to/golib` entry point checks
configuration, repository structure, cohesion, offline specification decisions,
local documentation links and secrets. It does not run application tests or
online documentation campaigns. This entry point requires a verifier supporting
`golib docs check --local` and `golib secrets check`; the currently declared
v1.4.0 verifier does not support it. CI and `make ci` retain their existing
contract until a capable published verifier is qualified and adopted. Do not
treat the prepared command as the current required CI route.

See the versioned [Golib ecosystem index](https://github.com/faustbrian/go-library-tools/blob/v1.4.0/docs/ecosystem/README.md)
for the shared design language.

## License

MIT. See [LICENSE](LICENSE).
