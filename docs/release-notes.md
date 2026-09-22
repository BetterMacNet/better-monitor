# Release notes

## 1.0.1 — 2026-09-22

### 修复

- 修复 Release 构建启动数秒后崩溃的问题。
- 修复每个进程的磁盘 I/O 速率显示为空的问题。

## 1.0.0 — 2026-09-22

### 主要内容

- 提供监控概览、进程监控、网络活动、端口与服务、启动项和设置页面
- 集中查看进程资源、网络连接、监听端口和启动项
- 提供可选的 AI 进程诊断能力，API 密钥保存在 macOS 钥匙串中
- 监控历史默认保存在本机

### 安装

使用 Homebrew Cask 安装：

```bash
brew install --cask bettermacnet/tap/better-monitor
```

也可以下载[最新发布](https://github.com/BetterMacNet/better-monitor/releases/latest)。

### 兼容性

- macOS 15.0（Sequoia）或更高版本
- 同时支持 Apple 芯片与 Intel 的通用二进制
- 使用 Developer ID 签名并经 Apple 公证

### 已知限制

- 显示当前 Wi-Fi 名称需要定位服务权限。
- 根据系统可见性和权限，macOS 可能限制进程和端口详情。
- 由 macOS 管理的现代登录项需要通过「系统设置」审查。
- 端口绑定风险提示不代表服务具备外部可达性。
- 启动项影响指标来自当前观测，不代表开机耗时或停用后的确定收益。
- AI 诊断为可选功能，只有在配置服务商并主动请求后才会使用网络访问；请求可能包含进程、网络、路径和文件活动摘要。

### 法律与支持

- [隐私政策](https://bettermac.net/en/privacy/)
- [使用条款](https://bettermac.net/en/terms/)
- [支持中心](https://bettermac.net/en/support/?product=better-monitor)
- [安全问题报告](../SECURITY.md)
