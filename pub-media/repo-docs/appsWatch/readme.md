# AppsWatch

<img src="https://raw.githubusercontent.com/vrw-GH/vrw-GH/main/pub-media/repo-docs/appsWatch/Screenshot.png" alt="screenshot" width="47%"><img src="https://raw.githubusercontent.com/vrw-GH/vrw-GH/main/pub-media/repo-docs/appsWatch/Screenshot2.png" alt="screenshot" width="47%">

Another Project by **Victor Wright** @ [WrightsDesk](https://www.wrightsdesk.com/apps/index.php "WD Apps List")

[Direct DOWNLOAD here](https://www.wrightsdesk.com/apps/downloads/apps_watch-1.1.5.exe "Ver 1.1.5 - Evaluatiion")

## Concept

> Goal:

- Regularly monitor for security news related to installed applications on a Windows PC..

> Core Features:

- Detect/list installed applications.
- Search news/security sites for vulnerabilities or issues per app.
- Monitoring the news sources at intervals.
- Notify via popup when new issues found.
- Check only selected apps
- Delete old-logs
- Features of licensed Vs. evaluation

> Framework:

- UI: Electron (HTML/CSS/JS)
- Logic: Node.js
- Registry Access: winreg
- Scraping: axios, cheerio
- Notifications: node-notifier
- Storage: JSON/local file DB

### Updates history

<details open>
<summary>Ver: 1.1.4</summary>

- main: reword "Unregistered" as "Evaluation"
- **Licensing: Adverts - leftPanel: Full/half/banners?
- registerer: allowed! // if real MID!=userdata.MID, its not same PC!
- monitorApps: too many reads
- monitorApps: [NVD] handle unlicenced version/delayed running
- **Licensing: limit monitor qty
- **Licensing: check limits "onload" too (direct settings edit)
- **Licensing: limit monitor frequency
- appsList: show title of apps also over tickbutton
- **Licensing: sources allowed only 1
- updateDetectedApps: show wait-cursor
- **Licensing: limit toggle detected apps
- **Licensing: limit folders
- **Licensing: limit toggle custom apps
- **Licensing: limit total "selected apps"
- Second-instance: mainWindow.focused but not interactable

</details>
<details>
<summary>Ver: 1.1.3</summary>

- Save REG in conf
- if RefKey.exp and not regKey - must regenerate refKey
- registrtation: clear form - re-confirm!!!
- Conf: save Licence tied to user-registration
- if Registration ok, remove reference and other..
- Validate licence *isReg()*
- confirmRegUser: verify uID,uEm,app,MID
- confirmRegUser: verify validity
- Registration: when create-reference not confirmed, inputs become inactive
- LicForm: reset button action
- LicForm: reset button remove CONF data
- Startup: AppPath not C:\windows\system
- Added the PayPal Donate link
- add NVD-api "attribution"
- Show link to NVD site in NVD API input
- Second-instance to restore/focus main window
- Registration: send email button - via email app
- main: save registration info to CONFIG
- moved utils,cryption and register modules to WDutilsLibrary
- autologon: check CONF creation
- Main: LICENcE file in C:\windows\system!!!
- develop JWT creation on registration
- Develop UI for registration
- Licence T&C - LICENCE : Proprietary Software - free basic, paid Pro(1-year?)
- build: include LICENcE file
- About: remove extra CRLF

</details>
<details>
<summary>Ver: 1.1.2</summary>

- !Autostart: app run folder = C:\Windows\System32?! / (also conf/settings folder)
- Main Window: Title, Footer and Sources sometimes not redrawing (false event?)
- Release: putSettings (even if not specifically saved)
- Conf: save CONF info tied to system
- Main: API key input field set focus
- Main: SRC1 disable(only licenced version ?)
- API-KEY: Double check if entry is correct, or Update method! (dialog?)
- MainWindow: html/body background image / Logo at Heading
- Main: show current PORTAL(x,y) in about/sys-info(DEV) ?
- Main: set min PORTAL width,height
- APPDATA: TODOs line conjoining!!
- Settings: (file-creation EPERM error)-false process.env folder when autorun
- Settings-Error Settings:  Unexpected end of JSON input (expected behaviour)
- Create initial empty settings/conf files
- Release: settings dont save on first run
- input(get) API Key or error
- check - Hex conf info (ie: SRC2 key)
- use conf for user entered data (ie SRC2 key)
- Assets: redesign App Logo/Icon
- Alerts: today items design
- Release: ScanResults - blank () in itemtitle?
- Main: tray disabling not happening for 1st monitoring at startup
- Release: Tray disabling duing 3m wait - show monitoring animation
- Release: check if console clear works - viewarea only
- Settings: input validate for Freqency (<>0)
- Release/about: Show TODO:(ver history)
- Alerts: order of newest
- Release: Uninstall does not remove REG-autostart
- Main: Hidden = "minimize" to tray, because close to tray is always active
- Hex conf info (ie: SRC2 key)
- alertlog: show items only by days (not 24hrs)
- main: add verX in footer (DEV)
- about: hide "updated" items
- Release: hide to tray on "minimize" too
- Release: Autostart: - creates REGentry but wrong folder (1-up)
- Settings: "Autostart/close to Tray" functionality, savebutton update
- Settings: enable errorcheck on frequency-input max
- main: if "closing" to tray, show notification (first time only)
- build: installer - better banner image
- mainwindow: show *flashing* "Monitoring now..."
- .btnPop iteration to 3 //? check bkgPop
- Release: data-init folder (for initial sample data)
- Release: init display "---" for lastscan date
- promise issues:
   test212: EXCLUDED_FOLDERS //? test45
   test232: TIMEOUT //? test88
- settings: All "Settings" get overwrtitten(?) not only changes
- getInstalledApps: check sort(a.name b.name)
- getSetting: //* get a current/refreshed value!!

</details>
<details>
<summary>Ver: 1.1.1</summary>

- Toggle Monitor-button visibility (as reminder) on any changes to selected apps
- Add other search Clients
- NVD by user API-license
- Auto-start on windows login
- Better log view, link as title
- Tasktray: added re-scan system apps
- alertLog: CSS for headertext one line only ("adobe" 07.11.2025 too long)
- alertLog: after monitoring - update of log display
- AlertLog: here we should get "all" and filtered!!
- alertLog: show number of articles (under filter?)
- Build options: appID, signTool, licencePFX
- notifier: add appID productName
- Sources: add/remove - standard: SRC2/SRC1/SRC0(DDG)

</details>
<details>
<summary>Ver: 1.0.0</summary>

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

</details>
