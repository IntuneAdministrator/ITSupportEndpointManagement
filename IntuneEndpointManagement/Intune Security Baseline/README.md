# Intune Security Baseline

OpenIntuneBaseline-style security baselines for Microsoft Intune, organized by platform and policy category (Windows 11, Windows 365, macOS, Mobile BYOD).

Policies are JSON exports for Intune Management / native import. Review assignments, scope tags, and version labels (`v3.x` / `v1.0`) before production.

## Categories

| Folder | Subcategories | Files |
|--------|--------------:|------:|
| [01 - Windows 11](./01%20-%20Windows%2011) | 10 | 76 |
| [02 - Windows 365](./02%20-%20Windows%20365) | 3 | 5 |
| [03 - macOS](./03%20-%20macOS) | 3 | 37 |
| [04 - Mobile BYOD](./04%20-%20Mobile%20BYOD) | 1 | 2 |

## How to use

1. Open the platform folder (Windows 11, Windows 365, macOS, or Mobile BYOD).
2. Import or recreate policies in Intune from the JSON exports (Settings Catalog, Compliance, App Protection, etc.).
3. Use **Native Import** copies when your tooling expects that format.
4. Pilot rings (Pilot / UAT / Production) carefully for update and Defender AV rings.
5. Do not assume one-click import for every field — validate in a test tenant first.

## Requirements

- Microsoft Intune
- Roles such as **Intune Administrator** / **Security Administrator**
- Matching platform enrollment (Windows Autopilot / ADE / BYOD app protection)

## License

This project is licensed under the [MIT License](./LICENSE).

Upstream OpenIntuneBaseline / community baseline content remains subject to its original license where applicable.

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
