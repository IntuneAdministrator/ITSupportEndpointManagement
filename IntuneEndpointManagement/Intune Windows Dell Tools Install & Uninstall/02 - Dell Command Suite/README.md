# Dell Command Suite

Per-app install / uninstall / detection scripts for Dell Command tools used with Intune Win32 packaging.

## Packages

| Package |
|---------|
| `Dell Command Configure` |
| `Dell Command Endpoint Configure Intune` |
| `Dell Command Monitor` |
| `Dell Command Update` |

## How to use

1. Open the package folder and pair scripts with the vendor installer.
2. Wire `*_install.ps1`, `*_uninstall.ps1`, and `*_DetectionRule.ps1` in the Win32 app.
3. Pilot before broad rings; confirm detection matches your install path / version.

## License

MIT License — see [LICENSE](../LICENSE).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
