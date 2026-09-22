# Better Monitor

[English](#english) · [简体中文](#简体中文)

![Better Monitor](assets/logo.png)

## English

A focused macOS system monitor for understanding what your Mac is doing right now.

Better Monitor brings process, network, port, and startup-item information into one native macOS app, with a clear overview for everyday diagnosis and a detailed view when you need to investigate further.

### Highlights

- **Monitoring overview** — See the health of CPU, memory, disk, network, battery, sensors, and running processes at a glance.
- **Process monitor** — Inspect resource usage and process details, with actions for processes you control.
- **Network activity** — Review active connections, traffic, interfaces, protocols, and destinations.
- **Ports and services** — Find listening ports, identify their owning processes, and surface useful risk signals.
- **Startup items** — Review startup entries, current resource impact, and the items that can be managed from the app.
- **Optional AI assistance** — Configure your own provider and use AI-powered process diagnostics when enabled.
- **Native macOS experience** — Built for macOS 15 or later, with a native SwiftUI interface.

### Requirements

- macOS 15.0 or later

### Install

Better Monitor is not publicly released yet. The product website and download link will be added here when the first signed release is published.

Homebrew Cask installation is supported when the cask is published:

```bash
brew install --cask better-monitor
```

### Permissions

Some information depends on macOS privacy permissions:

- Location permission is needed to show the current Wi-Fi network name on the Network Activity page.
- Process and port details may be limited by macOS when the system does not expose them to the app.
- Better Monitor does not need your location for location services; macOS requires this permission to provide the Wi-Fi name.

### Documentation

- [Features](docs/features.md)
- [Usage guide](docs/usage.md)
- [Release notes](docs/release-notes.md)
- [User rules](RULES.md)
- [Website](https://bettermac.net/)

### Brand asset

![Better Monitor logo](assets/logo.png)

### Support

Product information and download links will be added when Better Monitor is publicly released.

## 简体中文

一款专注于 macOS 的系统监控工具，帮助你快速了解 Mac 当前正在做什么。

Better Monitor 将进程、网络、端口和启动项信息集中在一个原生 macOS 应用中：日常使用时看概览，需要排查问题时再深入细节。

### 主要功能

- **监控概览** — 一眼查看 CPU、内存、磁盘、网络、电池、传感器和运行中进程的状态。
- **进程监控** — 查看资源占用和进程详情，并对你有权限控制的进程执行操作。
- **网络活动** — 查看当前连接、流量、网络接口、协议和目标地址。
- **端口与服务** — 找出监听端口、对应进程，并展示有帮助的风险信号。
- **启动项** — 审查启动项、当前资源影响，以及可以在应用内管理的条目。
- **可选 AI 助手** — 配置你自己的服务商，在启用后使用 AI 辅助进程诊断。
- **原生 macOS 体验** — 基于 SwiftUI 构建，支持 macOS 15 及更高版本。

### 系统要求

- macOS 15.0 或更高版本

### 安装

Better Monitor 目前尚未公开发布。首个签名版本发布后，会在这里补充产品官网和下载链接。

如果对应的 Homebrew Cask 已发布，也可以使用 Homebrew 安装：

```bash
brew install --cask better-monitor
```

### 权限说明

部分信息取决于 macOS 的隐私权限：

- 「网络活动」页面显示当前 Wi-Fi 名称需要定位权限。
- macOS 可能限制应用读取进程和端口的详细信息。
- Better Monitor 不会使用你的位置信息；只是 macOS 要求通过该权限提供 Wi-Fi 名称。

### 文档

- [功能介绍](docs/features.md)
- [使用说明](docs/usage.md)
- [Release notes](docs/release-notes.md)
- [用户规则](RULES.md)
- [BetterMac 官网](https://bettermac.net/)

### 品牌素材

![Better Monitor Logo](assets/logo.png)

### 支持

Better Monitor 正式公开发布后，会在这里补充产品信息和下载链接。

---

The public repository contains product information and release materials; application source code remains private. Signed and notarized distribution details will be added with the first public release.
