# Vulcan Nexus — Configuration

Cloud-synced configuration file for the Vulcan Nexus GEG1 Workstation Hub.

## Purpose

This repository stores the shared `config.json` that all Vulcan Nexus instances pull from on launch. When an admin makes changes through the app's Admin Panel, updates are pushed here automatically.

## How It Works

1. User launches Vulcan Nexus
2. App fetches `config.json` from this repo
3. Local config is updated with the latest version
4. If an admin makes changes, the app pushes the updated config back to this repo

## Files

| File | Purpose |
|------|---------|
| `config.json` | All app configuration (users, URLs, roles, permissions, systems) |
| `README.md` | This file |

## Config Structure

- `version` — Current config version
- `roles` — Role definitions and page permissions
- `users` — All registered users (alias, display name, role, shift)
- `kinesis` — System IDs and stream URL configuration
- `apps` — Desktop application paths and launch settings
- `monthly_docs` — Monthly rotating documents (DT Log, EOD, etc.)
- `documents` — Reference documents
- `bookmarks` — Web tool links and dashboards
- `learning` — Training platform links
- `sops` — Standard operating procedures
- `scripts` — Automation script paths
- `schedule` — Shift schedule and FH/BH alternation
- `settings` — App-wide settings (Chrome path, etc.)
- `themes` — Available color themes

## Important

- **DO NOT** manually edit `config.json` unless necessary
- All changes should be made through the Vulcan Nexus Admin Panel
- Manual edits may be overwritten on next admin push

## Access

This repo is used by the GEG1 Vulcan Engineering team. Contact Justin Richards for access.
