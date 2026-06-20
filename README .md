# 🛡️ PASTER DEFENDER

<p align="center">
  <img src="lateibanner.png" alt="PASTER DEFENDER Banner" width="600"/>
  <br>
  <b>Advanced Malware, RAT & SDK Poisoning Detection and Removal Tool</b>
</p>

---

## ・What is it?

**PASTER DEFENDER** is a security and system sanitization tool designed to analyze, detect, clean, and prevent RATs, malicious compiler execution events, SDK poisoning vectors, and memory droppers. Featuring a custom modern console UI styled with a blue & white theme, layered transparency, and rich command-line animations.

---

## ・Key Features

### 1. Interactive CMD Control Panel
* **Fluid Keyboard Navigation:** Control option selection using the Arrow keys (Up/Down) + Enter, or trigger actions instantly using direct numeric keys (`1`-`8`, `0`).
* **Cumulative Session Threat Badge:** Displays a real-time counter of total files flagged during active use.
* **Administrator Self-Elevation:** Automatically detects user permissions and relaunches with admin privileges to safely handle system-level firewall rules and directory modifications.

### 2. Multi-Vector Anti-Malware Analysis
* **SDK Injection Protection:** Identifies and strips SDK poisoning lines (e.g. `namespace VccLibaries`, `namespace SDKInfector`, `Bombakla`, `Rundollay`, `InfectSDK`, `InfectINIT`) from `.h`/`.hpp` headers.
* **ImGui Obfuscation Cleaner:** Detects and cleans malicious embedded hex binary payloads and hidden system call droppers inside `imgui` configuration source files.
* **PE Executable & YARA Signature Check:** Scans binaries for multiple MZ headers, hijacked executable PE section headers (`.rcd` sections), and known malware patterns.
* **Visual Studio Project Sanitizer:** Scrubs hidden downloader build events (e.g., hidden PowerShell command strings, web requests) from `.vcxproj`/`.csproj` projects and wipes corrupted `.suo` payloads.
* **Chrono-named Temp Dropper Sweep:** Scans temporary directories for chronologically-named executable scripts.

### 3. Active System Immunization
* **Network C2 Block Engine:** Automatically injects known C2 malicious domains into the system `hosts` file and provisions Windows Advanced Firewall block policies for malicious IPs.
* **Process Sweep:** Instantly terminates known malicious executable processes (`Berok.exe`, `Retev.exe`, `Zetolac.exe`, `HPSR.exe`).
* **Real-Time Directory Watcher:** Monitored directories are continuously tracked using `watchdog`. Files created or updated are scanned immediately to block new infections.

### 4. Audiovisual Diagnostics
* **10-Language Glitch Title Bar:** Cycles the console window title bar across 10 languages paired with random matrix styling.
* **Background Audio Cues:** Emits cyberpunk warnings and completion success sound chimes asynchronously without stalling scanning procedures.
* **ASCII Report Grid:** Outputs final threat summary reports inside a beautifully structured ASCII table listing details, categories, and cleanup status.
* **Live Marquee Status:** Renders a cropped path text of the active file at the bottom of the interface.

---

## ・Usage & Requirements

### Technical Requirements
* **Platform:** Windows (with Console Host / command prompt).
* **Python version:** Python 3.8 or newer.
* **Python Libraries:** `pefile`, `yara-python`, `colorama`, and `watchdog` (these are automatically installed by the script if not found).

### Execution

#### Option 1: Run the Precompiled Executable
Download the latest `PasterDefender.exe` from the **Releases** section and run it as Administrator.

#### Option 2: Run from Source
Open a terminal prompt as Administrator and run:
```cmd
python PasterDefender.py
```

---

## ・Disclaimer

This tool is provided for **educational and threat analysis purposes only**. Modifying source headers, building network blocks, and stopping system tasks should be executed with caution on production servers. The developer assumes no liability for system changes.

---
<p align="center">developed by <b>latei</b></p>
