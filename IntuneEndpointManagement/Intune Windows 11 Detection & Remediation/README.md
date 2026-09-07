# Intune Windows 11 Detection & Remediation

Proactive remediations for Windows 11 in Microsoft Intune (detection + remediation PowerShell scripts), organized by category.

Deploy via **Intune → Devices → Scripts and remediations → Remediations**. Set run context (system vs. user), schedule, and scope carefully. Always pilot before broad assignment.

## Categories

| Folder | Packages |
|--------|---------:|
| [01 - Device Compliance](./01%20-%20Device%20Compliance) | 7 |
| [02 - Device Configuration](./02%20-%20Device%20Configuration) | 10 |
| [03 - Device Performance](./03%20-%20Device%20Performance) | 6 |
| [04 - Microsoft Defender AV](./04%20-%20Microsoft%20Defender%20AV) | 10 |
| [05 - Miscellaneous](./05%20-%20Miscellaneous) | 6 |
| [06 - Reporting](./06%20-%20Reporting) | 12 |
| [07 - Toast Creator](./07%20-%20Toast%20Creator) | 1 |
| [08 - Toast Notifications](./08%20-%20Toast%20Notifications) | 11 |

## How to use

1. Open the category and package folder for the remediation you need.
2. Assign the **detection** script and (when present) the **remediation** script in Intune.
3. Prefer **system** context unless the script clearly targets the user profile / HKCU / toasts.
4. Reporting packages often use an empty remediation (`Remediate-Empty.ps1`) — detection is for inventory/reporting signals.
5. Pilot on a test group; confirm exit codes and Intune reporting.

## Requirements

- Microsoft Intune
- Role such as **Intune Administrator**
- PowerShell 5.1+ on Windows 11 endpoints

## License

This project is licensed under the [MIT License](./LICENSE).

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
