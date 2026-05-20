# iOS 18x-26 jailed customization 
# iOS System Customization, SparseRestore & Jailbreak Ecosystem (iOS 18x - iOS 26.x)

A curated, legally compliant directory documenting advanced system customization utilities, MobileGestalt modding suites, entry-level entitlement bypass frameworks, and specific jailbreak environments for modern iOS branches (including iOS 18.x up to early iOS 26.x iterations). 

These utilities leverage native backup manipulation patterns (`SparseRestore`), backup injection mechanisms, MDM configuration profiles, native iOS Shortcuts, or specific kernel exploit chains (such as the `DarkSword` webkit/kexploit stack) to execute modifications without relying on standard Apple Developer account limitations.

## ⚠️Legal Disclaimer & Independent Compliance Notice
**CRUCIAL NOTICE:** This repository functions strictly as an independent, educational directory and informational index. The maintainer of this repository has **absolutely no affiliation, partnership, or connection with the developers, entities, or actions** of the projects listed below (including but not limited to jailbreak.party, zeroxjf, the creator of FilzaJailedDS, lunginspector, Lars Fröder (opa334), or individual security research groups). 
>  This repository is for educational and research purposes only. Using these tools may violate Apple's Terms of Service and is done entirely at your own risk. The maintainer is not responsible for any bootloops, data loss, or bricked devices.
The maintainer does not condone, support, or take responsibility for how these third-party tools are operated, deployed, updated, or maintained by their respective creators. Any execution of kernel-level modifications, jailbreaks, MDM configuration installations, Shortcut actions, Package Managers, or unsandboxed file system modifications is performed strictly at the user's own risk. The maintainer is not liable for data loss, hardware instability, system boot loops, or security vulnerabilities resulting from external exploit implementations.

This repository hosts no proprietary binary files, copyrighted enterprise profiles, encryption keys, or modified application bundles (.IPAs). Use these tools at your own discretion; data back-ups are highly recommended before invoking low-level system configuration writes.

---

## 🛠️ Advanced Customization, Tweaking & Jailbreak Utilities

| Project Name | Supported Versions | Key Functionality & Exploit Vector | Official Open-Source Link |
| :--- | :--- | :--- | :--- |
| **cyanide-ios** | iOS 18.0+ | Advanced open-source **Jailed Package Manager** designed to organize, queue, and deploy non-jailbreak modifications and tweaks directly to the device. | [GitHub Repository](https://github.com/zeroxjf/cyanide-ios) |
| **FilzaJailedDS** | iOS 18.0 - 26.x | Powerful **unsandboxed** file manager utilizing modern kernel vulnerabilities to grant full **read/write (R/W)** root file system access on modern iOS versions. | [GitHub Repository](https://github.com/34306/FilzaJailedDS) |
| **Dopamine** | iOS 15.0 - 16.6.1 / **iOS 18.x (A11 Specific)** | Advanced rootless jailbreak environment. Extended via community implementations to leverage the `DarkSword` exploit chain specifically on legacy A11 hardware running iOS 18 branches. | [GitHub Repository](https://github.com/opa334/Dopamine) |
| **Accessible** | iOS 16.0+ | A jailed file system utility functioning entirely as an **iOS Shortcut**. It requires no exploits and safely enables browsing, viewing, and exporting hidden internal system apps and readable root partitions (e.g., `/System`). | [GitHub Repository](https://github.com/jailbreakdotparty/Accessible) |
| **Lithium** | iOS 17.0+ | An advanced customization tool that functions strictly by utilizing MDM configuration profiles designed for **supervised devices** to toggle strict feature flags (hiding apps from all views, overriding notifications, system-wide preferences). | [GitHub Repository](https://github.com/lunginspector/Lithium) |
| **Pancake Store** | iOS 15.0+ | Advanced third-party utility specialized as an **App Store app downgrader**, allowing users to fetch, deploy, and target legacy application versions. | [GitHub Repository](https://github.com/pancake-team/Pancake) |
| **Lara** | iOS 17.0 - 18.7.1 / 26.0.x | Comprehensive iOS Toolbox using the non-persistent `DarkSword` kexploit. Fine-grained kernel offset modifications. | [GitHub Repository](https://github.com/rooootdev/lara) |
| **Nugget** | iOS 17.0 - 26.0+ | The premier desktop-based MobileGestalt & Feature Flag customization suite. Tweak status bars, wallpapers, and internal UI flags via USB. | [GitHub Repository](https://github.com/leminlimez/Nugget) |
| **SparseBox** | iOS 16.0 - 18.1b5 | On-device MobileGestalt manager, system app internal opener, and app limit bypass utility (requires FMI off). | [GitHub Repository](https://github.com/khanhduytran0/SparseBox) |
| **SparseBoxPlus** | iOS 17.4 - 26.1+ | Community-driven refined iteration of SparseBox featuring an overhauled UI layout and modernized compliance updates. | [GitHub Distribution](https://github.com/jailbreakdotparty/SparseBoxPlus) |
| **BlacklistBeGone** | iOS 16.0 - 18.0.1+ | Desktop automation script utilizing SparseRestore to swap certificate validity databases with directories, preventing revoke tracking. | [GitHub Repository](https://github.com/jailbreakdotparty/BlacklistBeGone) |
| **Bridge** | iOS 16.0+ | Jailed internal system app launcher and asset extractor utility for auditing hidden core binaries. | [GitHub Distribution](https://github.com/jailbreakdotparty/Bridge) |
| **dirtyZero** | iOS 16.0+ | Core development framework focusing on backup-layer property list injection techniques. (Supports iOS 18+ now). | [GitHub Distribution](https://github.com/jailbreakdotparty/dirtyZero) |
| **Cowabunga Lite** | iOS 15.0 - 18.x+ | Desktop-driven backup modification manager. Customizes system configurations, icon themes, and control centers without on-device profiles. | [GitHub Repository](https://github.com/leminlimez/CowabungaLite) |

---

## 🔒 Crucial Implementation Frameworks & Prerequisites

To execute structural data writes via `SparseRestore` or desktop frameworks (`Nugget`, `Cowabunga Lite`), the following infrastructure configuration is uniformly mandated:

1. **Find My iPhone (FMI):** Must be temporarily disabled during the automated backup restoration phase. It can be immediately re-enabled once the partial system database overwrite completes.
2. **Device Connection Requirements:**
   * **Windows Hosts:** Native Apple Devices App or legacy iTunes connection synchronization pipeline is required.
   * **macOS / Linux Hosts:** Requires terminal integration with `pymobiledevice3`, `usbmuxd`, and proper python virtual environments (`venv`).
3. **Supervised Status (Lithium):** Device supervision must be pre-configured via configuration payloads or computer utilities prior to executing Lithium's shortcuts.
4. **Hardware Constraints:** Note that cutting-edge exploit structures (e.g., *FilzaJailedDS*, *Lara*, *Dopamine-DarkSword*) intentionally explicitly exclude A12+ or newer system architectures from specific features due to Pointer Authentication Codes (PAC) and Hardware Memory Tagging Extensions (MTE) unless stated otherwise by specific offset releases. Legacy systems bypass these microarchitectural lockouts.

---

## 📡 Community Integration Node

For bleeding-edge testing binaries, direct workflow logs, and uncompiled alpha/beta builds (such as active *dirtyZero 1.4 betas* or raw *PocketPoster* configurations), consult the core developer network index:


---
*Trademarks: iOS, iPadOS, Shortcuts, CoreTrust, Filza, Cyanide, and Dopamine are legal property of Apple Inc. and their respective original developers. This independent documentation directory maintains no corporate affiliation, endorsement, or responsibility regarding the external developers, third-party repositories, or their specific software actions.* 