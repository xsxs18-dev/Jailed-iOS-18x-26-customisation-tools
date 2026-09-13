# Jailed iOS 18.x – 26 Customisation Tools

A running list of jailbreak and jailbreak-adjacent customisation tools that actually work on iOS 18 through 26. Everything below has been checked against its current GitHub repo, so version support and links should be accurate as of **September 13, 2026**.

> ⚠️ Almost everything here works by abusing a real iOS bug (kernel r/w, sandbox escape, backup/restore quirks). That means real risk: bootloops, kernel panics, lost app data, or Apple closing the hole mid-way through you using it. Back up first, and only get these from the links below.

---

| Project | Supported Versions | What it does & how | Official Link |
|---|---|---|---|
| **Dopamine 3.0** | 18.0 – 18.7.1 (A8–A13, arm64) · 26.0 – 26.0.1 (A12/A13) | Full rootless semi-untethered jailbreak. This is also what covers A11 devices on iOS 18 (it's built into the main project now, not a separate community fork). | [GitHub](https://github.com/opa334/Dopamine) |
 (status bar mods, icon themes, live wallpapers, etc.) without a persistent jailbreak.
| **FilzaJailedDS** | 17.0 – 26.0.1 (except 18.7.2–18.7.7) | Unsandboxed file manager using the DarkSword exploit for root-level read/write access. Doesn't work on iPhone 17 series or M5 iPads (Apple's MTE blocks the exploit). | [GitHub](https://github.com/34306/FilzaJailedDS) |
| **FilzaSlop** | 18.x, 26.x, 27 beta 1–4 | Fork of FilzaJailedDS that opens up more container/app-group/system-group access using several sandbox-escape PoCs. Access only lasts as long as the underlying bug is unpatched. | [GitHub](https://github.com/0xjohnnydev/FilzaSlop) |
| **3105** | 17–18, 26.0–26.6.1, 27 beta (verified builds only) | Not a jailbreak — a native app-container browser, `.3105` patch manager, cache cleaner, and PosterBoard wallpaper tool. Kernel exploit use is opt-in. Needs an enterprise cert. | [GitHub](https://github.com/YangJiiii/3105) |
| **Accessible** | 16.0+ (some features need 15.0–18.3.2) | Jailed filesystem utility built as an iOS Shortcut — no exploits at all, so no elevated access. Lets you browse `/System`, `/private/preboot`, open hidden internal apps, and pull your MobileGestalt. | [GitHub](https://github.com/jailbreakdotparty/Accessible) |
| **Lithium** | 16.0+ | Customization tool that works entirely through MDM configuration profiles on a supervised device — hide apps from every view, kill notifications app-wide, custom lock screen text, custom fonts. No exploit, just abusing profiles meant for managed devices. | [GitHub](https://github.com/jailbreakdotparty/Lithium) |
| **PancakeStore** | 16.4+ | App Store downgrader (fork of MuffinStoreJailed) — no exploit used, just abuses Apple's own download-history API. Currently flagged **EoL / non-functional** on its own repo due to Apple backend changes; watch the repo for whether it comes back. | [GitHub](https://github.com/jailbreakdotparty/PancakeStore) |
| **Lara** | 17.0 – 18.7.1 · 26.0.x (M5 and A19 devices excluded) | iOS customization toolbox built on the DarkSword kexploit — MobileGestalt tweaks, Liquid Glass tweaks, kernel offset editing, SpringBoard customizer. Actively maintained, frequent updates. | [GitHub](https://github.com/rooootdev/lara) |
| **Nugget** | up to 18.7.1 / 26.1 (BookRestore) | Desktop MobileGestalt & feature-flag suite over USB — Dynamic Island on any device, PosterBoard, region unlocks, etc. **Archived by its dev as of July 2026** — still works but explicitly should **not** be used on iOS 27 (Apple changed the partial-restore method it relies on). | [GitHub](https://github.com/leminlimez/Nugget) |
| **SparseBox** | up to 18.1b5 | The original on-device MobileGestalt/SparseRestore toolbox. No longer maintained by its dev, who now recommends Nugget or SparseBoxPlus instead — kept here for reference. | [GitHub](https://github.com/khanhduytran0/SparseBox) |
| **SparseBoxPlus** | 17.4 – 26.1 | Actively maintained fork of SparseBox using the BookRestore (`bl_sbx`) exploit instead. On-device MobileGestalt editor, subtype changer, iPadOS UI toggle. | [GitHub](https://github.com/jailbreakdotparty/SparseBoxPlus) |
| **BlacklistBeGone** | 17.0 – 18.0.1 (permanently capped) | Clears the enterprise-cert blacklist/revoke database using SparseRestore, so sideloaded apps stop getting blocked. Dev has said this version will never support anything newer without a new file-write exploit. | [GitHub](https://github.com/jailbreakdotparty/BlacklistBeGone) |
| **Bridge** | 16.0+ | Jailed internal system app launcher and bundle extractor — open and inspect hidden Apple system apps you can't normally reach. | [GitHub](https://github.com/jailbreakdotparty/Bridge) |
| **dirtyZero** | 16.0 – 18.7.1 · 26.0 – 26.0.1 | Customization toolbox that uses various exploits to zero out file memory for its tweaks. Actively getting new tweaks and UI passes. | [GitHub](https://github.com/jailbreakdotparty/dirtyZero) |
| **Cowabunga Lite** | mainly 15.0 – 17.x | Desktop backup-modification tool for icon themes, control center, and system config changes. **Archived since Feb 2024** — most of what it did on newer iOS has been superseded by Nugget, Lithium, and SparseBoxPlus. Kept here since it's still what a lot of guides reference. | [GitHub](https://github.com/leminlimez/CowabungaLite) |

---

## ⚠️ A word of caution: fake "online jailbreaks"

If you see something promising a jailbreak "straight from Safari, no computer needed" — NekoJB Online, zJailbreak, XIXtract, Hacksnow, misaka26, that kind of thing — be careful. Security researchers (Corellium, among others) have shown these don't actually jailbreak anything. They just install a configuration profile with a root certificate that redirects you to an ad-funded third-party app store. Skip these.

