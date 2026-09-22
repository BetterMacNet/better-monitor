# Better Monitor

[English](README.md) · 简体中文

<img src="assets/logo.png" alt="Better Monitor" width="160">

一款专注于 macOS 的系统监控工具，帮助你快速了解 Mac 当前正在做什么。

Better Monitor 将进程、网络、端口和启动项信息集中在一个原生 macOS 应用中：日常使用时看概览，需要排查问题时再深入细节。

## 主要功能

- **监控概览** — 一眼查看 CPU、内存、磁盘、网络、电池、传感器和运行中进程的状态。
- **进程监控** — 查看资源占用和进程详情，并对你有权限控制的进程执行操作。
- **网络活动** — 查看当前连接、流量、网络接口、协议和目标地址。
- **端口与服务** — 找出监听端口、对应进程，并展示有帮助的风险信号。
- **启动项** — 审查启动项、当前资源影响，以及可以在应用内管理的条目。
- **可选 AI 助手** — 配置你自己的服务商，在启用后使用 AI 辅助进程诊断。
- **原生 macOS 体验** — 基于 SwiftUI 构建，支持 macOS 15 及更高版本。

## 系统要求

- macOS 15.0（Sequoia）或更高版本
- 通用二进制 — 同时支持 Apple 芯片与 Intel

## 安装

使用 [Homebrew](https://brew.sh)：

```bash
brew install --cask bettermacnet/tap/better-monitor
```

或从[最新发布](https://github.com/BetterMacNet/better-monitor/releases/latest)下载磁盘映像。

每个发布版本都使用 Developer ID 证书签名并经 Apple 公证，公证票据已装订到磁盘映像上，因此首次启动无需联网。

## 权限说明

部分信息取决于 macOS 的隐私权限：

- 「网络活动」页面显示当前 Wi-Fi 名称需要定位权限。
- macOS 可能限制应用读取进程和端口的详细信息。
- Better Monitor 不会使用你的位置信息；只是 macOS 要求通过该权限提供 Wi-Fi 名称。

## 文档

- [功能介绍](docs/features.md)
- [使用说明](docs/usage.md)
- [Release notes](docs/release-notes.md)
- [用户规则](RULES.md)
- [BetterMac 官网](https://bettermac.net/)

## 许可说明

Better Monitor 及本仓库中的原创材料均为专有内容，并非开源软件。版权所有。未经 BetterMacNet 事先书面许可，不授予复制、修改、分发或使用这些内容的任何许可。

## 支持

- [支持中心](https://bettermac.net/en/support/?product=better-monitor)
- [联系我们](https://bettermac.net/en/contact/?product=better-monitor)
- [使用条款](https://bettermac.net/en/terms/)
- [隐私政策](https://bettermac.net/en/privacy/)

---

本公开仓库存放产品介绍、使用文档和发布下载；应用源代码保持私有。
