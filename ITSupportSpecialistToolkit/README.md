# IT Support Specialist Toolkit

A structured collection of IT support, Windows administration, Microsoft 365 reporting, diagnostics, repair workflows, and technical support resources.

The toolkit is intended for internal IT professionals, systems administrators, endpoint support engineers, and Microsoft 365 administrators who need repeatable troubleshooting and operational resources.

**Maintainer:** [Allester Padovani](https://www.linkedin.com/in/allester-padovani/)  
**GitHub:** [IntuneAdministrator](https://github.com/IntuneAdministrator)

---

## Toolkit modules

| Folder | Purpose |
|---|---|
| [Audit and Report Microsoft 365](./Audit%20%26%20Report%20Microsoft%20365) | Reports covering Entra ID, Exchange Online, SharePoint, Teams, OneDrive, Purview, and licensing |
| [IT Repair and Diagnostic Toolkit](./IT%20Repair%20%26%20Diagnostic%20Toolkit) | Windows and macOS diagnostics, repair catalogs, launchers, deployment resources, and risk documentation |
| [Microsoft 365 Repair Scripts](./Microsoft%20365%20Repair%20Scripts) | Recovery workflows for Outlook, Teams, Office, OneDrive, Exchange Online, and Entra ID |
| [Tech Support Tools](./Tech%20Support%20Tools) | Portable diagnostics, Sysinternals resources, Microsoft troubleshooters, and network/update utilities |
| [Windows 10 and 11 Scripts](./Windows%2010%20%26%2011%20Scripts) | PowerShell-based Windows configuration and support helpers organized by Settings area |
| [Windows Batch File Collection](./Windows%20Batch%20File%20Collection) | Batch-based Microsoft 365, Windows repair, and configuration helpers |
| [Windows Repair Scripts](./Windows%20Repair%20Scripts) | Analysis, audio, malware response, networking, Windows Update, video, and general repair workflows |

---

## Recommended workflow

1. Identify the affected platform and operational area.
2. Open the matching module and read its local documentation.
3. Start with diagnostics and read-only checks.
4. Review scripts and parameters before execution.
5. Use elevation only when required.
6. Test repairs on a non-production device or limited scope.
7. Record the outcome in the applicable ticket or change record.

For the full Windows/macOS GUI catalog, begin with `IT Repair & Diagnostic Toolkit\02 - Launchers`.

---

## Common use cases

- Windows endpoint troubleshooting and repair
- Microsoft 365 service diagnostics and reporting
- User onboarding, offboarding, and account support
- Outlook, Teams, Office, and OneDrive recovery
- Network, Windows Update, audio, video, printer, and performance troubleshooting
- System inventory, security review, and operational reporting
- Repeatable PowerShell or batch-based support procedures

---

## Requirements

- Windows 10/11 (most modules); macOS host for Mac toolkit packs
- Windows PowerShell 5.1 or PowerShell 7 where noted
- Microsoft Graph, Exchange Online, or PnP PowerShell modules for relevant Microsoft 365 scripts
- Appropriate local, endpoint, or tenant administrative permissions

---

## Safety and responsible use

This collection includes read-only diagnostics as well as scripts capable of making significant changes. Consult the [Risk Inventory](./IT%20Repair%20%26%20Diagnostic%20Toolkit/01%20-%20Documentation/RISK-INVENTORY.md) before using high-impact tools.

- Follow least privilege and organizational change-control requirements.
- Back up systems before repair, removal, reset, or cleanup operations.
- Treat unsigned executables and third-party utilities as untrusted until validated.
- Use only properly licensed software and vendor-supported administration methods.
- Never run unfamiliar scripts directly in production.

---

## License

This project is licensed under the [MIT License](./LICENSE).

Third-party utilities and imported scripts retain their original licenses and terms. Review nested license files before use or redistribution.
