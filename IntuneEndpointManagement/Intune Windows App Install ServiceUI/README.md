# Intune Windows App Install ServiceUI

`ServiceUI.exe` helpers for showing interactive UI (for example during Intune Win32 installs running as SYSTEM). Includes x64 and x86 binaries.

Common pattern: wrap an interactive installer or script with ServiceUI so the logged-on user can see prompts while the Intune package runs in system context.

## Categories

| Folder | Contents |
|--------|----------|
| [01 - x64](./01%20-%20x64) | 64-bit `ServiceUI.exe` |
| [02 - x86](./02%20-%20x86) | 32-bit `ServiceUI.exe` |

## How to use

1. Prefer **x64** on modern 64-bit Windows endpoints.
2. Include the matching `ServiceUI.exe` in your Win32 package source folder.
3. Call it from the install command to launch an interactive process in the user session, for example:

```text
ServiceUI.exe -process:explorer.exe Deploy-Application.exe
```

4. Package with `IntuneWinAppUtil` and assign as a Win32 app in Intune.
5. Pilot on a test device; confirm the UI appears for the signed-in user.

Exact arguments can vary by packaging toolkit (e.g. PSAppDeployToolkit). Match the architecture of ServiceUI to the OS / process you target.

## Requirements

- Windows endpoints (x64 or x86 as appropriate)
- Microsoft Intune Win32 app packaging
- Role such as **Intune Administrator** / **Application Administrator**

## License

This project's Ozark documentation wrapper is licensed under the [MIT License](./LICENSE).

`ServiceUI.exe` remains subject to its original Microsoft / MDT / Deployment Toolkit licensing terms.

## Maintainer

Maintained by the Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
