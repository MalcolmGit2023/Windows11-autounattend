# Windows 11 Automated PE-Phase Installer

This project provides a streamlined solution for automating the **Windows PE phase** of a Windows 11 clean installation using `autounattend.xml`. It is designed for IT professionals who need to reimage machines efficiently while multitasking.

## 🔍 Overview

- **Purpose**: Automate Windows 11 setup through the PE phase only.
- **Tools Used**:
  - [Unattend Generator](https://schneegans.de/windows/unattend-generator/)
  - Windows System Image Manager (WSIM)
  - [NTLite](https://www.ntlite.com/) for driver injection
- **Key Features**:
  - Skips OOBE (Out-of-Box Experience)
  - Auto-selects language and region
  - Auto-wipes disk and partitions
  - Injects Wi-Fi drivers for seamless connectivity

## 📂 Contents

- `autounattend.xml`: Customized answer file
- `drivers/`: Injected Wi-Fi drivers
- `docs/`: Knowledge Base article
- `tools/`: Notes on tools and configuration

## 🚀 Usage

1. Place `autounattend.xml` in the root of a bootable Windows 11 USB.
2. Ensure Wi-Fi drivers are injected using NTLite.
3. Boot from USB and let the PE phase complete automatically.

## 📘 Documentation

See [`docs/KB-Automated-PE-Install.md`](docs/KB-Automated-PE-Install.md) for detailed instructions and use cases.
