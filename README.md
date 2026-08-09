# Tephra Terminal

> **Formerly LiqScope.** Same app, new name — if you came here looking for LiqScope, you're in the right place.

Native desktop app downloads for Tephra Terminal — an estimated liquidation heatmap tool. See the [Releases](../../releases) page for Mac, Windows, and Linux builds.

**Heads up:** the current installers are still named `LiqScope-*`, and the app window still shows "LiqScope" in its title bar. That's cosmetic left over from the rename — the app itself is current, and the naming will be corrected in the next release.

---

## ⚠️ First launch — you will see a security warning

The app isn't signed with a paid developer certificate, so **macOS and Windows both show a scary-looking warning the first time you open it.** This is expected. Here's how to get past it — you only have to do it once.

### macOS

Requires **macOS 12 or later**. Universal build — runs natively on both Intel and Apple Silicon Macs.

You'll see: **"LiqScope" Not Opened — Apple could not verify "LiqScope" is free of malware.**

**On macOS 15 (Sequoia) and newer**, that dialog only offers a *Done* button. There is no way through from the dialog itself — you have to allow it in Settings:

1. Click **Done** to dismiss the warning
2. Open **System Settings → Privacy & Security**
3. Scroll down to the **Security** section — you'll see *"LiqScope" was blocked to protect your Mac*
4. Click **Open Anyway**
5. Confirm with your password or Touch ID
6. Open the app again — it launches normally, and won't ask again

**On macOS 14 and earlier** it's quicker: **right-click (or Control-click) the app → Open**, then click **Open** in the dialog. Double-clicking will *not* offer this option — you have to use the right-click menu.

**Terminal alternative** (any macOS version, instant):

```bash
xattr -cr /Applications/LiqScope.app
```

### Windows

SmartScreen shows: **"Windows protected your PC"**.

1. Click **More info**
2. Click **Run anyway**

### Why this happens

Removing these warnings entirely requires a paid Apple Developer account and a Windows code-signing certificate. This project uses neither, so the warnings are unavoidable for now. The app is a thin wrapper that displays the Tephra Terminal website — it doesn't install background services or change system settings.

---

## Troubleshooting

**"You can't use this version of the application … requires macOS 26.0 or later"**

You have an old download. This was a build bug, fixed 2026-08-09 — the app actually supports macOS 12 and later. Delete it, then re-download `LiqScope-Mac.dmg` from [Releases](../../releases). The filename didn't change, so if your browser serves the same broken file from cache, clear it or force a fresh download.

**The app opens but can't load anything**

The app displays a live site, so it needs an internet connection and the service needs to be up. Wait a few minutes and reopen.
