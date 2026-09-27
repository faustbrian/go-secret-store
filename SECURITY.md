# Security policy

## Current boundary

This repository is planned, unclassified and non-releasable. It provides no
runtime package, secret-management API, backend, cryptographic construction,
supported version or installable security product. The repository name and
module declaration do not establish a sensitive-data or custody contract.

The [planning threat model](docs/security/threat-model.md) describes the
present repository boundary. It does not prove future runtime protections or
authorize an implementation. No version is supported for production use.

## Private reporting and disclosure

Report security-sensitive defects in the repository, automation or planning
claims through [GitHub private vulnerability reporting](https://github.com/faustbrian/go-secret-store/security/advisories/new).
Do not include exploit details, private reporter data, credentials or actual
secret material in public issues or examples.

Provide the affected commit or document, expected impact, relevant trust
boundary and a minimal sanitized reproduction when possible. The repository
maintainer owns acknowledgement, severity assessment, remediation coordination
and disclosure. This planning policy does not promise response times or runtime
support.

Coordinate disclosure privately. Identify affected automation or documents
accurately; do not invent affected module releases for a repository with no
runtime or published version. Confirmed future runtime vulnerabilities will
require regression evidence, upgrade guidance and coordinated publication
before a remediation claim. Planning or automation corrections need not create
a module release.

## Release verdict

Non-releasable. Scope classification and implementation require separate
reviewed authority and executable acceptance evidence. The absence of runtime
source is not evidence of a secure implemented secret store. Repository
automation and documentation remain subject to review and required CI.
