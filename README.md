# SysX - SysAdmin & Network Diagnostic Suite

**Version:** 1.2.0  
**Developer:** Romeet R. Singh  
**Platform Support:** Windows (Native GUI & Commands) / Linux & macOS (Fallback Utility Mode)

---

## Overview

**SysX** is a desktop GUI utility engineered for System Administrators, Network Engineers, and IT Support Professionals. Built with Python and Tkinter, SysX consolidates critical administrative utilities, hardware inspection tools, and network diagnostics into a single interface. 

It executes native operating system calls asynchronously in background threads, providing real-time streaming console output without freezing the user interface.

---

## Core Features

* **🖥️ Native Device Info Dashboard:** Native Windows UI rendering full hardware and software specs (OS Build, System UUID, CPU Cores/Cache, RAM Slot breakdown, Disk drives, GPU, BIOS, Active Network Adapters, and Environment Variables).
* **🌐 Advanced Network & DNS Diagnostics:** Includes Ping (with Continuous `-t` and custom packet counts), Ping Default Gateway, Subnet Calculator/Finder, 5-stage Internet Connectivity Diagnostic, Pathping, Traceroute, ARP Table, Routing Table, DNS Lookup, and DHCP Release/Renew.
* **🛡️ Security & File Integrity Tools:** Run System File Checker (`sfc /scannow`), DISM Component Store Repair, Windows Defender Malware Scans, Threat checks, and Security Log inspection.
* **👥 User & Session Management:** Enumerate local users, admin group memberships, active sessions, and system login history.
* **🔌 Remote Access Controls:** One-click options to enable/disable RDP, OpenSSH, WinRM remoting, and launch MSTSC sessions.
* **⚡ Smart Execution Engine:** Every execution automatically clears previous output to ensure clean results. Supports real-time thread cancellation via the **Stop** button.
* **📊 Log Management:** Export streaming execution console logs to plain `.txt` files with a single click.

---

## System Requirements

* **Operating System:** Windows 10, Windows 11, Windows Server 2016+ (Linux/macOS supported for cross-platform network commands).
* **Python Runtime:** Python 3.8 or higher (only required if running from source).
* **Privileges:** Administrator / Root rights recommended for advanced operations (`sfc`, `dism`, `chkdsk`, DHCP renewal).

---

## Installation & Running from Source

1. **Clone or Download the Code:** Save `sysx.py` to your local folder.
2. **Launch Application:**
   * Open PowerShell or Command Prompt as **Administrator**.
   * Run the script:
     ```cmd
     python sysx.py
     ```
     *(Or use `py sysx.py` if `python` path is not explicitly set).*

---

## Compiling to Standalone Executable (`.exe`)

To package **SysX** into a portable, single `.exe` file that runs on any machine without installing Python:

1. Install PyInstaller via the Python module manager:
   ```cmd
   py -m pip install pyinstaller
