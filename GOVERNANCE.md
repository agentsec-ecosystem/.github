# Governance

> Governance is a product feature. The OSS agent-security landscape is mostly single-maintainer,
> research-grade projects — the fragility enterprise users cannot accept. This is our policy, not a
> slogan.

## Roles

- **Contributor** → **Reviewer** → **Maintainer** (ladder below).
- The **Owner** (`@deghosal-2026`) is the founding admin and steward of the brand and the
  security-event schema.

## Maintainer ladder

Criteria are **time- and contribution-based, never popularity-based**.

| Stage | Criteria | Rights |
|---|---|---|
| Contributor | 1+ merged PR, or a reviewed rule/attack pack | none |
| Reviewer | 5+ substantive merged contributions over 2+ months; nominated by 2 maintainers | review, triage |
| Maintainer | 15+ merged contributions over 6+ months; sustained review record; accepts the trust duties | merge, release, CODEOWNERS |

## Multi-maintainer rule

1. Every repo: **≥2 maintainers from day one; ≥3 before 1.0**.
2. Enforcement paths, policy defaults, and anything touching secrets/revocation require **2-party
   review**, encoded in `CODEOWNERS`, not convention.
3. Security-sensitive paths additionally require a signed-off threat-model delta note in the PR.
4. **Current documented exception:** the organization launched with a single maintainer (the Owner).
   Until a second maintainer is added, the Owner is the sole maintainer and every change is
   self-reviewed against this policy. **Recruiting a second maintainer is a P0 governance task.**
   *Kill criterion:* if no second maintainer exists by the first public release, that release is
   explicitly labeled single-maintainer.

## Decision making

- **Lazy consensus:** an issue or PR proposal is accepted if no maintainer objects within 72 hours.
- Changes to the security-event schema, the LICENSE, or this document require explicit maintainer
  approval.
- The security-event schema is versioned and follows a published deprecation policy.

## Ecosystem council

Maintainers across tools meet monthly for release-wave coordination, shared non-functional floor
enforcement, and cross-tool API/schema changes. The event schema is the contract.

## Shared contracts

Shared components (the security-event schema, the audit-log format) live in **one governed repo**,
not copied per tool — one source of truth. Their changes are versioned like an API.

## Supply chain

- Release artifacts are **signed with provenance attestation**; upgrade paths are SHA-pinned.
- Dependency additions require maintainer review + SBOM update + license scan.
- **OpenSSF Scorecard** runs on every repo; target grade **A**, tracked per release.
- **DCO sign-off** is required on every commit — see [CONTRIBUTING](./CONTRIBUTING.md).

## Conduct and security

- [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)
- [SECURITY.md](./SECURITY.md)
