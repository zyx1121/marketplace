# zyx1121 marketplace

Solution plugins for Codex and Claude Code by [zyx1121](https://github.com/zyx1121).

## Install

Ask your agent to install a plugin from this marketplace, or use the host CLI.

```sh
# Claude Code
claude plugin marketplace add zyx1121/marketplace
claude plugin install fde@zyx1121
claude plugin install pve@zyx1121
claude plugin install nycu@zyx1121
claude plugin install macos@zyx1121
claude plugin install ubereats@zyx1121

# Codex versions with plugin add
codex plugin marketplace add zyx1121/marketplace
codex plugin add fde@zyx1121
codex plugin add pve@zyx1121
codex plugin add nycu@zyx1121
codex plugin add macos@zyx1121
codex plugin add ubereats@zyx1121
```

## Plugins

| Plugin | Version | Purpose |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.1.0 | Build and operate live client POCs through shared skills, MCP tools and scripts. |
| [pve](https://github.com/zyx1121/pve) | 0.1.0 | Operate Proxmox guests, port forwarding, internal DNS and Caddy through MCP. |
| [nycu](https://github.com/zyx1121/nycu) | 0.1.0 | NYCU portal, E3 coursework, public timetable and part-time attendance through MCP. |
| [macos](https://github.com/zyx1121/macos) | 0.1.0 | macOS Calendar, Reminders, Mail, Safari and screenshots through MCP. |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | Uber Eats order history, receipts and group-order ledgers through MCP. |

Each plugin owns its source and releases. This marketplace pins release commits.
The Claude-compatible catalog is shared by both hosts.

The existing `zyx@zyx` all-purpose plugin remains available separately during
incremental migration; registering this marketplace does not replace it.

## License

[MIT](LICENSE.md) — borrow what you like.
