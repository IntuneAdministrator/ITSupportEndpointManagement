# Universal App Scripts

Shared detect / install / uninstall scripts for packaging multiple Dell tools with one Intune Win32 wrapper pattern.

## Scripts

| File | Role |
|------|------|
| `UniversialDellDetect.ps1` | Detection |
| `UniversialDellInstall.ps1` | Install |
| `UniversialDellUninstall.ps1` | Uninstall |

## How to use

1. Review the universal scripts and align parameters with the apps you bundle.
2. Use them as Win32 install / uninstall / detection entry points when not using per-app scripts from categories `02`–`06`.
3. Pilot on a Dell test group before broad assignment.

## License

MIT License — see [LICENSE](../LICENSE).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
