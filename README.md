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

Local and hosted verification preserve the same planning structure, cohesion,
offline specification and local-link contracts with the checksum-pinned public
`go-library-tools` v2.1.2 release declared in `.golib.yaml`. Local Make scans
whole-tree secrets; hosted PR/push scans the exact committed change range.

Passing those checks proves only that this planning scaffold and its explicit
absence claims are internally consistent. It does not prove a secret-store API
or behavior.

The [security policy](SECURITY.md) provides private reporting. The
[versioned planning threat model](docs/security/threat-model.md) covers
repository integrity and the risk of unsupported security claims; it does
not assign a future runtime responsibility or sensitive-data contract.

Use the checksum-verified public `golib` v2.1.2 release declared in
`.golib.yaml`, with Go 1.27.2 as the verification producer. The planned module's
minimum remains Go 1.27.0; no runtime package or release is introduced.
An ordinary standalone checkout is sufficient, without sibling repositories,
goal ledgers or building Tools from source:

```sh
make check
make ci
```

Both routes, and the `make fast-check` alias, check configuration, repository
structure, cohesion, offline specification decisions, local documentation links
and unconditional whole-tree secrets. They run no application tests, mutation
campaigns or release checks. Hosted Required applies the same structural checks
and scans committed changed content against the exact validated PR base or push
before commit, without a fallback base or a duplicate full-history scan.
Missing or invalid change identities and failed checks remain failures.

`make check-full` optionally preserves the previous full manifest-selected
contract, including broad spelling and external-link documentation assurance.
It is not an ordinary CI prerequisite and does not establish runtime or release
qualification for this planned module.

`make check-online` explicitly adds authoritative specification refresh to the
local contract. Scheduled and manual CI also refresh those authorities online
and run whole-tree secrets. Passing any of these planning routes is not runtime
security or release qualification.

See the versioned [Golib ecosystem index](https://github.com/faustbrian/go-library-tools/blob/v1.4.0/docs/ecosystem/README.md)
for the shared design language.

## License

MIT. See [LICENSE](LICENSE).

## Documentation navigation

[Complete documentation map](docs/README.md#complete-documentation-map)

Use the [versioned ecosystem entry](https://github.com/faustbrian/go-library-tools/blob/v1.4.0/docs/ecosystem/README.md) for package
selection. The [frozen compatibility cohort](https://github.com/faustbrian/go-library-tools/blob/v1.8.4/docs/ecosystem/compatibility-sets.md)
is separate from current package releases and unpublished source changes.
Adopting them does not silently update that cohort.
