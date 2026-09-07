# x86

32-bit `ServiceUI.exe` for interactive UI during system-context Win32 installs on 32-bit Windows (or when a 32-bit session/process is required).

## Files

| File | Purpose |
|------|---------|
| `ServiceUI.exe` | Launch interactive process in the user session (x86) |

## How to use

1. Copy into your Win32 app source folder when targeting x86.
2. Reference it from the install command (with your interactive payload).
3. Use **01 - x64** instead for typical 64-bit endpoints.

## License

MIT License for Ozark docs — see [LICENSE](../LICENSE).

`ServiceUI.exe` remains under original Microsoft / MDT licensing.

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
