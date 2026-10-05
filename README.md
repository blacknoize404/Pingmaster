# Pingmaster

> **A desktop monitor for hosts and APIs**: it pings a target on a schedule, shows the live latency
> history and warns you the moment it goes down. It lives in the system tray and stays out of the way.
> It runs on Windows and Linux.

> **Documentación en español**: [README.es.md](README.es.md)

<p align="center">
  <img src="docs/images/pingmaster-landing.png" alt="Pingmaster landing view, with the start monitoring and settings buttons" width="32%">
  <img src="docs/images/pingmaster-timeout.png" alt="Pingmaster statistics view, with the response time chart" width="35%">
  <img src="docs/images/pingmaster-settings.png" alt="Pingmaster settings view: host, request type and timings" width="32%">
</p>

## What it does

- **Continuous monitoring.** Choose a host or API endpoint and Pingmaster probes it on a configurable
  schedule — HTTP, HTTPS, ICMP or native ICMP.
- **Latency statistics.** A rolling chart of response times per host, plus the current method and
  response state at a glance.
- **Tray notifications.** Windows balloon notifications and a sound when the host connects or drops,
  so you notice outages without watching the window.
- **Autostart on login**, configurable timeouts, request rate and ping method.
- **It remembers your settings** between runs.

## Download

Get the installer for Windows (`Pingmaster-*-windows-x64-setup.exe`) or the package for your Linux
from the [releases](https://github.com/blacknoize404/Pingmaster/releases):

| Distribution | Package |
|---|---|
| Windows 10/11 (x64) | `Pingmaster-*-windows-x64-setup.exe` (Inno Setup, per-user install) |
| Debian, Ubuntu and derivatives | `pingmaster_*.deb` (`sudo apt install ./pingmaster_*.deb`) |
| Fedora, openSUSE | `pingmaster-*.rpm` (`sudo dnf install ./pingmaster-*.rpm`) |
| Any other | `pingmaster-*.tar.gz`, with an `install.sh` that installs it for your user without administrator rights |

Every package brings its own Java runtime — no Java installation needed.

The application window is in Spanish.

## Source

The packages are built from the private `Pingmaster-src` repository with the same pipeline that ships
[MathUtils Studio](https://github.com/blacknoize404/MathUtils-Studio): Maven → ProGuard → jlink →
jpackage → Inno Setup / deb / rpm. The libraries it uses are public:

- [NetworkUtils](https://github.com/blacknoize404/NetworkUtils) — host latency and network traffic monitoring (Apache-2.0)
- [PersistenceUtils](https://github.com/blacknoize404/PersistenceUtils) — file-based settings (Apache-2.0)

## Licenses

Pingmaster itself is proprietary, free to use — see [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md) for
the third-party components inside the installers.
