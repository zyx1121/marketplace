<!-- 翻译自 README.md @ docs/readme-template-v2。只翻译 "For AI agents" 之前的章节，英文版更新时一起改。 -->

<div align="center">

<h1>zyx1121 marketplace</h1>

<p><strong>一份目录，就能在 Claude Code 和 Codex 安装 zyx1121 的插件。</strong></p>

[![CI](https://img.shields.io/github/actions/workflow/status/zyx1121/marketplace/check.yml?branch=main&style=flat-square&label=CI)](https://github.com/zyx1121/marketplace/actions)
[![Claude Code](https://img.shields.io/badge/Claude_Code-marketplace-D97757?style=flat-square)](https://github.com/zyx1121/marketplace)
[![License](https://img.shields.io/github/license/zyx1121/marketplace?style=flat-square)](LICENSE.md)

[English](README.md) | [繁體中文](README.zh-TW.md) | **简体中文**

</div>

每个插件都有自己的 repo 和发版。这个 marketplace 锁定每个插件的一个发版 commit，让两边安装到的都是同一个测过的版本。

## 功能

- **锁定发版**：每一项都用完整 SHA 指向发版 commit，而不是会变动的分支。
- **两边共用**：Claude Code 和 Codex 读取同一份 Claude 兼容的目录。
- **保护目录**：缺 SHA，或 README 显示的版本不一致时，CI 就会失败。

## 快速开始

```sh
claude plugin marketplace add zyx1121/marketplace
claude plugin install pve@zyx1121
```

Codex：先 `codex plugin marketplace add zyx1121/marketplace`，再 `codex plugin add pve@zyx1121`。开新的对话才会加载插件。

## 插件

| 插件 | 版本 | 用途 |
|---|---|---|
| [fde](https://github.com/zyx1121/fde) | 0.2.0 | 用共用的 skill、MCP 工具和脚本搭建并运维客户 POC。 |
| [task-web](https://github.com/zyx1121/task-web) | 0.4.0 | 用 zyx 模板做个人网页工具和研究 demo。 |
| [pve](https://github.com/zyx1121/pve) | 0.1.2 | 通过 MCP 操作 Proxmox guest、端口转发、内部 DNS 和 Caddy。 |
| [nycu](https://github.com/zyx1121/nycu) | 0.4.0 | 通过 MCP 使用阳明交大门户网站、E3、公开课表和兼任签到。 |
| [macos](https://github.com/zyx1121/macos) | 0.3.0 | 通过 MCP 使用日历、提醒事项、备忘录、邮件草稿、Safari 和截图。 |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | 通过 MCP 查询 Uber Eats 订单记录、收据和拼单账本。 |
| [zyx](https://github.com/zyx1121/plugin) | 0.29.0 | 演示文稿、文档、学术写作、Next.js 和开发流程的 skill。 |

个人页面用 task-web，已配置好的客户环境用 fde。个人任务运行在 FDE 工作区时，两个一起用。

Claude Code 从自己的 marketplace 安装完整的 `zyx@zyx`，包含 agent 和 utils MCP server。Codex 从这里安装 `zyx@zyx1121`，只有 skill。

## 其他

给 AI agent 的结构化信息见[英文版](README.md#for-ai-agents)。

## 许可证

[MIT](LICENSE.md)
