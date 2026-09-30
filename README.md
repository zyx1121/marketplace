# zyx1121 marketplace

Solution plugins for Codex and Claude Code by [zyx1121](https://github.com/zyx1121).

## Install

Ask your agent to install a plugin from this marketplace, or use the host CLI.

```sh
# Claude Code
claude plugin marketplace add zyx1121/marketplace
claude plugin install fde@zyx1121

# Codex versions with plugin add
codex plugin marketplace add zyx1121/marketplace
codex plugin add fde@zyx1121
```

## Plugins

| Plugin | Version | Purpose |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.1.0 | Build and operate live client POCs through shared skills, MCP tools and scripts. |

Each plugin owns its source and releases. This marketplace pins release commits.
The Claude-compatible catalog is shared by both hosts.

The existing `zyx@zyx` all-purpose plugin remains available separately during
incremental migration; registering this marketplace does not replace it.

## License

[MIT](LICENSE.md) — borrow what you like.
