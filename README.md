# iOS 18–26 jailed customization tools

A list of iOS customization tools, file managers and jailbreaks, with their underlying methods and version support.

**Version ranges are taken from upstream projects, not independently tested.** Check your exact iOS build and device before installing anything. Some entries also cover iOS 16, 17 or 27 for context.

## Tools

| Tool | iOS support | Method / exploit | Notes |
| --- | --- | --- | --- |
| [Dopamine 3](https://github.com/opa334/Dopamine) | 15–18.7.1; 26.0–26.0.1 on A12/A13 | Kernel exploit chain, varies by build/device | Rootless semi-untethered jailbreak. Hardware restrictions apply. |
| [Dopamine 3 RootHide](https://github.com/roothide/Dopamine-roothide) | Depends on device/build; verify the 3.x branch | Dopamine exploit chain + RootHide | RootHide fork of Dopamine 3. No separate complete version matrix in the 3.x README. |
| [Relaxin](https://github.com/OwnGoalStudio/Relaxin) | Officially documented: 16.5.1–17.3.1; wider support claims unverified | Kernel exploit chain | RootHide-style jailbreak. Archived; treat iOS 18/26 claims cautiously. |
| [FilzaJailedDS](https://github.com/34306/FilzaJailedDS) | 17.0–18.7.1; 26.0–26.0.1 | DarkSword | Filza with elevated filesystem access. Excludes 18.7.2–18.7.7; iPhone 17/M5 support pending upstream. |
| [FilzaSlop](https://github.com/0xjohnnydev/FilzaSlop) | 18, 26; early 27 betas | MobileHouseArrest / MCM bugs | Filza fork with app-container access and PosterBoard tools. Some features and signing methods are restricted. |
| [3105](https://github.com/YangJiiii/3105) | 17.0–18.7.1; 26.0–26.6.1; select 27 betas | Kernel exploit (optional on 17/18), MCM techniques | File browser, patch packages, wallpapers and dialer themes. Enterprise certificate required. |
| [Accessible](https://github.com/jailbreakdotparty/Accessible) | 16+ | None (Shortcuts) | Read accessible system files, inspect MobileGestalt and open system apps. No elevated privileges. |
| [Lithium](https://github.com/jailbreakdotparty/Lithium) | 16+ | None (configuration profiles) | Customizations through profiles on a personally supervised device. |
| [PancakeStore](https://github.com/jailbreakdotparty/PancakeStore) | 16.4+ (historical) | App Store download API | App downgrader; currently marked EOL/non-functional. |
| [Lara](https://github.com/rooootdev/lara) | 17.0–18.7.1; 26.0–26.0.1 | DarkSword | File manager, MobileGestalt and SpringBoard tweaks. No M5/A19 support. |
| [Mond](https://github.com/rooootdev/mond) | 27.0 early betas per support table | `bad_query` / `worse_query`, MCM | MobileGestalt and container tools. The README heading and support table disagree; use the detailed table. |
| [Erosion](https://github.com/jailbreakdotparty/Erosion) | 26.0–26.6.2 (limited); 27.0–27.2.1, 27.3b1 | [`worse_query`](https://github.com/forcequitOS/worse_query) | Wallpaper and dialer tweaks. MobileGestalt editing does **not** work on iOS 26. The upstream header claims wider 26.x coverage than its support list. |
| [Nugget](https://github.com/leminlimez/Nugget) | Up to 26.1 (feature-dependent) | SparseRestore / BookRestore | Desktop MobileGestalt and feature-flag editor. Archived; avoid on iOS 27. |
| [SparseBox](https://github.com/khanhduytran0/SparseBox) | Up to 18.1 beta 5 | SparseRestore | Original on-device MobileGestalt editor; unmaintained. |
| [SparseBoxPlus](https://github.com/jailbreakdotparty/SparseBoxPlus) | 17.4–18.7.4; 26.0–26.1, plus 26.2 dev beta 1 | BookRestore (`bl_sbx`) | On-device MobileGestalt editor. Upstream recommends Nugget instead because setup is unreliable. |
| [Omega](https://github.com/jailbreakdotparty/Omega) | 16–26.x (upstream claim) | Partial backup restore / SparseRestore | Modifies certificate-revocation databases for sideloading. |
| [Bridge](https://github.com/jailbreakdotparty/Bridge) | 16+ | None (system app launch / Shortcuts) | Opens hidden system apps. Its extraction helper is limited on iOS 26.1+. |
| [dirtyZero](https://github.com/jailbreakdotparty/dirtyZero) | 16.0–18.3.2 | CVE-2025-24203 | Zero-file tweaks that usually revert after reboot. Not supported on iOS 18.4+. |
| [iDevice Toolkit](https://github.com/GeoSn0w/iDevice-Toolkit) | 16.0–18.3.2 (system tweaks); up to 18.5 / 26 (limited tools) | CVE-2025-24203; normal IPA tooling | UI tweaks, file manager and IPA injection. The CVE-based tweaks do not extend to iOS 26. |
| [MDC0](https://github.com/34306/mdc0) | Check upstream release for exact builds | CVE-2025-24203 | SpringBoard/UI tweaks using the same file-zeroing bug as dirtyZero. |
| [Cowabunga Lite](https://github.com/leminlimez/CowabungaLite) | Mainly 15–17 | Backup modification | Desktop customization tool, archived in 2024. |

## A few things to know

- **Jailed doesn't mean root.** Container access, a sandbox escape, kernel read/write and a full jailbreak are different levels of access.
- **Versions aren't enough.** Chipset, exact build and signing method can decide whether a tool works.
- **Back up first.** File edits and MobileGestalt changes can cause crashes or bootloops. Check how to revert a tweak *before* applying it.
- **Online jailbreak sites:** Installing a profile or alternative app store isn't a jailbreak. Stick to upstream repositories.

Last reviewed: **2026-11-12**. If something is wrong or outdated, open an issue or PR with an upstream source.
