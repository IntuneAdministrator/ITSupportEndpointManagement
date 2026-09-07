# Microsoft 365 Repair Scripts

Client and tenant repair scripts for Outlook, Teams, Office apps, OneDrive, Exchange, Entra ID, and user lifecycle, plus unified recovery tools.

## Categories

| Folder | Items |
|--------|------:|
| [01 - Outlook](./01%20-%20Outlook) | 3 |
| [02 - Teams](./02%20-%20Teams) | 1 |
| [03 - Office Apps](./03%20-%20Office%20Apps) | 4 |
| [04 - OneDrive](./04%20-%20OneDrive) | 1 |
| [05 - Exchange Online](./05%20-%20Exchange%20Online) | 1 |
| [06 - Entra ID](./06%20-%20Entra%20ID) | 2 |
| [07 - User Lifecycle](./07%20-%20User%20Lifecycle) | 1 |
| [08 - Unified and Recovery Tools](./08%20-%20Unified%20and%20Recovery%20Tools) | 3 |

## How to use

1. Open the category for the app or workload you are repairing.
2. Run the package script (often with a `launch.bat` helper).
3. Prefer least-privilege admin rights; reboot or resign-in when the script requires it.

## Requirements

- Windows PowerShell 5.1+ or PowerShell 7 where noted
- Appropriate admin rights for the workload you are targeting
- Pilot before production use

## License

This project is licensed under the [MIT License](./LICENSE).

Upstream or bundled third-party tools may ship their own license terms - honor those for those packages.

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
