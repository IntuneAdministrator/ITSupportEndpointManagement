# Intune macOS Management Scripts

macOS management content for Microsoft Intune: app installers, configuration scripts, custom attributes, custom profiles, and admin tools. Organized by numbered categories for the Ozark / IT Support Endpoint Management working set.

## Categories

| Folder | Subcategories | Packages |
|--------|--------------:|---------:|
| [01 - Apps](./01%20-%20Apps) | 8 | 39 |
| [02 - Config](./02%20-%20Config) | 7 | 53 |
| [03 - Custom Attributes](./03%20-%20Custom%20Attributes) | 5 | 33 |
| [04 - Custom Profiles](./04%20-%20Custom%20Profiles) | 6 | 20 |
| [05 - Tools](./05%20-%20Tools) | 3 | 8 |

## How to use

1. **Apps** — Deploy install/uninstall scripts as Intune scripts or package them for LOB / shell scripting workflows. Review each package `readme.md` when present.
2. **Config** — Assign as platform / remediation scripts; confirm run context (root vs. user).
3. **Custom Attributes** — Register as Intune custom attributes; scripts should return a single clear value on stdout.
4. **Custom Profiles** — Upload `.mobileconfig` files as custom configuration profiles; replace Contoso / tenant-specific values.
5. **Tools** — Run from an admin workstation or during enrollment/migration projects as documented per tool.

Always pilot on a test ADE ring before broad assignment.

## Requirements

- Microsoft Intune with macOS enrollment (ADE preferred for many profiles)
- Role such as **Intune Administrator**
- macOS test devices for validation
- Network access to vendor download URLs used by install scripts

## License

This project is licensed under the [MIT License](./LICENSE).

Third-party scripts, profiles, and vendor installers remain subject to their upstream / vendor licenses where applicable.

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
