# Update Analyzer  
A universal, distro‑neutral update visibility tool for Debian/Ubuntu/Mint systems.  

## Overview
Most Linux update tools — especially Linux Mint’s Update Manager — show only a curated subset of available updates. They hide or collapse:  
- phased updates  
- dependency updates  
- library siblings  
- transitional packages  
- Ubuntu Pro client updates  
- Flatpak runtimes and SDKs  
- non‑Mint‑maintained packages  
- packages that appear “upgradable” but are not installed locally  

Update Analyzer exposes the **complete, unfiltered truth** of your system’s update state. It reads the system directly — no logs, no assumptions, no filtering.  This is the update visibility Linux desktops should have had all along.  

---

## Features

### **A. Full APT visibility**
Shows *all* upgradable packages, including:
- libraries  
- transitional packages  
- minimal/t64 variants  
- dependency‑driven updates  
- runtime siblings  
- packages Mint Update Manager hides  

No filtering. No guessing. No UI curation.

---

### **B. Phased update detection (with status colors)**

- 🟢 **Green** — Eligible update  
  Your machine is inside the rollout percentage, or the update is not phased.

- 🟡 **Yellow** — Phased update (not yet eligible)  
  The update exists, but your machine is outside the rollout percentage. Mint Update Manager hides these entirely.  

- 🔴 **Red** — Package NOT installed locally  
  (APT reports an update for a package that is not installed.) 
  This happens with transitional packages, optional components, or leftover metadata.The analyzer exposes these so you see the real APT state.

---

### **C. Flatpak integration**
Flatpak is now a major part of the Linux desktop. The analyzer includes:

- app updates  
- runtime updates  
- SDK updates  
- extension updates  

Mint Update Manager shows only selective Flatpak updates. The analyzer shows **all** of them.  

---

### **D. Manually Installed .deb Packages**
The analyzer detects packages installed manually via `.deb` files (outside APT).

These packages:
- are not tracked by APT  
- do not receive version or security metadata  
- cannot be evaluated for updates  

The analyzer marks them with a **neutral grey “?” icon** and displays **“N/A”** for update fields. This makes their status explicit instead of silently ignoring them.  

---

### **E. Distro‑neutral**
Works on any Debian‑based system:

- Linux Mint  
- Ubuntu  
- Debian  
- Pop!\_OS  
- KDE Neon  
- Zorin  
- Elementary  
- Linux Lite  
- Raspberry Pi OS  
- Anything APT‑based  

No Mint‑specific logic. No assumptions. Just **APT + Flatpak truth**.  

---

## Installation

Prebuilt Linux bundles are provided on the **Releases** page.

1. Download the latest `update-analyzer-linux-x64-<version>.zip`.
2. Extract it:
   
   unzip update-analyzer-linux-x64-<version>.zip
   cd bundle

3. Run the analyzer:

   ./update_analyzer


Alternatively, you may also double‑click the `update_analyzer` executable in your file manager to run the application. This works because the file manager automatically sets the working directory to the bundle folder.

---

## Why This Tool Exists
Linux Mint’s Update Manager tries to mimic the simplicity of Windows Update.  But Linux is a package‑centric, transparent, decentralized ecosystem.  Hiding updates creates confusion — especially with phased rollouts and Flatpak runtimes.  Update Analyzer restores:

- **accuracy**  
- **visibility**  
- **control**  
- **trust**  

It shows the system as it actually is, not as a curated UI wants it to appear.

---

## Contributing
Contributions are welcome.  Although this release ships only the shell‑script analyzer, the project itself is **built in Flutter**. If you are interested in the source, please contact the author through GitHub. Bug reports and feature suggestions are appreciated.

## License
MIT License.

