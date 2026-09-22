# Better Monitor

[English](README.md) · 简体中文

<img src="assets/logo.png" alt="Better Monitor" width="160">

一款原生 macOS 系统监控工具，帮助你了解 Mac 当前正在做什么。

Better Monitor 将进程、网络、端口、启动项和硬件信息集中在一个应用中，适合日常观察和针对性排查。

## 什么时候使用 Better Monitor

- 快速查看 CPU、内存、磁盘、网络、电池、传感器和进程状态。
- 找出 CPU 或内存占用异常高的应用或进程。
- 查看活跃网络连接、流量、协议和目标地址。
- 查看监听端口、所属进程和风险信号。
- 查看后台启动项及其当前资源影响。

## 快速开始

1. 安装 Better Monitor：

   ```bash
   brew install --cask bettermacnet/tap/better-monitor
   ```

2. 启动 Better Monitor，从左侧导航选择需要查看的页面。
3. 想快速了解状态时打开「监控概览」；需要排查具体问题时，进入进程、网络、端口或启动项页面。
4. 只有在需要显示当前 Wi-Fi 名称时才授予定位服务权限。根据权限和系统可见性，macOS 仍可能限制进程和端口详情。

也可以从[最新发布](https://github.com/BetterMacNet/better-monitor/releases/latest)下载磁盘映像，将 `Better Monitor.app` 拖入「应用程序」文件夹。每个发布版本都使用 Developer ID 证书签名并经 Apple 公证，公证票据已装订到磁盘映像上。

## 主要功能

- **监控概览** — 一眼查看系统健康度和关键资源信息。
- **进程监控** — 查看资源占用、身份、路径、网络活动和打开的文件，并对你有权限控制的进程执行操作。
- **网络活动** — 查看网络接口、连接、流量、协议、TCP 状态和目标地址。
- **端口与服务** — 找出监听端口、对应进程，并展示有帮助的风险信号。
- **启动项** — 查看可读取的 LaunchAgent 和 LaunchDaemon、当前资源影响，并通过系统设置审查现代登录项。
- **可选 AI 助手** — 配置你自己的服务商，在需要时主动请求 AI 辅助进程诊断。
- **原生 macOS 体验** — 基于 SwiftUI 构建，支持 macOS 15 及更高版本。

详情请查看[功能介绍](docs/features.md)和[使用说明](docs/usage.md)。

## 权限与能力边界

- 显示当前 Wi-Fi 名称需要定位服务权限。Better Monitor 不会将该权限用于定位服务。
- 当系统不向应用公开信息时，macOS 可能限制进程和端口详情。
- 由 macOS 管理的现代登录项需要通过「系统设置」审查，应用内不会完整管理它们。
- 非本机端口绑定只是需要进一步核对的风险信号，不代表服务已具备外部可达性，也不代表完成了安全审计。
- 启动项影响指标来自当前运行状态，不代表开机耗时，也不保证停用后一定节省资源。

## 隐私与可选 AI

核心监控默认在本机完成，不需要账号或云服务。AI 助手是可选功能：

- 只有在你配置服务商并主动请求诊断摘要后，AI 诊断才会使用网络访问。
- API 密钥保存在 macOS 钥匙串中。
- 发送诊断信息前会显示数据披露说明。
- 请求可能包含诊断所需的进程、网络、路径和文件活动摘要。启用前请查看服务商的数据处理方式。
- 应用内的本地 AI 对话和监控历史可以清除；清除不会删除已经发送给服务商的数据。
- 对于已发送用于诊断的数据，以服务商自己的保留和模型训练条款为准。

不配置 AI 也可以使用核心监控功能。

## 文档与支持

- [功能介绍](docs/features.md)
- [使用说明](docs/usage.md)
- [Release notes](docs/release-notes.md)
- [用户规则](RULES.md)
- [最新发布](https://github.com/BetterMacNet/better-monitor/releases/latest)
- [报告 Bug](https://github.com/BetterMacNet/better-monitor/issues/new?template=bug_report.md)
- [功能请求](https://github.com/BetterMacNet/better-monitor/issues/new?template=feature_request.md)
- [安全问题报告](SECURITY.md)
- [支持中心](https://bettermac.net/en/support/?product=better-monitor)
- [联系我们](https://bettermac.net/en/contact/?product=better-monitor)
- [BetterMac 官网](https://bettermac.net/)
- [隐私政策](https://bettermac.net/en/privacy/)
- [使用条款](https://bettermac.net/en/terms/)

## 系统要求

- macOS 15.0（Sequoia）或更高版本
- 通用二进制 — 同时支持 Apple 芯片与 Intel

## 许可说明

Better Monitor 及本仓库中的原创材料均为专有内容，并非开源软件。版权所有。未经 BetterMacNet 事先书面许可，不授予复制、修改、分发或使用这些内容的任何许可。
