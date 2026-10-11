<!-- 翻譯自 README.md @ docs/readme-template-v2。只翻 "For AI agents" 以上的章節，英文版更新時一起改。 -->

<div align="center">

<h1>zyx1121 marketplace</h1>

<p><strong>一份目錄，就能在 Claude Code 和 Codex 安裝 zyx1121 的 plugin。</strong></p>

[![CI](https://img.shields.io/github/actions/workflow/status/zyx1121/marketplace/check.yml?branch=main&style=flat-square&label=CI)](https://github.com/zyx1121/marketplace/actions)
[![Claude Code](https://img.shields.io/badge/Claude_Code-marketplace-D97757?style=flat-square)](https://github.com/zyx1121/marketplace)
[![License](https://img.shields.io/github/license/zyx1121/marketplace?style=flat-square)](LICENSE.md)

[English](README.md) | **繁體中文** | [简体中文](README.zh-CN.md)

</div>

每個 plugin 都有自己的 repo 和發版。這個 marketplace 釘住每個 plugin 的一個發版 commit，讓兩邊安裝到的都是同一個測過的版本。

## 功能

- **釘住發版**：每一項都用完整 SHA 指向發版 commit，而不是會變動的分支。
- **兩邊共用**：Claude Code 和 Codex 讀同一份 Claude 相容的目錄。
- **保護目錄**：缺 SHA，或 README 顯示的版本不一致時，CI 就會失敗。

## 快速開始

```sh
claude plugin marketplace add zyx1121/marketplace
claude plugin install pve@zyx1121
```

Codex：先 `codex plugin marketplace add zyx1121/marketplace`，再 `codex plugin add pve@zyx1121`。開新的對話才會載入 plugin。

## Plugin

| Plugin | 版本 | 用途 |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.2.0 | 用共用的 skill、MCP 工具和腳本建立並維運客戶 POC。 |
| [task-web](https://github.com/zyx1121/task-web) | 0.4.0 | 用 zyx 模板做個人網頁工具和研究 demo。 |
| [pve](https://github.com/zyx1121/pve) | 0.1.2 | 透過 MCP 操作 Proxmox guest、port forwarding、內部 DNS 和 Caddy。 |
| [nycu](https://github.com/zyx1121/nycu) | 0.2.0 | 透過 MCP 使用陽明交大入口網站、E3、公開課表和兼任簽到。 |
| [macos](https://github.com/zyx1121/macos) | 0.3.0 | 透過 MCP 使用行事曆、提醒事項、備忘錄、郵件草稿、Safari 和截圖。 |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | 透過 MCP 查 Uber Eats 訂單紀錄、收據和團購帳本。 |
| [zyx](https://github.com/zyx1121/plugin) | 0.29.0 | 簡報、文件、學術寫作、Next.js 和開發流程的 skill。 |

個人頁面用 task-web，已設定好的客戶環境用 fde。個人任務跑在 FDE 工作區時，兩個一起用。

Claude Code 從自己的 marketplace 安裝完整的 `zyx@zyx`，包含 agent 和 utils MCP server。Codex 從這裡安裝 `zyx@zyx1121`，只有 skill。

## 其他

給 AI agent 的結構化資訊在[英文版](README.md#for-ai-agents)。

## 授權

[MIT](LICENSE.md)
