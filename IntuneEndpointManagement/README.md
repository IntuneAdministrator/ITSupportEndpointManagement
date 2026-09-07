# Intune Endpoint Management

A practical engineering toolkit for Microsoft Intune administrators and endpoint management professionals. It brings together PowerShell automation, proactive remediations, security baselines, Win32 packaging, Dell hardware management, macOS configuration, and Microsoft 365 administration resources.

The collection is designed to provide reusable starting points for real-world endpoint operations. Review each script, adapt it to your environment, validate it in a lab, and deploy through a controlled pilot group before broad assignment.

**Maintainer:** [Allester Padovani](https://www.linkedin.com/in/allester-padovani/)  
**GitHub:** [IntuneAdministrator](https://github.com/IntuneAdministrator)  
**Technical writing:** [Endpoint Tech Blog](https://endpointtechblog.com/)

---

## Table of contents

- [What this repo includes](#what-this-repo-includes)
- [Repository layout](#repository-layout)
- [Prerequisites](#prerequisites)
- [How to use these scripts](#how-to-use-these-scripts)
- [Module details](#module-details)
  - [Intune Endpoint Management](#intune-endpoint-management)
  - [Windows 11 detection and remediation](#windows-11-detection-and-remediation)
  - [Security baselines](#security-baselines)
  - [macOS management scripts](#macos-management-scripts)
  - [Dell tools install and uninstall](#dell-tools-install-and-uninstall)
  - [Dell detection and remediation](#dell-detection-and-remediation)
  - [Win32 packaging tool](#win32-packaging-tool)
  - [ServiceUI for Win32 app installs](#serviceui-for-win32-app-installs)
- [Safety notes](#safety-notes)
- [License](#license)
- [Connect](#connect)

---

## What this repo includes

| Area | What you get |
| --- | --- |
| Microsoft 365 / Entra | License reports, MFA status, Conditional Access export, guest users, offboarding, inactive users |
| Intune admin tools | Intune Management console, device troubleshooter, Company Portal tray tool, IntuneWin downloader |
| Windows 11 | Detect / remediate scripts for compliance, configuration, Defender, performance, reporting, and toast notifications |
| Security baselines | Importable policies for Windows 11, Windows 365, macOS, and mobile BYOD |
| macOS | Config scripts, custom attributes, configuration profiles, apps, and admin tools |
| Dell hardware | Win32 install / uninstall / detection scripts plus BIOS, warranty, and driver remediations |
| App packaging | Microsoft Win32 Content Prep Tool (`.intunewin`) and ServiceUI helpers |

---

## Repository layout

```text
Intune Endpoint Management/
Intune Windows 11 Detection & Remediation/
Intune Security Baseline/
Intune macOS Management Scripts/
Intune Windows Dell Tools Install & Uninstall/
Intune Windows Dell Detection & Remediation/
Intune Win32 Packaging Tool/
Intune Windows App Install ServiceUI/
```

---

## Prerequisites

- A Microsoft Intune licensed tenant and an account with enough permissions to create policies, apps, and remediations
- Windows PowerShell 5.1 or PowerShell 7 for most Windows scripts
- [Microsoft Graph PowerShell](https://learn.microsoft.com/powershell/microsoftgraph/installation) for Microsoft 365 / Entra reporting scripts
- .NET Framework 4.7.2 for the Win32 Content Prep Tool
- Dell Command | Configure, Dell Command | Update, and related Dell tools for Dell-specific remediations
- Test devices (or Autopilot / Windows 365 lab VMs) before you assign anything broadly

---

## How to use these scripts

### Proactive remediations (detect / remediate)

Most Windows 11 and Dell folders follow the Intune remediations pattern:

1. Open **Intune admin center** > **Devices** > **Remediations**.
2. Create a script package.
3. Paste the `Detect_*.ps1` script as detection and `Remediate_*.ps1` as remediation.
4. Detection should **exit 0** when the device is healthy and **exit 1** when remediation should run.
5. Assign to a pilot group first, then expand.

### Win32 apps

1. Put the installer and the matching install / uninstall / detection scripts in one folder.
2. Package with the Win32 Content Prep Tool into an `.intunewin` file.
3. Upload the package in **Intune** > **Apps** > **Windows**.
4. Use the detection script as the detection rule.

### Security baselines

Import the JSON files with the Intune Management tool in this repo, or use native Intune import where the folder is named `NativeImport`. Review every setting against your environment before assignment.

### Microsoft Graph reports

Run the reporting scripts from an elevated PowerShell session. Sign in when prompted (interactive, or certificate-based auth where the script supports it). CSV output is written to the current directory.

---

## Module details

### Intune Endpoint Management

Admin and Microsoft 365 operations scripts, organized by platform:

| Platform | Workloads |
| --- | --- |
| `01 - Entra ID` | Conditional Access, identity/access reports, Entra devices |
| `02 - Microsoft 365` | User lifecycle (offboarding / inactive users) and licensing |
| `03 - Intune` | Management console, device troubleshooter, Company Portal tray, IntuneWin downloader |

### Windows 11 detection and remediation

Proactive remediations grouped by job:

- **Device compliance** — BitLocker, Credential Guard, Device Guard, firewall, Secure Boot, custom file / registry checks
- **Device configuration** — UAC, WDAC, time zone, certificates, VPN, wallpaper, drive mapping, Office / Outlook templates, DNS
- **Microsoft Defender Antivirus** — real-time protection, cloud-delivered protection, network protection, PUA, tamper protection, scans, and intelligence updates
- **Device performance** — disk cleanup, low disk space, user profiles, system performance, inactive local / Entra users
- **Reporting** — uptime, software inventory, BitLocker, certificates, firewall, local admins, pending reboot, event log errors
- **Toast notifications** — reboot required, pending updates, low disk, high CPU / memory, printer issues, network, battery, antivirus
- **Miscellaneous** — Windows AI registry, SoftwareDistribution folder, generic registry and service restarts
- **ToastCreator** — helper for building toast notifications

### Security baselines

Opinionated Intune baselines (often labeled **OIB**) ready to import:

| Platform | Contents |
| --- | --- |
| Windows 11 | Compliance, Settings Catalog, update rings, driver updates, health monitoring, helper scripts |
| Windows 365 | Cloud PC device security, connectivity, and resource redirection |
| macOS | FileVault, Gatekeeper, Defender, Edge, Office, OneDrive, Platform SSO, updates |
| Mobile (BYOD) | iOS and Android app protection policies |

### macOS management scripts

| Folder | Purpose |
| --- | --- |
| `Config` | Hardening and setup: sharing services, FileVault / bootstrap token, Defender, firewall, Gatekeeper, Dock, wallpaper, Rosetta 2, NTP, and more |
| `Custom Profiles` | `.mobileconfig` payloads for Edge, Office, OneDrive, Terminal, notifications, software update, Wi-Fi, and third-party apps |
| `Custom Attributes` | Inventory scripts (battery, CPU, Defender, Edge, .NET, compatibility) |
| `Apps` | App deployment helpers |
| `Tools` | PSSOForge, enrollment profile groups, MDM check-in monitor, Intune agent logs, network checker, bundle ID helper, migration samples |

### Dell tools install and uninstall

Win32-ready install, uninstall, and detection scripts for Dell management software:

- Dell Command \| Update, Configure, Monitor, and Endpoint Configure for Microsoft Intune
- Dell Display Manager / Display and Peripheral Manager
- Dell Optimizer, Power Manager, Peripheral Manager, Trusted Device
- Dell SupportAssist for Business
- Microsoft .NET Desktop Runtime 8 and ASP.NET Core 8 (common Dell dependencies)

`Universal App Scripts` can install or update several Dell tools from one package when the installer files sit next to the script.

### Dell detection and remediation

Custom compliance sensors and remediations for Dell PCs:

- BIOS admin password, Fastboot, thermal mode, and other BIOS settings
- SafeBIOS / indicators of attack
- Dell Command \| Update critical drivers
- Warranty / out-of-warranty status
- Battery health and chassis intrusion
- Display ComfortView and related settings

Review any script named `do_not_use` before you assign it. Those are marked as not ready for production.

### Win32 packaging tool

Microsoft Win32 Content Prep Tool. It converts a setup folder into an `.intunewin` package for Intune Win32 apps.

```powershell
IntuneWinAppUtil -c <setup_folder> -s <setup.exe_or.msi> -o <output_folder> -q
```

Run `IntuneWinAppUtil -h` for full usage. Keep generated `.intunewin` files as secure as the original installers; they contain encrypted source files.

### ServiceUI for Win32 app installs

ServiceUI helpers for Win32 apps that need to interact with the logged-on user (for example, a visible installer or prompt) while Intune runs the package in the system context. x64 and x86 originals are included.

---

## Safety notes

- Run every script in a test ring before production. BIOS, compliance, and uninstall scripts can break devices if settings do not match your hardware or tenant.
- Some Microsoft Graph scripts need high-privilege directory permissions. Use least privilege and an app registration with certificate auth when you schedule them.
- Dell BIOS remediations may require a BIOS administrator password and Dell Command \| Configure. Confirm the password handling in each script before you deploy.
- This collection includes tools and samples from Microsoft, Dell, and the Intune community. Read the header comments and any `LICENSE` or `README` in a subfolder before you redistribute.
- Never commit tenant exports, access tokens, certificates, application secrets, device identifiers, or customer data.

---

## License

This project is licensed under the [MIT License](./LICENSE) (Copyright (c) 2026 Allester Padovani).

This repository is a curated collection. Some nested tools may also ship their own license files (for example MIT, Apache 2.0, or Microsoft software terms). Honor those terms for those packages.

The software is provided as-is, without warranty. You are responsible for testing and for any change you make in your tenant.

---

## Connect

- LinkedIn: [Allester Padovani](https://www.linkedin.com/in/allester-padovani/)
- GitHub: [IntuneAdministrator](https://github.com/IntuneAdministrator)
- Technical articles: [Endpoint Tech Blog](https://endpointtechblog.com/)
