# Avenrail releases

Installers for [Avenrail](https://github.com/ashish200729/Avenrail), and the feed the app reads to update itself.

**[Download the latest release](https://github.com/ashish200729/avenrail-releases/releases/latest)**

| Platform | File |
| --- | --- |
| macOS, Apple Silicon | `Avenrail_<version>_aarch64.dmg` |
| macOS, Intel | `Avenrail_<version>_x64.dmg` |
| Windows (x64) | `Avenrail_<version>_x64-setup.exe` |
| Linux (x64) | `.deb`, `.AppImage`, or `.rpm` |

On macOS and Windows, Avenrail checks this repository's latest release on launch and offers new versions itself. Linux packages are updated by downloading the new one.

macOS builds are signed ad hoc and not notarized. On the first launch of a downloaded copy, allow it in **System Settings › Privacy & Security › Open Anyway**, or run `xattr -dr com.apple.quarantine /Applications/Avenrail.app`. See [Opening Avenrail on macOS](https://github.com/ashish200729/Avenrail#opening-avenrail-on-macos).

## Verifying a download

Every release lists the SHA-256 of each file in `SHA256SUMS.txt`. Update packages (`.app.tar.gz`, `-setup.exe`) are also signed with Avenrail's updater key, and the app refuses any update whose signature does not match.

## How releases are made

Nothing here runs on a schedule or on a push. A release starts only when the maintainer runs `npm run release:publish -- <version>` in the source repository, which starts [the release workflow](.github/workflows/release.yml). It builds every package from the tagged source, signs the update packages, uploads them to a draft release, and publishes the draft together with `latest.json`. The full process is in [docs/releasing.md](https://github.com/ashish200729/Avenrail/blob/main/docs/releasing.md).

Report problems in the [Avenrail repository](https://github.com/ashish200729/Avenrail/issues).
