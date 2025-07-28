# KB: Automating Windows 11 PE-Phase Installation

## Executive Summary

This KB outlines the process of creating a fully automated Windows 11 installation experience through the Windows PE phase. It is intended for IT professionals who require a hands-free, efficient reimaging process.

## Objectives

- Eliminate manual input during Windows PE setup
- Auto-wipe and partition the disk
- Inject Wi-Fi drivers for early connectivity
- Skip OOBE to allow post-setup customization

## Tools & Resources

| Tool | Purpose |
|------|---------|
| [Unattend Generator](https://schneegans.de/windows/unattend-generator/) | Initial XML creation |
| Windows System Image Manager (WSIM) | XML customization |
| [NTLite](https://www.ntlite.com/) | Driver injection |

## Implementation Steps

1. **Generate Base XML**
   - Use the Unattend Generator to create a base `autounattend.xml`.

2. **Customize with WSIM**
   - Remove OOBE-related components.
   - Ensure disk configuration and locale settings are defined.

3. **Inject Drivers with NTLite**
   - Add Wi-Fi drivers to the Windows image.
   - Save and export the updated ISO.

4. **Deploy**
   - Copy `autounattend.xml` to the root of the bootable USB.
   - Boot target machine and let setup run unattended.

## Notes

- This setup is ideal for environments where IT staff need to multitask during reimaging.
- OOBE can be completed manually later or scripted separately.

## Troubleshooting

- **Setup halts at OOBE**: Ensure OOBE components are removed from XML.
- **No network**: Verify Wi-Fi drivers are compatible and properly injected.

## Related Articles

- [How to Inject Drivers with NTLite](https://www.ntlite.com/documentation/)
- [Microsoft Docs: Windows Unattended Setup Reference](https://learn.microsoft.com/en-us/windows-hardware/customize/desktop/unattend/microsoft-windows-setup)
