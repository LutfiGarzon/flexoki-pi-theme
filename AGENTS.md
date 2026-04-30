# flexoki-pi-theme Development Rules

## Commit Convention

This project uses [semantic-release](https://semantic-release.gitbook.io/semantic-release) for automated versioning and publishing. All commits must follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <description>
```

### Types

| Type | Version bump | Example |
|------|-------------|---------|
| `feat` | minor | `feat: add nord color variant` |
| `fix` | patch | `fix: correct link color contrast` |
| `perf` | patch | `perf: remove unused color vars` |
| `refactor` | patch | `refactor: rename accent variables` |
| `style` | patch | `style: align hex case formatting` |
| `docs` | patch | `docs: update install instructions` |
| `chore` | patch | `chore: bump schema URL` |
| `ci` | patch | `ci: add publish workflow` |

Breaking changes: add `!` after type/scope or `BREAKING CHANGE:` footer.

```
feat!: rename black var to ink

refactor(vars)!: drop legacy palette tokens
```

## Pull Requests

- **PR title must follow the commit convention above.** The title becomes the squash-merge commit message.
- Only **squash and merge** is used so the PR title is the single commit that triggers release.
- Branch names are freeform (`ci/`, `feat/`, `fix/`).
- Keep PRs focused — one theme change per PR.

## Publishing

Merging to `main` triggers the release workflow. No manual version bumps in `package.json` — semantic-release handles it.
