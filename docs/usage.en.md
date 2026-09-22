# Better Monitor Usage Guide

## Install and launch

Better Monitor 1.0.0 is signed with a Developer ID certificate, notarized by Apple, and available through Homebrew Cask.

Install with Homebrew:

```bash
brew install --cask bettermacnet/tap/better-monitor
```

You can also download the [latest release](https://github.com/BetterMacNet/better-monitor/releases/latest), move `Better Monitor.app` to the Applications folder, and launch it. The notarization ticket is stapled to the disk image, so the first launch does not require a network connection.

After launch, choose a page from the navigation sidebar.

## Where to start

- To check system status: open **Monitoring overview**.
- To find a CPU- or memory-heavy app: open **Process monitor**.
- To check whether a process is communicating over the network: open **Network activity** or its process details.
- To see what is listening locally: open **Ports and services**.
- To review background startup activity: open **Startup items**.

## Inspect processes

In **Process monitor**:

1. Sort by CPU, memory, or another available metric.
2. Select a process to view its details.
3. Confirm its name, path, and identity before taking action.
4. Save relevant work before ending a process; unsaved data may be lost.

macOS may prevent actions on system processes or processes owned by another user.

## Inspect ports

In **Ports and services**:

1. Review the listening-port list.
2. Use filters to focus on external-bind warnings, risk signals, or recent changes.
3. Select a service to inspect its port, process, and signing details.
4. Confirm the service's purpose before ending its owning process.

A risk signal does not prove external reachability. Treat it as a prompt for further review.

## Review network activity

The network page shows current interfaces and connection information. If the Wi-Fi name is unavailable:

1. Open **System Settings**.
2. Go to **Privacy & Security → Location Services**.
3. Allow Better Monitor to use Location Services.
4. Return to the app and check the network page again.

Better Monitor uses this permission only to read the Wi-Fi name provided by macOS. It does not record or upload your location.

## Manage startup items

In **Startup items**, review each entry's details and current resource impact before disabling it. The impact reflects current runtime observations; it does not represent boot time or guarantee a specific improvement after disabling an item.

Modern login items managed by macOS remain read-only in the app. Use the provided link to review them in System Settings.

## Use AI diagnostics

AI assistance is optional:

1. Open **Settings** and configure an AI provider.
2. Save the API key when prompted; it is stored in the macOS Keychain.
3. Read and confirm the data-disclosure notice.
4. Request a diagnostic summary from process details.

A request may include process, network, and file-activity summaries needed for diagnosis. Confirm that the provider and its data handling meet your requirements before enabling the feature.

## Privacy and data

Better Monitor keeps monitoring data on your Mac by default. Network access for AI diagnostics occurs only after you configure a provider and request a summary. See the [Privacy Policy](https://bettermac.net/en/privacy/) for more information.
