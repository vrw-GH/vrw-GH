# AppsWatch

[<img src="https://raw.githubusercontent.com/vrw-GH/assets/main/repo-media/appsWatch/Screenshot.png" alt="screenshot" width="95%">](http:# "await link..")
[<img src="https://raw.githubusercontent.com/vrw-GH/vrw-GH/main/pub-media/repo-docs/appsWatch/Screenshot.png" alt="screenshot" width="95%">](http:# "await link..")

Another Project by **Victor Wright** @ [WrightsDesk](https://www.wrightsdesk.com)

## Concept

> Goal:

- Monitor security news related to installed applications on a Windows machine.

> Core Features:

- Detect/list installed applications.
- Search news/security sites for vulnerabilities or issues per app.
- Monitor these sources at intervals.
- Notify the user via popup when new issues appear.

> Framework:

- UI: Electron (HTML/CSS/JS)
- Logic: Node.js
- Registry Access: winreg
- Scraping: axios, cheerio, puppeteer?
- Notifications: node-notifier
- Storage: JSON/local file DB

## TODO / Feature Requests

- App Ignore List (use PC Apps list, strikeout)
- searchDDG: get article published date
- Open single instance only
- Delete old-logs / cleanup (120days)
- Features of licensed Vs. unlicensed

### Features / Version info

> Ver: 1.1.1 (Dev)

- Toggle Monitor-button visibility (as reminder) on any changes to selected apps
- Add other search Clients
- NVD by user API-license
- Auto-start on windows login
- Better log view, link as title
- Tasktray - added re-scan system apps

> Ver: 1.0.0

- Scan System for installed Apps
- Exclude sysFolders keywords:
  Symlinks,StartsWith"$/.",Windows,Recycle.bin,cache,ProgramData,System Volume Information,WpSystem,Program Files (&x86)? etc.
- Add Folders to scan
- Add Custom Apps / or any "Topic"
- Monitor Clients:
  DuckDuckGo (SRC0) / Default
  National Vulnerability Database (SRC2)
- Monitoring include/exclude keywords:
  vulnerability,CVE-,exploit,zero-day,critical patch,-download,-update etc.
- Security Log filtering by app / days / client
- Log links to relevant website
- Tasktray - Show/hide, Monitor Now and Quit
