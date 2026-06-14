<div align="center">

# RemoCode IDE

### 终端优先的 macOS 原生 IDE — 为 Vibe Coding 而生

离开工位时，在 Discord 里继续指挥 Agent。

[![最新版本](https://img.shields.io/github/v/release/BlueOriginAI/RemocodeIDE?label=最新版本&color=0071e3)](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)
[![平台](https://img.shields.io/badge/macOS-14%2B-1d1d1f?logo=apple&logoColor=white)](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)
[![架构](https://img.shields.io/badge/Apple%20Silicon-arm64-248a3d)](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)
[![下载量](https://img.shields.io/github/downloads/BlueOriginAI/RemocodeIDE/total?label=下载量&color=5865f2)](https://github.com/BlueOriginAI/RemocodeIDE/releases)

**[⬇️ 下载最新版](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)** · **[🌐 官网 ide.remocode.cc](https://ide.remocode.cc)** · **[💬 Discord 远程配置教程](https://ide.remocode.cc/docs/discord-bot)**

<br/>

<img src="assets/remocode-ide-preview.png" width="880" alt="RemoCode IDE — 终端、文件树与源代码管理" />

</div>

---

## 为什么是 RemoCode

> 传统 IDE 是文件中心，RemoCode 是任务中心：先看正在跑的东西，再看需要改的代码。

> Vibe Coding 不是自动补全，而是人、终端、Git、Agent 共同迭代。IDE 必须把这些状态放在一个可扫视的界面里。

> macOS 原生体验保留了桌面工具的速度和质感，同时通过远程配置接入云端算力和持续运行的工作区。

|  |  |  |
| :-- | :-- | :-- |
| **⌨️ Terminal-first** | **🌿 Git-aware** | **📡 Remote-ready** |
| 启动即进入执行现场 | 变更树和 PR 都在右侧面板 | Discord 远程指挥 Agent，订阅后登记远程工作区 |

---

## 把编码现场整理成一个连续界面

### 🖥 命令行是第一现场
启动默认进入终端，文件、Git、Agent 输出都围绕当前工作区展开，减少在编辑器和 shell 之间反复切换。

### 🌿 Git 面板贴着工作流走
变更树、提交、PR、历史记录和远程同步在同一个上下文里完成，适合多分支、多 worktree 的 Vibe Coding 节奏。

### 🤖 为 Agent 协作设计
RemoCode 把终端会话、文件树、变更状态和上下文保留在 IDE 内，让人和 Agent 可以围绕同一个工作面推进。

### 💬 Discord 远程控制
绑定 Discord 机器人后，人不在 Mac 前也能给 Claude Code、Codex 派任务、看进度、收结果，IDE 持续在线干活。

---

## 人在外面，Agent 在 Mac 上继续干活

绑定一个 Discord 机器人，在手机上发任务、盯进度、收结果，回到工位时改动已在 Git 面板里等你。

- **📱 手机就是遥控器** — 在 Discord 私信或频道里发一条命令，Mac 上的 IDE 立即启动 Agent 开始执行。
- **🔐 白名单与本机令牌** — 只响应允许的用户 ID，机器人令牌保存在 Mac 本机；远程命令仅限 IDE 已知的项目和工作树。
- **📥 结果回传到对话** — Agent 的执行进度、终端输出和变更摘要直接回到 Discord 消息流，随时接住上下文。

```text
# dev · RemoCode Remote                                        ● 已连接

你          !rc run 修复登录页在窄屏下的布局问题
RemoCode    ▶ 已在 remocode-ide 启动 Claude Code，开始处理…
RemoCode    ✓ 完成：globals.css、login-panel.tsx 共 2 个文件已修改，构建通过。
你          !rc status
RemoCode    ● 已连接 · 当前无运行中任务 · 工作树 main 干净
```

<div align="center">
<img src="assets/discord-bot-joined.webp" width="620" alt="Discord 机器人已加入服务器" />
</div>

> 完整的机器人配置步骤见 **[Discord 远程配置教程](https://ide.remocode.cc/docs/discord-bot)**。

---

## Vibe Coding 工作流

1. 打开项目后直接回到终端上下文
2. 让 Agent 改代码，同时在文件树和 Git 面板里检查影响面
3. 用树状变更视图整理提交，必要时切换 PR 和历史记录
4. 绑定 Discord 机器人，出门后继续在手机上给 Agent 派任务
5. 订阅 RemoCode Pro 后登记远程机器，让 IDE 接入长时间运行的工作区

---

## ⬇️ 下载与安装

| 文件 | 平台 | 系统要求 |
| --- | --- | --- |
| [**Remocode-arm64.dmg**](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest) | Apple Silicon（M 系列） | macOS 14 (Sonoma) 及以上 |

1. 在 **[Releases](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)** 下载最新的 `.dmg`。
2. 打开 DMG，把 **Remocode** 拖进「应用程序」。
3. **首次打开**：当前版本尚未经 Apple 公证，请 **右键点击 App → 打开 → 再点「打开」**（仅需一次）。
4. 应用内置 **Sparkle 自动更新**，安装一次后即可自动获取后续版本。

---

## RemoCode Pro

购买 RemoCode Pro 后即可在 IDE 内登记远程设备、接入长时间运行的工作区，订阅绑定到登录账户。
详情与订阅见 **[ide.remocode.cc/#pricing](https://ide.remocode.cc/#pricing)**。

---

## 关于本仓库

本仓库**仅用于对外发布、下载地址维护与项目宣传**，不包含任何源代码。
所有正式构建以 [Releases](https://github.com/BlueOriginAI/RemocodeIDE/releases) 形式发布。

<div align="center">

**[官网](https://ide.remocode.cc)** · **[下载](https://github.com/BlueOriginAI/RemocodeIDE/releases/latest)** · **[Discord 教程](https://ide.remocode.cc/docs/discord-bot)** · **[RemoCode Pro](https://ide.remocode.cc/#pricing)**

</div>
