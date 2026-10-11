# marketplace

Catalog that pins zyx1121 plugins to release commits for Claude Code and Codex. Read [README.md](README.md) first.

## Pin a new release

1. Merge the release in the plugin repo, so that its version is on `main`.
2. In `.claude-plugin/marketplace.json`, set the entry's `version` and its `source.sha` to the full 40-character commit SHA of that release.
3. In `README.md`, set the same version in the plugin's table row. CI compares the two.
4. Open a PR titled `chore: pin <name> <version>`, wait for the check, and squash-merge it.
5. Update the installed copy: `claude plugin marketplace update zyx1121`, then `claude plugin update <name>@zyx1121`. Start a new session to load it.

## Rules

- Every entry uses `"source": "url"`, a `https://github.com/` URL and a full SHA. Never point at a branch.
- One entry per plugin name.
- Keep the table row format `| [<name>](<url>) | <version> | <purpose> |`. The CI check finds rows by this prefix.
- Repository documents are English.
