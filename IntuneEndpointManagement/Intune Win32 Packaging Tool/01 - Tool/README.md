# Tool

Microsoft Win32 Content Prep Tool executable used to create `.intunewin` packages for Intune.

## Files

| File | Purpose |
|------|---------|
| `IntuneWinAppUtil.exe` | Pack source folder + setup file into `.intunewin` |

## How to use

```text
IntuneWinAppUtil.exe -c "<sourceFolder>" -s "<setupFile>" -o "<outputFolder>" [-q]
```

Then add the `.intunewin` as a Windows app (Win32) in Intune.

## License

MIT License for Ozark docs — see [LICENSE](../LICENSE).

The executable is licensed under Microsoft terms — see [03 - License](../03%20-%20License).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
