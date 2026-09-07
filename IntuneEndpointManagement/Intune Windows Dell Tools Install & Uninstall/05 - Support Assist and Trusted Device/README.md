# Support Assist and Trusted Device

Per-app install / uninstall / detection scripts for Dell SupportAssist for Business, its dependency detection, and Dell Trusted Device.

## Packages

| Package | Notes |
|---------|-------|
| `Dell SupportAssist Business` | Install + detection (add uninstall if you maintain one) |
| `Dell SupportAssist Business Dependency` | Detection rule for dependency readiness |
| `Dell Trusted Device` | Install / uninstall / detection |

## How to use

1. Open the package folder and pair scripts with the vendor installer.
2. Install required Microsoft runtimes from `06 - Microsoft Runtimes` when the product requires them.
3. Use the dependency detection package to gate SupportAssist assignment if needed.
4. Pilot before broad rings.

## License

MIT License — see [LICENSE](../LICENSE).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
