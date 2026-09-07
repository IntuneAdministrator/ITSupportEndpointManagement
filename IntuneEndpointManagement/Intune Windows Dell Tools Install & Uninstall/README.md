# Intune Windows Dell Tools Install & Uninstall

Win32-style PowerShell scripts to **install**, **uninstall**, and **detect** Dell commercial tools (and required Microsoft runtimes) for Microsoft Intune packaging, organized by category.

Pair each package with the corresponding Dell installer media / `.intunewin` content. Prefer the PDF under `07 - Documentation` for the original deployment walkthrough.

## Categories

| Folder | Packages |
|--------|---------:|
| [01 - Universal App Scripts](./01%20-%20Universal%20App%20Scripts) | 1 (universal detect / install / uninstall) |
| [02 - Dell Command Suite](./02%20-%20Dell%20Command%20Suite) | 4 |
| [03 - Display and Peripheral](./03%20-%20Display%20and%20Peripheral) | 4 |
| [04 - Optimizer and Power](./04%20-%20Optimizer%20and%20Power) | 2 |
| [05 - Support Assist and Trusted Device](./05%20-%20Support%20Assist%20and%20Trusted%20Device) | 3 |
| [06 - Microsoft Runtimes](./06%20-%20Microsoft%20Runtimes) | 2 |
| [07 - Documentation](./07%20-%20Documentation) | 1 (PDF) |

## How to use

1. Open the category and (when present) the app package folder.
2. Use `*_install.ps1`, `*_uninstall.ps1`, and `*_DetectionRule.ps1` as the Intune Win32 install / uninstall / detection rule scripts.
3. For multi-app packaging, start with `01 - Universal App Scripts` if you use the universal wrappers.
4. Install required runtimes from `06` before apps that depend on them (for example SupportAssist / Trusted Device).
5. Package as Win32 (`.intunewin`), assign to Dell device groups, and pilot before broad rings.
6. Read `07 - Documentation` for version-specific install instructions.

## Requirements

- Microsoft Intune (Win32 app deployment)
- Role such as **Intune Administrator**
- Dell commercial Windows endpoints (PowerShell 5.1+)
- Vendor installers / media for each Dell tool you package

## License

This project is licensed under the [MIT License](./LICENSE).

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
