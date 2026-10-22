# Sakura — official downloads

Sakura is under development by **SoulOfSwords**. This public repository contains release information and downloads, not application source code.

## Latest update — 22 October 2026

New Windows Companion/VTuber installers and Sakura Mobile 0.3.20. Companion chat now prepares confirmed Google Calendar events and keeps the event title separate from spoken scheduling instructions. Agent workspace, grounded answers, voice interruption, camera and model controls are updated. See [22 October release notes](RELEASE-NOTES-2026-10-22.md) for details and testing limits.

## Download

Get the installers from [the releases page](https://github.com/soulofswords/Sakura-Downloads/releases).

- **Sakura VTuber:** Live2D, PMX and VRM avatars, camera tracking, expressions, model customization and phone controls.
- **Sakura Companion:** companion conversations, Gemini or optional local AI, offline Kokoro speech, and VTuber features.
- **Sakura Mobile:** one Android 9+ app with phone-local assistant, PC companion controls, expression selection and phone-camera tracking. Install over the existing Sakura Mobile app as an update. Use the same home network for PC controls or one-time model transfer. Sakura Mobile Local mode then renders the saved model and uses your API key for online chat away from home, without a connected PC.

The latest [22 October 2026 Windows + Android beta](https://github.com/soulofswords/Sakura-Downloads/releases/tag/windows-beta-2026-10-22) contains new Companion/VTuber installers and Sakura Mobile 0.3.20. The older separate VTuber Mobile product is merged into Sakura Mobile for new releases. See the [22 October release notes](RELEASE-NOTES-2026-10-22.md) and [previous release notes](RELEASE-NOTES.md) for changes and testing limits.

Character models are **not bundled**. Import your own models and respect their creators' usage terms. Local AI models are optional downloads. Cloud AI requires your own provider key and internet access; ambiguous keys or custom endpoints require manual provider selection.

## Windows requirements

Windows 10/11 x64 is the target platform. Suggested starting hardware: 8 GB RAM, a modern four-core CPU, graphics with WebGL support, and 5 GB free storage plus space for imported assets. Prefer 16 GB RAM and a dedicated GPU for complex models or streaming. These are provisional targets, not benchmark-certified minimum requirements.

Local Qwen 2B: 16 GB RAM preferred, with 4 GB VRAM recommended. Local Qwen 4B: 16 GB RAM and 6–8 GB VRAM recommended. Gaming and streaming alongside local AI may need more memory. CPU-only inference is slower.

## Updates and verification

Install updates into the existing product's folder to preserve settings and imported artwork. Keep Companion and VTuber in separate installation folders. Back up important personal assets before updating.

Each release includes SHA-256 checksums. In PowerShell, run `Get-FileHash -Algorithm SHA256` with the downloaded file's path and compare it with `SHA256SUMS.txt` in the same release.

The Windows installers contain a compiled native application core and obfuscated first-party JavaScript. This makes inspection harder; it is not irreversible encryption and cannot prevent all reverse engineering. The source repository remains private. Third-party software retains its own license notices.

Publisher branding is SoulOfSwords. These testing installers are not Authenticode-signed; publisher metadata is not a signing certificate.

Android APKs use the existing local testing signing key and package IDs. Physical phone camera/network behavior still requires testing on your device. Camera viewing and face tracking are separate, optional controls. In Companion camera mode, selected images go to the PC's chosen AI provider; PC local Qwen mode keeps image inference local. Phone Local mode uses online provider replies and does not currently inspect the phone screen or camera. Screen viewing makes sampled vision requests, including silent timeline observations while enabled; cloud requests can incur provider charges.

## Feedback

Report reproducible bugs in [Issues](https://github.com/soulofswords/Sakura-Downloads/issues) or join [the Sakura Discord](https://discord.gg/kgxeMRFWDw). Include your product, release version, model format, hardware and reproduction steps. Do not post API keys, pairing codes or personal recordings without reviewing them first.

Protected macOS releases are not available here yet. They require a Mac build host and testing on Apple Silicon.
