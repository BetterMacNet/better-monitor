# Better Monitor Features

Better Monitor 1.0.0 is a native macOS system monitor for everyday observation and focused troubleshooting. It brings the information you need into one window instead of sending you between multiple system tools.

## Monitoring overview

The overview page provides a quick view of:

- CPU usage and core status
- Memory usage
- Disk and network activity
- Battery and sensor information
- Running processes
- System health and items that need attention

## Process monitor

Use the process page to investigate high resource usage and unusual activity:

- Sort running processes by available resource metrics
- Inspect process identity, path, and resource details
- Review network activity and open files for a process
- End processes only when you have permission and have confirmed the target
- Request an optional AI-assisted diagnostic summary for supported processes

## Network activity

The network activity page combines connection state and traffic information:

- Current network interfaces and connection state
- Upload, download, and throughput trends
- Active connections, protocols, and TCP states
- Destination addresses and connection counts
- Current Wi-Fi name, when macOS Location Services permission is available

## Ports and services

Use the ports page to understand what is listening on the Mac:

- Listening ports and transport protocols
- Service names and owning processes
- Bind scope and external-reachability warning signals
- Process signing status
- Port changes and risk filters

A non-local bind is a signal to investigate, not proof that a service is externally reachable or has been security-audited.

## Startup items

The startup-items page helps you review background startup activity:

- Readable LaunchAgents and LaunchDaemons
- Modern login items that macOS manages through System Settings
- Current resource impact and running state
- Enable or disable entries supported by the app

The impact shown is based on current observations; it is not a measurement of boot time or a guaranteed saving after disabling an item.

## Local history and privacy

Monitoring history is stored locally by default. Core monitoring does not require an account or cloud service. Data is sent to an external AI provider only when you configure one and explicitly request a diagnostic summary.

## Optional AI assistance

AI is not required to use Better Monitor. When enabled, you can configure your own provider to help interpret process resource, network, and file activity.

- API keys are stored in the macOS Keychain
- A data-disclosure notice is shown before sending diagnostic information
- AI output is diagnostic assistance, not a substitute for your judgment
