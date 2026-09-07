# Intune Win32 Packaging Tool

Microsoft Win32 Content Prep Tool (`IntuneWinAppUtil.exe`) and related documentation for packaging Win32 apps for Microsoft Intune / Company Portal.

Official source: [Microsoft-Win32-Content-Prep-Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool)

## Categories

| Folder | Contents |
|--------|----------|
| [01 - Tool](./01%20-%20Tool) | `IntuneWinAppUtil.exe` |
| [02 - Documentation](./02%20-%20Documentation) | Upstream README, release notes, security notes |
| [03 - License](./03%20-%20License) | Microsoft license terms (PDF) |

## How to use

1. Open a command prompt or PowerShell.
2. Run `01 - Tool\IntuneWinAppUtil.exe`.
3. Provide:
   - Source folder of the app
   - Setup file (e.g. `.msi` / `.exe` / `.ps1`)
   - Output folder for the `.intunewin` package
4. Upload the generated `.intunewin` in **Intune → Apps → Windows → Add → Windows app (Win32)**.
5. Configure install/uninstall commands, detection rules, and assignments.

Example:

```text
IntuneWinAppUtil.exe -c "C:\Apps\MyApp" -s setup.exe -o "C:\Apps\Out" -q
```

## Requirements

- Windows admin workstation
- Microsoft Intune with Win32 app permissions
- Role such as **Intune Administrator** / **Application Administrator**

## License

This folder's Ozark documentation wrapper is licensed under the [MIT License](./LICENSE).

`IntuneWinAppUtil.exe` and Microsoft documentation remain subject to the [Microsoft License Terms](./03%20-%20License/Microsoft%20License%20Terms%20For%20Win32%20Content%20Prep%20Tool.pdf).

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
