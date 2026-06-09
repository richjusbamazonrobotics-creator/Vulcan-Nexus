# Vulcan Nexus

**GEG1 Workstation Hub** — A centralized launcher and resource management tool for the Vulcan Engineering team.

## Overview

Vulcan Nexus is a Python-based GUI application that provides one-click access to all daily tools, video streams, documents, bookmarks, and scripts used by the Vulcan Engineering team. It features role-based access control, cloud-synced configuration, and automatic updates.

## Features

- **Home Dashboard** — Two-column layout with shift passdown (left) and shift calendar (right), team announcement banner, Full Stack launch, and quick links
- **Applications** — Launch Cisco Secure Client VPN, Slack, Outlook, and Better MMA
- **Bookmarks** — Team-wide web tools and dashboards
- **Documents** — Monthly docs (Downtime Log, End of Day Report, Daily Sync) and role-gated reference documents
- **Kinesis Streams** — Live video streams for all 6 GEG1 systems (18 cameras)
- **Scripts** — Workshell and automation utilities
- **Settings** — Customizable quick links, Full Stack items, and themes — accessed via the ⚙ gear icon in the sidebar footer
- **Team Roster** — Online-first alphabetical list with active status indicators and full shift names
- **Training & SOPs** — Amazon Learn, Global Robotics University, and standard operating procedures
- **Admin Panel** — Manage all URLs, users, and role permissions (Admin and Owner only)
- **Owner Panel** — Announcement banner, role permission matrix, and cloud sync controls (Owner only)

## Role Hierarchy

| Role | Home | Apps | Kinesis | Docs | Links | Training | Scripts | Roster | Settings | Admin | Owner Panel |
|------|:----:|:----:|:-------:|:----:|:-----:|:--------:|:-------:|:------:|:--------:|:-----:|:-----------:|
| Owner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Administrator | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — |
| Tech Lead | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — |
| Operations Lead | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — |
| Field Engineer | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — | — |
| Vulcan Floor Monitor | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | ✓ | — | — |
| Inductor | ✓ | ✓ | — | ✓ | ✓ | ✓ | — | — | ✓ | — | — |

> **Note:** The Owner account (`richjusb`) is permanently protected in the application code.
> It cannot be demoted, edited, or deleted through the GUI or by editing config.json.

## Tech Stack

- Python 3.12
- CustomTkinter (GUI framework)
- PyInstaller (packaging)
- GitHub API (config sync + auto-update)

## Development Setup

1. Clone this repository:
   ```
   git clone https://github.com/richjusbamazonrobotics-creator/geg1-vfe-config
   cd geg1-vfe-config
   ```

2. Create and activate a virtual environment:
   ```
   py -3.12 -m venv .venv
   .venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Add your GitHub token for config sync (create `secrets.json`):
   ```json
   { "github_token": "github_pat_YOUR_TOKEN_HERE" }
   ```

5. Run locally:
   ```
   python launcher.py
   ```

6. Build the `.exe`:
   ```
   build.bat
   ```

## Project Structure

```
Vulcan Nexus/
├── .venv/                  # Python virtual environment (not committed)
├── build/                  # PyInstaller intermediate files (not committed)
├── dist/                   # Built .exe output (not committed)
├── release/                # Final release package (not committed)
├── build.bat               # Build and package script
├── config.json             # Local config cache (auto-synced from GitHub)
├── icon.ico                # Application icon
├── launcher.py             # Main application source
├── preferences.json        # User preferences (local only)
├── README.md               # This file
├── README.txt              # End-user instructions (ships with release)
├── requirements.txt        # Python dependencies
├── secrets.json            # GitHub token — DO NOT COMMIT OR SHARE
└── VulcanNexus.bat         # Dev quick-launcher (runs dist\Vulcan Nexus.exe)
```

## Configuration

- Config is fetched from GitHub on every launch (with cache-busting)
- Admin panel changes push automatically to GitHub via the API
- All other team members receive updates on their next app launch
- Config repo: `github.com/richjusbamazonrobotics-creator/geg1-vfe-config`

## Distribution

1. Run `build.bat`
2. Zip the `release/` folder
3. Go to GitHub → Releases → Draft new release
4. Tag the release (e.g. `v3.6.0`) and attach the zip as a release asset
5. The app will detect the new release tag and prompt users to update on next launch

## Security Notes

- `secrets.json` contains your GitHub PAT and **must never be committed or distributed**
- It is intentionally excluded from the release package by `build.bat`
- The Owner account is hardcoded in `launcher.py` and cannot be altered at runtime

## Author

Justin Richards — Vulcan Engineering, GEG1
