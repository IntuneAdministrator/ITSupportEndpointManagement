# Intune Endpoint Management

Microsoft 365 endpoint tools organized by **platform**, then by **workload area**, then by tool.

This tree only contains what is in the folder today. There are **no** standalone Exchange Online, Teams, SharePoint, or OneDrive-only packages here. Licensing cost tools may *call* Exchange Online PowerShell as a dependency, but they live under **Microsoft 365 → Licensing**.

## Platforms

| Platform | Focus |
|----------|--------|
| [01 - Entra ID](./01%20-%20Entra%20ID) | Conditional Access, identity/access reports, Entra devices |
| [02 - Microsoft 365](./02%20-%20Microsoft%20365) | User lifecycle (offboarding / inactive users) and licensing |
| [03 - Intune](./03%20-%20Intune) | Admin console, device troubleshooter, Company Portal tray, Win32 packaging |

## Structure

```text
01 - Entra ID
  01 - Conditional Access
  02 - Identity and Access
  03 - Devices
02 - Microsoft 365
  01 - User Lifecycle
  02 - Licensing
03 - Intune
  01 - Management Console
  02 - Device Troubleshooter
  03 - Company Portal
  04 - Win32 Packaging
```

## How to use

1. Pick the **platform** (Entra ID, Microsoft 365, or Intune).
2. Open the **workload** subfolder.
3. Open the tool and run / package the entry script or app.
4. Pilot any write, delete, offboarding, or license-change action first.

## Requirements

- Microsoft 365 tenant with the matching workload enabled
- PowerShell 5.1+ (PowerShell 7 where a tool requires it)
- Graph / Entra / Intune / Exchange modules as required by each script

## License

This project is licensed under the [MIT License](./LICENSE).

Upstream tools may ship their own license files; honor those for those packages.

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
