# Switchboard Releases

This repository hosts the public release artifacts and changelog for
**Switchboard**, a macOS app for managing groups of Claude Code terminal
sessions. The application source lives in a separate private repository.

## What's here

- **Releases** — signed macOS bundles (`.app`, `.dmg`) and the auto-updater
  artifacts (`.app.tar.gz` + `.sig`) for each version, published under
  [Releases](https://github.com/codeforward-bv/switchboard-releases/releases).
- **`latest.json`** — the [Tauri v2 updater](https://v2.tauri.app/plugin/updater/)
  manifest. The app checks
  `https://github.com/codeforward-bv/switchboard-releases/releases/latest/download/latest.json`
  to discover and download updates.
- **`CHANGELOG.md`** — the [Keep a Changelog](https://keepachangelog.com/)
  history, mirrored here from the app repo.

## Installing

1. Download the `.dmg` of the newest release from the
   [Releases page](https://github.com/codeforward-bv/switchboard-releases/releases)
   (1.0.0-beta.15 or later) and drag Switchboard to your Applications folder.
2. Open Switchboard. Because the app is not notarized by Apple, macOS says it
   could not verify it — click **Done**.
3. Go to **System Settings → Privacy & Security**, scroll to Security and
   click **Open Anyway** next to Switchboard, then confirm.

That is needed only once. The app updates itself from then on, without asking.

Releases before 1.0.0-beta.15 are reported by macOS as *damaged*: their app
bundle was not signed. Install a newer one instead.
