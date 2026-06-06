```python
```markdown

# GEG1 VFE Workstation Launcher - Configuration

Central configuration file for the GEG1 Vulcan Field Engineering Workstation Launcher.

## Overview

This repository hosts the shared `config.json` that the launcher pulls on startup. Any changes pushed here are automatically reflected for all team members on their next launch.

## What's in config.json

- **User roles** — Maps Windows aliases to roles (Admin, Tech Lead, Field Engineer, VFM, OLE)
- **Monthly documents** — SharePoint URLs for DT Log, EOD Report, and Daily Sync
- **Role permissions** — Defines which pages each role can access

## How Updates Work

1. Admin edits `config.json` (via the app's Admin Panel or directly here)
2. Changes are pushed to this repository
3. Team members receive updates automatically on next app launch

## Roles

| Role | Access Level |
|------|-------------|
| Admin | Full access + Admin Panel |
| Tech Lead | All tools and documents |
| Field Engineer | All tools and documents |
| VFM | Basic apps and bookmarks |
| OLE | Basic apps and bookmarks |

## Maintained By

Justin Richards (@richjusb) — GEG1 Vulcan Field Engineering

