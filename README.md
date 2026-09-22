# Better Monitor

English · [简体中文](README.zh-CN.md)

<img src="assets/logo.png" alt="Better Monitor" width="160">

A focused macOS system monitor for understanding what your Mac is doing right now.

Better Monitor brings process, network, port, and startup-item information into one native macOS app, with a clear overview for everyday diagnosis and a detailed view when you need to investigate further.

## Highlights

- **Monitoring overview** — See the health of CPU, memory, disk, network, battery, sensors, and running processes at a glance.
- **Process monitor** — Inspect resource usage and process details, with actions for processes you control.
- **Network activity** — Review active connections, traffic, interfaces, protocols, and destinations.
- **Ports and services** — Find listening ports, identify their owning processes, and surface useful risk signals.
- **Startup items** — Review startup entries, current resource impact, and the items that can be managed from the app.
- **Optional AI assistance** — Configure your own provider and use AI-powered process diagnostics when enabled.
- **Native macOS experience** — Built for macOS 15 or later, with a native SwiftUI interface.

## Requirements

- macOS 15.0 (Sequoia) or later
- Universal binary — Apple silicon and Intel

## Install

With [Homebrew](https://brew.sh):

```bash
brew install --cask bettermacnet/tap/better-monitor
```

Or download the disk image from the [latest release](https://github.com/BetterMacNet/better-monitor/releases/latest).

Every release is signed with a Developer ID certificate and notarized by Apple. The notarization ticket is stapled to the disk image, so the first launch works without a network connection.

## Permissions

Some information depends on macOS privacy permissions:

- Location permission is needed to show the current Wi-Fi network name on the Network Activity page.
- Process and port details may be limited by macOS when the system does not expose them to the app.
- Better Monitor does not need your location for location services; macOS requires this permission to provide the Wi-Fi name.

## Documentation

- [Features](docs/features.en.md)
- [Usage guide](docs/usage.en.md)
- [Release notes](docs/release-notes.en.md)
- [User rules](RULES.md)
- [Website](https://bettermac.net/)

## License

Better Monitor and the original materials in this repository are proprietary and not open source. All rights reserved. No license is granted to copy, modify, distribute, or use them without prior written permission from BetterMacNet.

## Support

- [Support center](https://bettermac.net/en/support/?product=better-monitor)
- [Contact us](https://bettermac.net/en/contact/?product=better-monitor)
- [Terms of Use](https://bettermac.net/en/terms/)
- [Privacy Policy](https://bettermac.net/en/privacy/)

---
