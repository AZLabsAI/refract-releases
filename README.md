<div align="center">

# Refract

**Say it messy. Send it right.**

Refract rewrites the text you type or dictate so it fits the app you're in: email, chat, an AI prompt, a bug report.
One click or one shortcut, and the rewrite lands back in your text box.

[![macOS](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAZLabsAI%2Frefract-releases%2Fmain%2Flatest.json&query=%24.mac.version&prefix=v&label=macOS&color=7b6cff)](https://github.com/AZLabsAI/refract-releases/releases?q=mac-v)
[![Windows](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAZLabsAI%2Frefract-releases%2Fmain%2Flatest.json&query=%24.windows.version&prefix=v&label=Windows&color=34a8d4)](https://github.com/AZLabsAI/refract-releases/releases?q=windows-v)
[![Microsoft Store](https://img.shields.io/badge/Microsoft%20Store-get%20it-0a1023)](https://apps.microsoft.com/detail/9PH9Q8N4B37S)

</div>

This repository holds the downloads and the update feed for Refract, a free app by [AZ Labs](https://azlabs.ai). The source code is private.

## Download

| | Get it | You need |
|---|---|---|
| **Windows** | Newest `windows-v…` release: [Releases → Windows](https://github.com/AZLabsAI/refract-releases/releases?q=windows-v), file `Refract-Setup-<version>-win-x64.exe`. Or the [Microsoft Store](https://apps.microsoft.com/detail/9PH9Q8N4B37S). | Windows 10 or 11, 64-bit. No admin rights. |
| **macOS** | Newest `mac-v…` release: [Releases → macOS](https://github.com/AZLabsAI/refract-releases/releases?q=mac-v), file `Refract-<version>-mac.zip`. | macOS 14 or later, Apple silicon. |

The Store version is updated by the Store, so it can trail the direct download by a few days. Direct downloads update themselves (see below).

## Install

**Windows**

1. Run the installer and choose **Install**. It installs for your account only and adds a Start menu shortcut.
2. The installer isn't code-signed yet, so SmartScreen may warn you. Choose **More info**, then **Run anyway**.
3. Refract lives in the notification area. Click it to open Settings and pick an AI provider.
4. To remove it: **Settings → Apps → Installed apps → Refract**.

**macOS**

1. Unzip and drag **Refract** to Applications.
2. The app isn't notarized by Apple yet. The first time, Control-click it, choose **Open**, then confirm.
3. Allow **Accessibility** when asked. Refract needs it to read your text and put the rewrite back.
4. Open the menu bar icon, then **Settings**, and pick an AI provider.

## Use it

Highlight some text (or click into the box), then click the floating glass button, tap **Ctrl + Shift**, or press **Ctrl + Alt + R** (Windows) or its Mac equivalent. Right-click the button for other presets. Drag its lower-right corner to resize it. **Ctrl + Alt + Z** undoes a rewrite on Windows.

You bring the AI: a provider key, a ChatGPT plan sign-in, or a local model through Ollama or LM Studio.

## Updating

Open **Settings** and choose **Check for updates**. Refract also checks in the background every few hours, and you can turn that off in the same place. An update is downloaded, checked against the SHA-256 published in [`latest.json`](latest.json), and installed. Your settings and keys stay. On the Mac the update must also be signed by the same developer as the app you are running.

The Microsoft Store build doesn't use this updater.

## Check a download yourself

Compare the hash of your file with the `sha256` for your platform in [`latest.json`](latest.json).

```bash
# macOS
shasum -a 256 Refract-<version>-mac.zip
```

```powershell
# Windows
Get-FileHash .\Refract-Setup-<version>-win-x64.exe -Algorithm SHA256
```

## Privacy

Refract sends your text to the AI provider you choose, plus any backup providers you configure. The update check only downloads `latest.json` from this repository. It sends no text, keys or settings. More in Settings → About.

## Help

Questions or problems: [azlabs.ai/contact](https://azlabs.ai/contact).
