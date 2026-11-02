# Avenrail

A desktop workspace for your coding agents. This repository publishes Avenrail's installers and the feed the app reads to update itself, and it is where to report problems.

**[Download the latest release](https://github.com/ashish200729/avenrail-releases/releases/latest)**

| Mac | File |
| --- | --- |
| Apple Silicon (M1 and later) | `Avenrail_<version>_aarch64.dmg` |
| Intel | `Avenrail_<version>_x64.dmg` |

Open the DMG, drag Avenrail into Applications, and open it from Applications rather than from the disk image, so it can update itself. Windows and Linux builds are coming later.

## Opening Avenrail on macOS

Avenrail's macOS builds are signed ad hoc but not notarized by Apple. On the first launch of a downloaded copy, macOS says it cannot verify the developer. Allow it once, in either way:

- **System Settings.** Try to open Avenrail, close the warning, then open System Settings › Privacy & Security, scroll to Security, and click **Open Anyway** next to Avenrail. Confirm with your password. On macOS 14 and earlier, Control-clicking the app and choosing **Open** also works.
- **Terminal.** Remove the download quarantine flag: `xattr -dr com.apple.quarantine /Applications/Avenrail.app`

Later launches open directly. Only allow builds you downloaded from this repository's [releases](https://github.com/ashish200729/avenrail-releases/releases).

## Updates

Avenrail checks this repository's latest release when it starts and every six hours while it stays open. When a new version is out, an **Update** button appears at the bottom of the sidebar, and **Settings → Version → Check for updates** checks on demand. The update is verified against the signing key built into the app before it installs, and the app refuses any update whose signature doesn't match. Avenrail then restarts; if chats are running it asks first, and they resume afterwards.

## Verifying a download

Every release lists the SHA-256 of each file in `SHA256SUMS.txt`:

```sh
shasum -a 256 -c SHA256SUMS.txt --ignore-missing
```

## Reporting a problem

[Open an issue](https://github.com/ashish200729/avenrail-releases/issues/new/choose) with your Avenrail version and macOS version. Report security vulnerabilities [privately](https://github.com/ashish200729/avenrail-releases/security/advisories/new), never in a public issue.

## About this repository

Avenrail's source code is private. Releases are built from it by GitHub Actions and posted here only when the maintainer publishes one. Nothing runs in this repository.
