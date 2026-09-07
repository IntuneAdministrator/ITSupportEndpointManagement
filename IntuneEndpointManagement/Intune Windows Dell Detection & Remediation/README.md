# Intune Windows Dell Detection & Remediation

Dell-focused Microsoft Intune packages for **custom compliance** (JSON + discovery scripts) and **Proactive Remediations** (detection + remediation PowerShell), organized by category.

Use on Dell commercial Windows endpoints. Pilot first. Packages marked **Do Not Use** are kept for reference only — do not assign them in production.

## Categories

| Folder | Packages |
|--------|---------:|
| [01 - Custom Compliance](./01%20-%20Custom%20Compliance) | 5 |
| [02 - BIOS Password and Settings](./02%20-%20BIOS%20Password%20and%20Settings) | 5 |
| [03 - SafeBIOS Remediation](./03%20-%20SafeBIOS%20Remediation) | 1 |
| [04 - Drivers and DCU](./04%20-%20Drivers%20and%20DCU) | 1 |
| [05 - Dell Optimizer and Display](./05%20-%20Dell%20Optimizer%20and%20Display) | 2 |
| [06 - Warranty Remediation](./06%20-%20Warranty%20Remediation) | 1 |

## How to use

1. Open the category and package folder for the control you need.
2. **Custom Compliance** (`01`): import the `.json` policy and wire the sensor `.ps1` in Intune custom compliance.
3. **Remediations** (`02`–`06`): assign detection + remediation under **Intune → Devices → Scripts and remediations → Remediations**.
4. Prefer **system** context unless a script clearly targets the user session.
5. Skip any package or script named **Do Not Use**.
6. Pilot on a Dell test group; confirm exit codes and Intune reporting.

## Requirements

- Microsoft Intune
- Role such as **Intune Administrator**
- Dell commercial Windows endpoints (PowerShell 5.1+)
- Related Dell agents where a package depends on them (DCU, SafeBIOS, Dell Optimizer, DDM, DCM)

## License

This project is licensed under the [MIT License](./LICENSE).

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
