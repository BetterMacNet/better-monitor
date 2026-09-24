# Release notes

## 1.0.3 — 2026-09-24

### 新增

- **AI Monitor**：新页面，位于侧边栏「监控概览」下方。细看 Apple 芯片的 CPU 簇、GPU、神经网络引擎、媒体引擎、统一内存带宽、功耗和传感器；按进程识别 Ollama、LM Studio、MLX、llama.cpp 等本地 AI 运行时，开启「连接本地 AI 运行时」后显示已加载模型、GPU/CPU 分配和 tokens/秒（只访问 127.0.0.1，数据不离开你的 Mac）。页面随浅色 / 深色外观和界面语言切换，只在页面显示时采样。需要 Apple 芯片。
- AI Monitor 中的结束与强制结束沿用「进程监控」的安全校验：受保护的系统进程、其他用户的进程或已被复用的 PID 会被拒绝，并说明原因。

### 修复

- 侧边栏选中项的图标在浅色模式下几乎看不见。

### 致谢

- AI Monitor 基于 [SiliconScope](https://github.com/kennss/SiliconScope)（MIT）；第三方许可声明随 app 附带（`ThirdPartyNotices.txt`）。

## 1.0.2 — 2026-09-23

### 新增

- 界面支持简体中文、English、日本語、한국어。在「设置 → 外观与显示 → 界面语言」切换，即时生效，无需重启；默认跟随系统语言。系统自带菜单和权限弹窗会在下次启动时切换。

### 修复

- 登录项较多时不再误报「登录项不可用」。
- 登录项路径与数据迁移更安全：登录项改为读取 POSIX 路径；迁移数据目录时拒绝符号链接的目录或条目。
- Wi-Fi 信号质量的颜色改为按 RSSI 判断。

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
