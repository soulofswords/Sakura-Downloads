# Sakura — official downloads

Sakura is under development by **SoulOfSwords**. This public repository contains release information and downloads, not application source code.

## Download

Get the installers from [the latest release](https://github.com/soulofswords/Sakura-Downloads/releases/latest).

- **Sakura VTuber:** Live2D, PMX and VRM avatars, camera tracking, expressions, model customization and phone controls.
- **Sakura Companion:** companion conversations, Gemini or optional local AI, offline Kokoro speech, and VTuber features.

Character models are **not bundled**. Import your own models and respect their creators' usage terms. Local AI models are optional downloads. Gemini requires your own API key and internet access.

## Windows requirements

Windows 10/11 x64 is the target platform. Suggested starting hardware: 8 GB RAM, a modern four-core CPU, graphics with WebGL support, and 5 GB free storage plus space for imported assets. Prefer 16 GB RAM and a dedicated GPU for complex models or streaming. These are provisional targets, not benchmark-certified minimum requirements.

Local Qwen 2B: 16 GB RAM preferred, with 4 GB VRAM recommended. Local Qwen 4B: 16 GB RAM and 6–8 GB VRAM recommended. Gaming and streaming alongside local AI may need more memory. CPU-only inference is slower.

## Updates and verification

Install updates into the existing product's folder to preserve settings and imported artwork. Keep Companion and VTuber in separate installation folders. Back up important personal assets before updating.

Each release includes SHA-256 checksums. In PowerShell, run `Get-FileHash -Algorithm SHA256` with the downloaded file's path and compare it with `SHA256SUMS.txt` in the same release.

The Windows installers contain a compiled native application core and obfuscated first-party JavaScript. This makes inspection harder; it is not irreversible encryption and cannot prevent all reverse engineering. The source repository remains private. Third-party software retains its own license notices.

Publisher branding is SoulOfSwords. These testing installers are not Authenticode-signed; publisher metadata is not a signing certificate.

## Feedback

Report reproducible bugs in [Issues](https://github.com/soulofswords/Sakura-Downloads/issues) or join [the Sakura Discord](https://discord.gg/kgxeMRFWDw). Include your product, release version, model format, hardware and reproduction steps. Do not post API keys, pairing codes or personal recordings without reviewing them first.

Protected macOS releases are not available here yet. They require a Mac build host and testing on Apple Silicon.
