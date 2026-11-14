# HackathonApp — Garmin Connect IQ

A Garmin Connect IQ wearable application built in **Monkey C**, structured for rapid AI-assisted prototyping with **Claude Code** and Garmin's Connect IQ SDK.

## Overview

* **Platform:** Garmin Connect IQ (Wearables)
* **Language:** Monkey C
* **Status:** Initial scaffolding & AI agent workflow configured

---

## Tech Stack & Tooling

* **Garmin Connect IQ SDK** & Device Simulator
* **VS Code** with the official **Monkey C** extension
* **Eclipse Temurin JDK** (Java 17/21 LTS) for Monkey C compilation
* **Claude Code** configured with domain-specific Agent Skills:
  * `monkey-c-garmin` — Monkey C syntax, lifecycles, graphics (`Dc`), and Toybox API rules
  * `garmin-dev` — Automated Windows SDK detection, building, and simulator launching

---

## Project Structure

```text
HackathonApp/
├── .claude/
│   └── skills/
│       ├── garmin-dev/        # Build & simulator automation scripts
│       └── monkey-c-garmin/   # Monkey C language & Toybox API reference
├── resources/                 # Layouts, strings, drawables, and bitmaps
├── source/                    # Monkey C (.mc) application and view classes
├── manifest.xml               # App ID, permissions, and supported watch models
├── monkey.jungle              # Build configuration and resource mappings
└── .gitignore                 # Excludes compiled binaries (.prg, .iq) and signing keys (.der)
```

---

## Prerequisites

1. **Java Development Kit (JDK):** [Eclipse Adoptium Temurin 17 or 21](https://adoptium.net) installed on Windows with `JAVA_HOME` configured.
2. **Visual Studio Code** with the **Monkey C** extension installed.
3. **Garmin Connect IQ SDK Manager:** Latest SDK and at least one target device profile downloaded.
4. **Developer Signing Key:** A local `.der` key generated via `Monkey C: Generate a Developer Key` (stored outside this repository).

---

## Getting Started

1. **Clone the repository:**
   ```powershell
   git clone https://github.com
   cd HackathonApp
   ```
2. **Open in VS Code:**
   Open the `HackathonApp` root folder in Visual Studio Code (`File > Open Folder...`).
3. **Verify environment:**
   Open the Command Palette (`Ctrl+Shift+P`) and run **`Monkey C: Verify Installation`**.
4. **Run in the Simulator:**
   Press **`F5`** (or run **`Monkey C: Build Current Project`** followed by **Run Without Debugging**) to compile `bin/HackathonApp.prg` and launch the Connect IQ Simulator.

---

## License

Built for hackathon prototyping.
