<div align="center">

<h1>zyx1121 marketplace</h1>

<p><strong>One catalog that installs zyx1121 plugins in Claude Code and Codex.</strong></p>

[![CI](https://img.shields.io/github/actions/workflow/status/zyx1121/marketplace/check.yml?branch=main&style=flat-square&label=CI)](https://github.com/zyx1121/marketplace/actions)
[![Claude Code](https://img.shields.io/badge/Claude_Code-marketplace-D97757?style=flat-square)](https://github.com/zyx1121/marketplace)
[![License](https://img.shields.io/github/license/zyx1121/marketplace?style=flat-square)](LICENSE.md)

**English** | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md)

</div>

Each plugin keeps its own repo and releases. This marketplace pins one release commit of each, so both hosts install the same tested version.

## Features

- **Pins releases**: each entry points at a release commit by its full SHA, not at a moving branch.
- **Serves both hosts**: Claude Code and Codex read the same Claude-compatible catalog.
- **Guards the catalog**: CI fails when an entry has no SHA or when the README shows a different version.

## Quick start

```sh
claude plugin marketplace add zyx1121/marketplace
claude plugin install pve@zyx1121
```

Codex: `codex plugin marketplace add zyx1121/marketplace`, then `codex plugin add pve@zyx1121`. Start a new session to load the plugin.

## Plugins

| Plugin | Version | Purpose |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.2.0 | Build and operate live client POCs with shared skills, MCP tools and scripts. |
| [task-web](https://github.com/zyx1121/task-web) | 0.4.0 | Personal web tools and research demos on the zyx template. |
| [pve](https://github.com/zyx1121/pve) | 0.1.2 | Proxmox guests, port forwarding, internal DNS and Caddy through MCP. |
| [nycu](https://github.com/zyx1121/nycu) | 0.2.0 | NYCU portal, E3 coursework, the public timetable and part-time attendance through MCP. |
| [macos](https://github.com/zyx1121/macos) | 0.3.0 | Calendar, Reminders, Notes, Mail drafts, Safari and screenshots through MCP. |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | Uber Eats order history, receipts and group-order ledgers through MCP. |
| [zyx](https://github.com/zyx1121/plugin) | 0.29.0 | Skills for slides, documents, academic writing, Next.js and the dev workflow. |

Use task-web for a personal page and fde for a configured client environment. Use both when a personal task runs in an FDE workspace.

Claude Code installs the full `zyx` plugin as `zyx@zyx` from its own marketplace, with its agents and the utils MCP server. Codex installs `zyx@zyx1121` from here and gets the skills only.

## For AI agents

Facts for coding agents and LLM tools. The rules for changing the catalog are in [AGENTS.md](AGENTS.md).

- **Summary**: Claude Code and Codex plugin marketplace that pins zyx1121 plugins to release commits.
- **Type**: plugin
- **Interfaces**: the catalog `.claude-plugin/marketplace.json`. No CLI, MCP or HTTP service.
- **Install**: `claude plugin marketplace add zyx1121/marketplace`
- **Run**: `claude plugin install <name>@zyx1121`
- **Verify**: `claude plugin list` shows the plugin with the version in the table above
- **Config**: none
- **Secrets**: none
- **Limits**: a plugin release reaches users only after a pin update here.

## License

[MIT](LICENSE.md)
