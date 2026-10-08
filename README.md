# zyx1121 marketplace

Solution plugins for Codex and Claude Code by [zyx1121](https://github.com/zyx1121).

## Install

Ask your agent to install a plugin from this marketplace, or use the host CLI.

```sh
# Claude Code
claude plugin marketplace add zyx1121/marketplace
claude plugin install fde@zyx1121
claude plugin install task-web@zyx1121
claude plugin install pve@zyx1121
claude plugin install nycu@zyx1121
claude plugin install macos@zyx1121
claude plugin install ubereats@zyx1121

# Codex versions with plugin add
codex plugin marketplace add zyx1121/marketplace
codex plugin add fde@zyx1121
codex plugin add task-web@zyx1121
codex plugin add pve@zyx1121
codex plugin add nycu@zyx1121
codex plugin add macos@zyx1121
codex plugin add ubereats@zyx1121
codex plugin add zyx@zyx1121
```

## Plugins

| Plugin | Version | Purpose |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.1.1 | Build and operate live client POCs through shared skills, MCP tools and scripts. |
| [task-web](https://github.com/zyx1121/task-web) | 0.2.0 | Personal web tools and research demos with the zyx template, separate from FDE operations. |
| [pve](https://github.com/zyx1121/pve) | 0.1.0 | Operate Proxmox guests, port forwarding, internal DNS and Caddy through MCP. |
| [nycu](https://github.com/zyx1121/nycu) | 0.1.0 | NYCU portal, E3 coursework, public timetable and part-time attendance through MCP. |
| [macos](https://github.com/zyx1121/macos) | 0.2.0 | Native Notes, Calendar and Reminders with consistent IDs, schedules and conflict protection, plus Mail, Safari and screenshots through MCP. |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | Uber Eats order history, receipts and group-order ledgers through MCP. |
| [zyx](https://github.com/zyx1121/plugin) | 0.29.0 | Skills for slides, docs, academic writing, Next.js and the dev workflow. |

Task Web supplies the personal template. FDE operates configured environments.
Use them together when a personal task runs in an FDE workspace, or separately
when the project already has its own design or deployment workflow.

Each plugin owns its source and releases. This marketplace pins release commits.
The Claude-compatible catalog is shared by both hosts.

Claude Code keeps installing the all-purpose plugin as `zyx@zyx` from its own
marketplace, which also brings its agents and the utils MCP server. Codex
installs `zyx@zyx1121` from here and gets the skills only.

## License

[MIT](LICENSE.md): borrow what you like.
