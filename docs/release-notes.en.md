# Release Notes

## 1.0.3 — 2026-09-24

### New

- **AI Monitor**: a new page, right below Monitoring Overview in the sidebar. It shows Apple silicon in detail — CPU clusters, GPU, Neural Engine, Media Engine, unified-memory bandwidth, power, and sensors — and detects local AI runtimes such as Ollama, LM Studio, MLX, and llama.cpp from their processes. Turn on "Connect to local AI runtimes" to see the loaded model, GPU/CPU offload, and tokens per second (127.0.0.1 only; nothing leaves your Mac). The page follows the light / dark appearance and interface language, and samples only while it is on screen. Requires Apple silicon.
- Quit and Force Quit in AI Monitor use the same safety checks as Process Monitor: protected system processes, other users' processes, and reused PIDs are refused with the reason.

### Fixes

- The icon of the selected sidebar item was nearly invisible in the light appearance.

### Acknowledgements

- AI Monitor is built on [SiliconScope](https://github.com/kennss/SiliconScope) (MIT); third-party license notices ship inside the app (`ThirdPartyNotices.txt`).

## 1.0.2 — 2026-09-23

### New

- The interface is now available in Simplified Chinese, English, Japanese, and Korean. Switch in Settings → Appearance & Display → Interface language; the change applies immediately without a restart, and the default follows your system language. System menus and permission prompts switch at the next launch.

### Fixes

- "Login items unavailable" is no longer reported when there are many login items.
- Hardened login item paths and data migration: login items are read as POSIX paths, and data migration refuses symlinked directories or entries.
- Wi-Fi signal quality colors are now based on RSSI.

## 1.0.1 — 2026-09-22

### Fixes

- Fixed a Release-build crash a few seconds after launch.
- Fixed per-process disk I/O rates returning empty values.

## 1.0.0 — 2026-09-22

### Highlights

- Monitoring overview, process monitor, network activity, ports and services, startup items, and settings pages
- Centralized views for process resources, network connections, listening ports, and startup items
- Optional AI-assisted process diagnostics, with API keys stored in the macOS Keychain
- Monitoring history stored locally by default

### Installation

Install with Homebrew Cask:

```bash
brew install --cask bettermacnet/tap/better-monitor
```

You can also download the [latest release](https://github.com/BetterMacNet/better-monitor/releases/latest).

### Compatibility

- macOS 15.0 (Sequoia) or later
- Universal binary for Apple silicon and Intel
- Developer ID signed and notarized by Apple

### Known limitations

- Location Services is required to show the current Wi-Fi name.
- macOS may limit process and port details based on system visibility and permissions.
- Modern login items managed by macOS are reviewed through System Settings.
- Port bind warnings do not prove external reachability.
- Startup-item impact reflects current observations, not boot time or guaranteed savings.
- AI diagnostics are optional and use network access only after provider configuration and an explicit request. A request may include process, network, path, and file-activity summaries.

### Legal and support

- [Privacy Policy](https://bettermac.net/en/privacy/)
- [Terms of Use](https://bettermac.net/en/terms/)
- [Support Center](https://bettermac.net/en/support/?product=better-monitor)
- [Security reporting](../SECURITY.md)
