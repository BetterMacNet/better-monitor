# Release Notes

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
