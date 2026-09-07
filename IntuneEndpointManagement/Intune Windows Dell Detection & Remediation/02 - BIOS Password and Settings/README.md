# BIOS Password and Settings

Detection and remediation scripts for Dell BIOS admin password and settings (fastboot, thermal mode, setting compliance). Firmware package is marked **Do Not Use**.

## Packages

| Package | Notes |
|---------|-------|
| `BIOS Admin Password` | Detect / remediate admin password setting; includes change detection |
| `BIOS Fastboot` | Detect / remediate Fastboot setting |
| `BIOS Thermal Mode` | Detect / remediate thermal mode |
| `BIOS Setting Compliant` | Detect / remediate BIOS setting compliance |
| `BIOS Firmware (Do Not Use)` | Reference only — do not assign |

## How to use

1. Open the package folder and review detection / remediation scripts.
2. Deploy as an Intune Remediation (system context recommended).
3. Confirm BIOS password / privilege requirements before remediating production fleets.
4. Do not deploy **BIOS Firmware (Do Not Use)**.

## License

MIT License — see [LICENSE](../LICENSE).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
