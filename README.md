# Vulcan Nexus

**GEG1 Workstation Hub** — A centralized launcher and resource management tool for the GEG1 Vulcan Field Engineering team.

## Overview

Vulcan Nexus is a Python-based GUI application that provides one-click access to all daily tools, video streams, documents, bookmarks, and scripts used by the VFE team. It features role-based access control, cloud-synced configuration, and automatic updates.

## Features

- **Home Dashboard** — Shift calendar (FH/BH), progress bar, quick links, Full Stack launch
- **Applications** — Launch Cisco VPN, Slack, Outlook, Better MMA
- **Kinesis Streams** — Live video streams for all 6 systems (18 cameras)
- **Documents** — Monthly docs (DT Log, EOD Report, TIM Report, 2-Way Radio Tracker)
- **Bookmarks** — Team-wide web tools and dashboards
- **Training & SOPs** — GRU, Amazon Learn, and standard operating procedures
- **Scripts** — Workshell and automation utilities
- **Team Roster** — Members grouped by shift with active shift highlighting
- **Settings** — Customizable quick links, Full Stack items, themes
- **Admin Panel** — Manage all URLs, users, and role permissions (Owner/Admin only)

## Role Hierarchy

| Role | Access Level |
|------|-------------|
| Owner | Full access to all features |
| Admin | Full access except owner-only actions |
| Tech Lead | All tabs except Admin Panel |
| OLE | Same as Tech Lead |
| Field Engineer | All tabs except Admin Panel |
| VFM | All tabs except Admin Panel |
| Inductor | All tabs except Admin Panel |

## Tech Stack

- Python 3.12
- CustomTkinter (GUI framework)
- PyInstaller (packaging)
- GitHub API (config sync + auto-update)

## Development Setup

1. Clone this repository
2. Create virtual environment:
py -3.12 -m venv .venv .venv\Scripts\activate pip install customtkinter pyinstaller

3. Run locally:
python launcher.py

4. Build .exe:
build.bat


## Project Structure

Vulcan Nexus/ ├── .venv/ # Python virtual environment ├── dist/ # Built .exe output ├── release/ # Zipped release package ├── build.bat # Build script ├── config.json # Local configuration ├── icon.ico # Application icon ├── launcher.py # Main application source ├── README.md # This file ├── requirements.txt # Python dependencies ├── secrets.json # GitHub token (DO NOT SHARE) └── Vulcan Nexus.bat # Quick launcher for dev testing


## Configuration

- Config is synced from GitHub on every launch
- Admin changes push automatically to GitHub via API
- Team members receive updates on their next app launch
- Config repo: github.com/richjusbamazonrobotics-creator/geg1-vfe-config

## Distribution

1. Run `build.bat`
2. Zip the `release/` folder
3. Create a new GitHub Release with the version tag
4. Attach the zip file to the release

## Author

Justin Richards — Vulcan Field Engineering, GEG1
