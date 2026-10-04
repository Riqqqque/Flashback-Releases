# Flashback

**Your best moments, already waiting.**

Flashback is a fast, local-first instant replay recorder for Windows 11. It keeps the last moments of your screen in a rolling buffer and saves them as an MP4 only when you press a key, already filed under the game you were playing. Recording, screenshots, editing and your library are free and never need an account. Flashback Cloud is an optional paid add-on for sharing.

This repository is the official public home for Flashback's Windows installers, their SHA-256 checksums, and the [Flashback wiki](https://github.com/Riqqqque/Flashback-Releases/wiki). The application source is maintained separately and isn't public.

## Download

- **[flashbk.gg](https://flashbk.gg)**: the Download button always points at the current release.
- **[Latest release](https://github.com/Riqqqque/Flashback-Releases/releases/latest)** on this repository.

Flashback runs on 64-bit Windows 11 and is built for a GPU with a hardware video encoder (most current NVIDIA, AMD and Intel graphics). The 0.8.0 installer is about 106 MB. Setup is a single step with its own install screen: it installs for your Windows user, with no administrator prompt and no Visual C++ or other runtime to install first. See [System Requirements](https://github.com/Riqqqque/Flashback-Releases/wiki/System-Requirements) and [Getting Started](https://github.com/Riqqqque/Flashback-Releases/wiki/Getting-Started).

Don't download Flashback installers from unofficial mirrors.

## New in 0.8.0

- **Editable audio tracks for everyone**: a Flashback mix every player plays, plus Game and desktop and Microphone tracks, on by default with no microphone needed. **Record audio from** picks one speaker or headset. ([Audio](https://github.com/Riqqqque/Flashback-Releases/wiki/Audio))
- **Clean microphone audio**: the static on voice in clips from 0.7.22 to 0.7.41 is fixed, and Flashback warns you when the microphone itself drops audio. ([Troubleshooting Audio](https://github.com/Riqqqque/Flashback-Releases/wiki/Troubleshooting-Audio))
- **Game profiles for any game or app**, name presets and folder layouts with a live preview, and an Editor and Montage that open clips straight from your library, with music, fades and crossfades for montages. ([Per-Game Profiles](https://github.com/Riqqqque/Flashback-Releases/wiki/Per-Game-Profiles), [Naming and Organization](https://github.com/Riqqqque/Flashback-Releases/wiki/Naming-and-Organization), [Editor and Montage](https://github.com/Riqqqque/Flashback-Releases/wiki/Editor-and-Montage))
- **A redesigned Cloud tab**, profile links at `flashbk.gg/<username>`, and Cloud account deletion you can undo for seven days. Cloud opens from its server, and the Cloud tab shows whether it's open. ([Flashback Cloud](https://github.com/Riqqqque/Flashback-Releases/wiki/Flashback-Cloud))
- Keycap shortcut fields, a Ghost Mode switch in the tray, Discord status settings that say who sees your status and its **Get Flashback** link, Flashback on .NET 10 with its own trimmed FFmpeg build, and a one-step installer.

## What's in a release

Each Flashback release here (0.6.74 and later) is an immutable tag with exactly two files:

| File | What it is |
|---|---|
| `Flashback-Setup-<version>.exe` | The installer, signed through Microsoft Artifact Signing |
| `SHA256SUMS.txt` | The installer's SHA-256 checksum |

Releases tagged `ffmpeg-...` hold the complete corresponding source of the FFmpeg build Flashback bundles. GitHub also adds **Source code (zip / tar.gz)** archives to every release; they contain only this README, not Flashback.

## Verify your download

1. **Check the hash.** In PowerShell:

   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Flashback-Setup-<version>.exe" -Algorithm SHA256
   ```

   The result must match the release's `SHA256SUMS.txt` and the checksum on [flashbk.gg/faq](https://flashbk.gg/faq).

2. **Check the signature.** Right-click the installer, choose **Properties > Digital Signatures**, and confirm Windows reports a valid signature from a named, verified publisher, not "Unknown publisher".

Because the signing certificate is new, Windows SmartScreen may still show "Windows protected your PC" for a while. Choose **More info**, check the publisher, then **Run anyway**. Step-by-step help: [Verifying Downloads](https://github.com/Riqqqque/Flashback-Releases/wiki/Verifying-Downloads).

Updates installed from inside Flashback are verified automatically: every update needs two independent signatures, a matching package hash and a pinned publisher before it installs. See [Update Security Chain](https://github.com/Riqqqque/Flashback-Releases/wiki/Update-Security-Chain).

## Learn more

The [wiki](https://github.com/Riqqqque/Flashback-Releases/wiki) covers everything about Flashback 0.8.0 and Flashback Cloud:

- **Using it:** [Getting Started](https://github.com/Riqqqque/Flashback-Releases/wiki/Getting-Started), [Instant Replay](https://github.com/Riqqqque/Flashback-Releases/wiki/Instant-Replay), [Settings Reference](https://github.com/Riqqqque/Flashback-Releases/wiki/Settings-Reference), [FAQ](https://github.com/Riqqqque/Flashback-Releases/wiki/FAQ) and [Troubleshooting](https://github.com/Riqqqque/Flashback-Releases/wiki/Troubleshooting).
- **Cloud:** [Flashback Cloud](https://github.com/Riqqqque/Flashback-Releases/wiki/Flashback-Cloud), [Sharing and Visibility](https://github.com/Riqqqque/Flashback-Releases/wiki/Sharing-and-Visibility) and [Profiles and Friends](https://github.com/Riqqqque/Flashback-Releases/wiki/Profiles-and-Friends).
- **How it works:** [Why Flashback Is Light](https://github.com/Riqqqque/Flashback-Releases/wiki/Why-Flashback-Is-Light), [Architecture Overview](https://github.com/Riqqqque/Flashback-Releases/wiki/Architecture-Overview) and [Benchmarks](https://github.com/Riqqqque/Flashback-Releases/wiki/Benchmarks).

Release notes for every version are on [flashbk.gg/changelog](https://flashbk.gg/changelog).

## Community and support

- **Discord community:** [discord.gg/eutwRqvfrw](https://discord.gg/eutwRqvfrw), to talk with other Flashback players.
- **Support:** [flashbk.gg/support](https://flashbk.gg/support) for bugs, account, billing and anything that needs a reply from a person.
- **Security issues:** report privately through the [support form with the Security type](https://flashbk.gg/support?type=security) or to [support@flashbk.gg](mailto:support@flashbk.gg). Please keep details private until a fix ships.

## Licenses and policies

- Flashback is proprietary software: the source code is private, and the official releases may be downloaded and used free of charge under the [Flashback license](LICENSE) and the [Flashback Terms](https://flashbk.gg/terms). Please don't re-host the installer or its files.

- Third-party components and their licenses are listed in the `THIRD_PARTY_NOTICES.md` file and `licenses` folder inside every Flashback install, and summarized on the wiki's [Third-Party Software](https://github.com/Riqqqque/Flashback-Releases/wiki/Third-Party-Software) page.
- [Privacy](https://flashbk.gg/privacy), [Terms](https://flashbk.gg/terms), [Billing and refunds](https://flashbk.gg/refunds), [Acceptable use](https://flashbk.gg/acceptable-use), [Copyright](https://flashbk.gg/copyright) and [Security](https://flashbk.gg/security) are on flashbk.gg.
