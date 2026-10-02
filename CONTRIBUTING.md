# Contributing to agentsec-ecosystem

Thanks for helping make agents safer to run. This org contains many repositories, so the process
below is the default; a repository's own `CONTRIBUTING.md` overrides it.

## Before you start

- For bugs and small fixes, open an issue or a pull request directly.
- For new features or changes that affect an interface others depend on, open an issue first so we
  can agree on the approach.
- For security issues, do **not** open a public issue — follow [`SECURITY.md`](./SECURITY.md).

## Development flow

1. Fork the repository (or create a branch if you have write access).
2. Branch from `main`: `git checkout -b feat/short-description`.
3. Keep changes focused; one logical change per pull request.
4. Add or update tests for any behavior change.
5. Run the repository's formatter, linter, and test suite before pushing.
6. Open a pull request and fill in the template. Link the issue it closes.

## Pull request expectations

- `main` is protected: changes land through pull requests with passing checks.
- Keep the diff reviewable. Prefer several small pull requests over one large one.
- Explain **why**, not just **what**, in the description.
- A maintainer will review, request changes, or merge.

## Commit messages

Use clear, imperative subject lines (`add rate-limit policy action`, not `added stuff`).
Conventional Commits are welcome but not required.

## Developer Certificate of Origin (DCO)

Every commit must be signed off. Add a `Signed-off-by` line with your real name and email:

```sh
git commit -s -m "add rate-limit policy action"
```

Which produces:

```
Signed-off-by: Jane Dev <jane@example.com>
```

By signing off you certify the [Developer Certificate of Origin](./DCO). We do **not** use a CLA.
A CI check enforces this on pull requests; to fix a missing sign-off, amend or rebase with `-s`.

## Licensing

By contributing, you agree that your contributions are licensed under the Apache License 2.0 (see
the repository's `LICENSE`). Do not add code you cannot license this way; note third-party
attribution in `THIRD_PARTY_NOTICES.md` where it applies.

See [GOVERNANCE.md](./GOVERNANCE.md) for the maintainer ladder, review rules, and decision-making.

## Code of conduct

Participation is governed by our [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md).
