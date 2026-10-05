# Isnad — releases

Builds of **Isnad**, a local-first AI workspace for the Mac. Chat, documents, memory, agents and tools in one app; answers come from models running on your machine, and your data stays in an encrypted database on your disk.

This repository holds release files only. The source is not here.

## Download

Get the latest beta from **[Releases](https://github.com/im3an/isnad-releases/releases)**: the file ending in `_aarch64.dmg`.

**Requirements:** an Apple Silicon Mac (M1 or later), 16 GB of memory or more recommended, and about 8 GB of free disk space for the models.

## Install

1. Check the download against the SHA-256 published with the release:

   ```bash
   shasum -a 256 ~/Downloads/Isnad_*_aarch64.dmg
   ```

2. Open the DMG and drag **Isnad** into Applications.
3. Beta builds are not yet signed with an Apple Developer ID. The first time, right-click the app, choose **Open**, then confirm. If macOS still refuses:

   ```bash
   xattr -dr com.apple.quarantine "/Applications/Isnad.app"
   ```

4. Follow the setup window. It checks for [Ollama](https://ollama.com/download) and downloads the models Isnad needs, or uses a chat model you already have.

## Updates

From beta 5 on, Isnad checks this repository for a newer release shortly after launch and every six hours, and offers it in a notification. Every update is signed, and the app refuses one whose signature doesn't match the key built into it. *Check for updates…* in the account menu checks on demand.

The `.app.tar.gz` and `.sig` files on each release are for the in-app updater, and `latest.json` on the `updater` release tells installed apps which version is current. You don't need to download them yourself.

## Feedback

Use **Send beta feedback** in the account menu at the bottom left of the app. It opens an email with your version and platform filled in. If something broke, attach `~/Library/Application Support/app.isnad.desktop/logs/backend.log`.
