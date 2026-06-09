# Vulcan Nexus

**GEG1 Workstation Hub** — A centralized launcher and resource management tool for the Vulcan Engineering team.

---

## Getting Started

1. Download the latest release zip from the [Releases](../../releases) page
2. Extract the zip to your Desktop — **do not run from inside the zip**
3. Double-click `Vulcan Nexus.exe` to launch
4. The app will automatically detect your Windows login and assign your role

> If you see limited access or missing pages, contact your admin to have your alias added to the roster.

---

## What's Inside

### Home
Your default landing page. Shows the current shift passdown on the left and the shift calendar on the right. If there is an active team announcement it will appear as a banner at the top. Launch Full Stack or jump to your pinned quick links from here.

### Applications
One-click launchers for your daily tools — Cisco Secure Client VPN, Slack, Outlook, and Better MMA.

### Bookmarks
Team-wide web tools and dashboards including the Beta KPI Dashboard, FCResearch, QuickSight Analytics, SIM Ticket Manager, and more.

### Documents
Access monthly docs (Downtime Log, End of Day Report, Daily Sync) and role-gated reference documents. Only documents relevant to your role will be visible.

### Kinesis Streams
Live video streams for all 6 GEG1 systems (18 cameras). Opens directly in your browser.

### Scripts
Automation utilities including the Workshell SSH tunnel environment.

### Training & SOPs
Links to Amazon Learn, Global Robotics University, and all standard operating procedures for GEG1.

### Team Roster
Alphabetical list of all team members with their role, shift, and active status. Online users are shown first.

### Settings
Accessible via the **⚙ gear icon** next to your name in the bottom-left corner. Lets you customize your theme, quick links, and Full Stack items.

### Admin Panel *(Admin and Owner only)*
Manage all bookmarks, documents, SOPs, users, and role permissions. Changes are pushed to the cloud and take effect for all users on their next launch.

### Owner Panel *(Owner only)*
Post team-wide announcements, manage the role permission matrix, and control cloud sync.

---

## Role Access

| Role | Home | Apps | Kinesis | Docs | Links | Training | Scripts | Roster | Settings | Admin | Owner Panel |
|------|:----:|:----:|:-------:|:----:|:-----:|:--------:|:-------:|:------:|:--------:|:-----:|:-----------:|
| Owner | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Administrator | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — |
| Tech Lead | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — |
| Operations Lead | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — |
| Field Engineer | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — | — |
| Vulcan Floor Monitor | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | ✓ | — | — |
| Inductor | ✓ | ✓ | — | ✓ | ✓ | ✓ | — | — | ✓ | — | — |

---

## Requirements

- Windows 10 or 11
- Google Chrome installed at the default location
- Internet connection (for config sync and Kinesis streams)

---

## Troubleshooting

**App won't open**
Make sure you extracted the zip before running. Do not run the `.exe` directly from inside the zip file.

**Wrong permissions or missing from roster**
Contact your admin (@richjusb) to have your Windows alias and role added.

**Links not opening**
Make sure Chrome is installed at the default path and your VPN is connected for internal Amazon links.

**Showing old data**
Close and reopen the app — config is refreshed on every launch.

**App is slow to start**
Normal on first launch while the app fetches config from the cloud. If it takes more than 10 seconds, check your internet connection.

---

## Contact

Justin Richards (@richjusb) — Vulcan Engineering, GEG1
