# Better Monitor User Rules

Better Monitor 的用户反馈规则。它们把 BetterMac 用户社区中反复出现、且能转化为产品行为的痛点，沉淀为公开的产品约束；不是运行时配置，也不是安全软件规则库。

> 这些规则来自 `better_monitor-bak/docs/deep-research-user-pain-points-report.md`（2026-08-25）及其中引用的公开社区讨论。公开仓库不包含工单中的姓名、邮箱、设备信息或未脱敏原文。

## Rules

### R-001 — 先证据，后解释

任何健康结论、异常摘要或诊断建议必须先列出可观测事实，再给出可能解释、置信度和下一步。每个结论都应能回到时间窗口、主体、数据来源和证据质量。

### R-002 — 未知不等于正常

缺失、过期、权限不足或不支持的数据必须显示为 `unknown`、`partial`、`stale` 或 `unsupported`，不能渲染成 0、正常或确定原因。证据不足时明确写“当前证据不足以归因”。

### R-003 — 问题发生后仍可回看

监控不应只保留当前快照。可观测的尖峰、卡顿、睡眠/唤醒和电池变化应保留前后上下文；进程退出后仍保留其历史实例和最后一次可靠观测。

### R-004 — 按应用归因，同时保留进程身份

用户通常关心一个 App 或工作负载的总成本，而不是孤立 PID。展示层可以聚合 App、Helper、Renderer、XPC 和子进程，但底层必须保留 `bootSession + PID + startTime`，避免 PID 重用覆盖历史。

### R-005 — 指标必须可解释

`%CPU`、相对能耗和网络速率不能脱离口径展示：

- CPU 需要区分逻辑核心等效值与整机占比。
- 相对 Energy Impact 不能伪装成电池百分比或精确 Wh。
- 事实、估算、残余和置信度必须分开标示。

### R-006 — 监控器不能成为负担

采样频率、监控器自身 CPU、内存、唤醒和写入开销应可见。电池、低电量或高温状态下应降低高成本采集；核心监控不能依赖高开销私有接口。

### R-007 — 本地优先，隐私透明

默认不要求账号，不上传原始进程数据，不依赖云端才能完成核心监控。启用 AI 或导出诊断资料前，必须说明会发送或保存哪些进程、网络、路径和文件活动摘要。

### R-008 — 能力边界必须显式

Direct、权限受限和不可用能力不能被 UI 隐藏。进程网络、GPU、系统磁盘、崩溃原因或睡眠唤醒原因没有可靠来源时，显示覆盖范围和限制，不用推测补齐。

### R-009 — 破坏性动作默认不自动执行

结束进程、停用启动项或修改系统设置必须由用户明确触发，并进行身份、权限和目标复核。诊断摘要和 AI 文本不得自动生成 `kill`、`sudo`、shell、删除文件或修改系统的执行指令。

### R-010 — 端口风险不是外部可达性证明

非本机绑定只能作为需要核对的风险信号。除非另有可靠探测证据，不得宣称端口已经被外部访问、暴露或完成安全审计；界面应明确“外部可达性未验证”。

### R-011 — 启动项描述必须符合 macOS 能力

应用列出可读取的 LaunchAgent 和 LaunchDaemon，并为 macOS 管理的现代登录项提供系统设置入口。现代登录项不被完整枚举时，不得宣传为已在应用内列出全部登录项。

### R-012 — 启动项影响只表示当前观测

启动项页面的影响指标来自当前运行状态，不代表开机耗时、启动延迟或禁用后的确定收益。所有无法由 macOS 公开数据证明的收益预估都应省略。

## Evidence sources

- [Process CPU history — Ask Different](https://apple.stackexchange.com/questions/299281/how-to-check-processes-cpu-usage-history-in-macos)
- [Sleep energy attribution — Ask Different](https://apple.stackexchange.com/questions/472283/detecting-which-process-program-is-running-and-consuming-energy-while-mac-is-sle)
- [High CPU usage after Tahoe — Apple Community](https://discussions.apple.com/thread/256271160)
- [Performance history — Reddit](https://www.reddit.com/r/WebSoftGiveaway/comments/1uo7kzc/macos_keeps_no_performance_history_so_i_couldnt/)
- [Battery drain during sleep — V2EX](https://www.v2ex.com/t/1141072)
- [Monitor overhead — V2EX](https://v2ex.com/t/1215344)
- [Per-app network visibility — V2EX](https://cn.v2ex.com/t/1227537)
- [Grouped process monitoring — MacRumors](https://forums.macrumors.com/threads/are-there-alternatives-to-activity-monitor-with-a-standalone-app-not-menu-bar-only-shows-stats-for-individual-apps-and-groups-processes-by-app.2376159/)
- [Local history and no telemetry — Reddit](https://www.reddit.com/r/MacOSApps/comments/1vx31y6/i_made_a_free_open_source_performance_monitor_for/)

## Repository contribution rules

- Git commits use the BetterMacNet GitHub account: `BetterMacNet` (`github@bettermac.net`).
