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
| [pve](https://github.com/zyx1121/pve) | 0.2.0 | 通过 MCP 操作 Proxmox guest、端口转发、内部 DNS 和 Caddy。 |
| [nycu](https://github.com/zyx1121/nycu) | 0.4.0 | 通过 MCP 使用阳明交大门户网站、E3、公开课表和兼任签到。 |
| [macos](https://github.com/zyx1121/macos) | 0.3.0 | 通过 MCP 使用日历、提醒事项、备忘录、邮件草稿、Safari 和截图。 |
| [ubereats](https://github.com/zyx1121/ubereats) | 0.1.0 | 通过 MCP 查询 Uber Eats 订单记录、收据和拼单账本。 |
| [zyx](https://github.com/zyx1121/plugin) | 0.50.1 | 演示文稿、文档、学术写作、Next.js 和开发流程的 skill。 |
| [tailscale](https://github.com/zyx1121/tailscale) | 0.1.0 | 通过 MCP 读 Tailscale 设备、线上的 policy 文件并验证 policy，只读。 |
| [stick](https://github.com/zyx1121/stick) | 0.2.0 | 通过 MCP 在 Linux 或 Windows 主机运行命令、操作 tmux 与 Windows 桌面。 |
| [secret-mod](https://github.com/zyx1121/secret-mod) | 0.1.0 | 用表单问账号密码，存进 keychain，让 Claude 用而看不到值。 |
| [hum](https://github.com/zyx1121/hum) | 0.1.0 | 输入框上方一行，显示每台机器的 CPU、内存与磁盘。 |
| [music-mod](https://github.com/zyx1121/music-mod) | 0.6.1 | 输入框上方一行，显示 Music.app 正在播的歌。 |
| [today-mod](https://github.com/zyx1121/today-mod) | 0.6.1 | 当天行程显示在输入框上方，也交给 Claude 当背景。 |
| [golem-mod](https://github.com/zyx1121/golem-mod) | 0.3.0 | golem 事件显示在输入框上方，另有通知与 /golem。 |
| [ship-mod](https://github.com/zyx1121/ship-mod) | 0.3.1 | CI 与部署进度显示在输入框上方，另有通知与 /ship。 |
| [i-have-dyslexia](https://github.com/zyx1121/i-have-dyslexia) | 0.1.0 | 把回复整理成阅读障碍者好读的格式。 |
| [admiralty-code](https://github.com/zyx1121/admiralty-code) | 0.1.0 | 用 Admiralty Code 标出每项回报的来源可靠度与可信度。 |
| [paper-generator](https://github.com/zyx1121/paper-generator) | 0.7.2 | 从研究想法到 LaTeX 论文，含模拟审稿。 |

个人页面用 task-web，已配置好的客户环境用 fde。个人任务运行在 FDE 工作区时，两个一起用。

Claude Code 从自己的 marketplace 安装完整的 `zyx@zyx`，包含 agent 和 utils MCP server。Codex 从这里安装 `zyx@zyx1121`，只有 skill。

## 其他

给 AI agent 的结构化信息见[英文版](README.md#for-ai-agents)。

## 许可证

[MIT](LICENSE.md)
