# GEG1 Vulcan Field Engineering - Workstation Launcher

A professional GUI tool for the VFE team to quickly launch daily applications, Kinesis streams, documents, bookmarks, training resources, and scripts from one interface.

## Quick Start (End Users)

1. Download `GEG1_VFE_Launcher.exe` from your team lead
2. Place it anywhere on your machine (Desktop recommended)
3. Double-click to run
4. Your role and permissions are auto-detected from your Windows login

## Setup (Developer / Admin)

### Prerequisites
- Python 3.10+
- Windows 10/11

### Installation
1. Clone or download this project folder
2. Open a terminal in the project folder
3. Run: python -m venv .venv .venv\Scripts\activate pip install -r requirements.txt

4. Launch: `python launcher.py` or double-click `GEG1_VFE_Launcher.bat`

### Building the .exe
1. Double-click `build.bat`
2. The .exe will be in the `dist/` folder
3. Distribute the .exe to your team

## Configuration

The app pulls `config.json` from GitHub on every launch. To update:
1. Edit config in the Admin Panel (admin role only)
2. Push changes to GitHub (manually or via Save & Push)

### Roles
- **Admin** - Full access including Admin Panel
- **Field Engineer** - All tools except Admin Panel
- **Tech Lead** - All tools except Admin Panel
- **VFM** - Home, Apps, Kinesis, Docs, Bookmarks, Training
- **OLE** - Home, Apps, Docs, Bookmarks, Training

## File Structure
GEG1_VFE_Launcher/ ├── launcher.py - Main application ├── config.json - User/role/doc config (synced from GitHub) ├── secrets.json - GitHub token (NEVER share or push) ├── requirements.txt - Python dependencies ├── README.md - This file ├── build.bat - PyInstaller build script ├── GEG1_VFE_Launcher.bat - Dev launcher └── .venv/ - Virtual environment


## Auto-Update
- Config syncs from GitHub on every launch
- .exe updates check GitHub Releases for new versions

## Support
Contact Justin Richards (@richjusb) for access or issues.
