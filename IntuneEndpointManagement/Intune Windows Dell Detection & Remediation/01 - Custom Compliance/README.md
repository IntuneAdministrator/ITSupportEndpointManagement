# Custom Compliance

Dell custom compliance policies for Intune: JSON definitions plus discovery/sensor scripts (battery health, SafeBIOS, missing critical drivers via DCU, chassis intrusion, warranty expire).

## Packages

| Package | Contents |
|---------|----------|
| `Battery Health` | Compliance JSON + battery health sensor |
| `SafeBIOS` | Compliance JSON + SafeBIOS sensor |
| `Driver Missing DCU` | Compliance JSON + DCU missing critical drivers sensor |
| `Chassis Intrusion` | Compliance JSON + WMI chassis intrusion sensor |
| `Warranty Expire` | Compliance JSON + DCM warranty expire sensor |

## How to use

1. Open the package folder and review the `.json` policy and sensor `.ps1`.
2. Create or update a **custom compliance** policy in Intune and attach the discovery script.
3. Assign to Dell device groups; pilot before broad rings.

## License

MIT License — see [LICENSE](../LICENSE).

## Maintainer

Ozark Tech Team / [Allester Padovani](https://www.linkedin.com/in/allester-padovani/).
