# Sakura — official downloads

Sakura is an avatar companion and VTuber application by **SoulOfSwords**. This repository contains public downloads, guides and release information; application source code is maintained separately.

**README updated: 29 October 2026**  
**Latest stable release: v1.0.1 · Windows installers refreshed 28 October 2026**

## Download Sakura

| Product | Choose it for | Download |
| --- | --- | --- |
| **Sakura Companion 1.0.1** | Companion conversations, local/cloud AI, Agent workflows and optional VTuber tracking | [Windows x64 installer](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura-Companion-Setup-Windows-x64.exe) |
| **Sakura VTuber 1.0.1** | Standalone avatar tracking, expressions, Chat Reader, voice conversion and streaming | [Windows x64 installer](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura-VTuber-Setup-Windows-x64.exe) |
| **Sakura Mobile 0.3.31** | Android companion controls, phone-camera tracking, model transfer and supported phone-local features | [Android APK](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura-Mobile-Android-0.3.31.apk) |

**[Stable release notes and all downloads](https://github.com/soulofswords/Sakura-Downloads/releases/tag/v1.0.1)** · [Previous releases](https://github.com/soulofswords/Sakura-Downloads/releases)

The October 28 Windows refresh kept version **1.0.1**. If you downloaded an earlier 1.0.1 installer, compare its SHA-256 with the refreshed release's checksums. Mobile 0.3.31 was not rebuilt for that Windows refresh.

Install Companion and VTuber in **separate folders**. Companion includes Companion, VTuber and Agent modes; the standalone VTuber product focuses on tracking and streaming rather than companion chat AI.

## Guides

- [Companion guide — PDF](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura_Companion_Guide.pdf)
- [VTuber guide — PDF](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura_VTuber_Guide.pdf)
- [Both guides — offline HTML ZIP](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/Sakura-1.0.1-Offline-Guides.zip)
- [Release notes](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/RELEASE-NOTES.md)
- [SHA-256 checksums](https://github.com/soulofswords/Sakura-Downloads/releases/download/v1.0.1/SHA256SUMS.txt)

These illustrated guides describe the published 1.0.1 Windows refresh. Development changes listed below may have different navigation until updated installers and guides are released.

## Included in the published 1.0.1 refresh

- **PMX, VRM and Live2D characters:** import your models, use expressions, customize appearance and connect supported tracking sources.
- **Version and graphics settings:** Settings → Theme → About Sakura shows the edition/version; Graphics offers Low, Balanced and High rendering quality.
- **Part appearance expressions:** save a material's color or transparency as a model-specific On/Off preset. Color and opacity remain independent.
- **PMX backgrounds and props:** opt in to add up to four static PMX objects alongside a 3D character, with position, scale and rotation controls. In this published build, Companion's entry is under Memory & privacy → Background & stage items. Scenery is intended for PMX/VRM scenes, not the separate Live2D renderer.
- **Agent workflows:** reviewed text-edit diffs, stale-file protection, bounded execution and recovery, source-linked episodic recall, goal/event automations, approved image/document analysis and task metrics.
- **Library and connection fixes:** required 3D preview page included, expired phone pairings rejected, listener/gateway lifecycle fixes and more reliable Agent approval cards.
- **Separate illustrated guides** for Companion and standalone VTuber.

Agent capabilities depend on the selected model, installed dependencies and connected tools. Skills provide workflow instructions; they do not install services or increase a model's parameters.

## In development — 29 October, not yet in the downloadable installers

The following changes are implemented in the development build and the owner's local apps. **Downloading the current v1.0.1 installers does not include them yet.**

- A simpler **Agent workspace** with a task sidebar, central activity stream and bottom composer, keeping the avatar in its existing position.
- Session-only **Ask for approval / Approve for me / Full access** options, with native Windows confirmation for broader access and existing tool boundaries retained.
- Prompt-driven setup for **Playwright, Firecrawl and Nuclei**, plus reviewed MCP connection setup. Firecrawl needs a provider key; Nuclei needs authorized scan targets. Optional tools are not silently bundled or enabled.
- **MikuMikuDance handoff** for the currently selected PMX, beside PMX Editor. MMD is a separate user-installed application; the handoff is implemented, while live model-rendering verification remains pending.
- A dedicated **Background & stage items** toolbar button in Companion, and separate stage/prop library navigation.
- Additional approval, private-storage, microphone-decoding, startup, camera-ownership and packaging corrections.

New protected installers and release-specific verification are still required before these are described as shipped features.

## Models, accounts and optional downloads

Personal character models, RVC voice weights and local AI weights are **not bundled**. Import your own, or use supported model-library downloads and respect each creator's usage terms. Supported cloud-library imports ask for a **Sakura account**; users do not need the publisher's Jio account.

Cloud AI needs your own provider key and internet access. Local AI, optional RVC runtimes, hardware trackers, browser dependencies, MCP services and messaging gateways may need separate downloads or configuration. Owner publishing credentials, personal MCP connections, account sessions, API keys and conversation history are not included in installers.

Camera viewing and avatar tracking are separate optional features. With cloud vision enabled, selected images or screen samples go to the chosen provider and may incur charges. Local inference requires a compatible vision model. Phone Local mode uses online provider replies and does not currently inspect the phone screen or camera.

## System requirements

**Windows:** Windows 10/11 x64. Suggested starting hardware is 8 GB RAM, a modern four-core CPU, WebGL-capable graphics and 5 GB free storage plus room for models and optional runtimes. Prefer 16 GB RAM and a dedicated GPU for complex characters or streaming. These are provisional recommendations, not benchmark-certified minimums.

**Local AI:** Qwen 2B benefits from 16 GB RAM and roughly 4 GB VRAM; Qwen 4B benefits from 16 GB RAM and 6–8 GB VRAM. Requirements vary with quantization, context, vision, avatar complexity and other running apps. Larger models require substantially more memory. CPU inference is slower.

**Android:** Android 9 or later. Use the same home network for PC controls, tracking or model transfer. Supported saved-model phone-local features can operate without a connected PC; online AI still needs internet.

**macOS:** no verified protected macOS installer is attached to the current release. A native Mac build and Apple Silicon testing are still required.

Tracking performance depends on the camera, phone, network, GPU and model. A fixed 60 FPS is not guaranteed.

## Updating and verifying downloads

1. Back up important personal assets.
2. Close Sakura and install the update into the existing product's installation folder.
3. Keep Companion and standalone VTuber in separate folders.
4. Install the APK over the existing Sakura Mobile app. If an old phone pairing is rejected, create a new pairing code and reconnect.

To verify a Windows download in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 "C:\Downloads\Sakura-Companion-Setup-Windows-x64.exe"
```

Compare the result with **SHA256SUMS.txt from the same release**.

Windows packages use a compiled native core and obfuscated first-party JavaScript. This deters casual inspection; it is not irreversible encryption or a guarantee against reverse engineering. Third-party software retains its own licenses.

The Windows executables are currently **not Authenticode-signed**. Stable release status does not mean publisher signing is available. Current Android APKs retain their existing testing signing identity; production signing changes must preserve update compatibility.

## Feedback

Report reproducible bugs in [Issues](https://github.com/soulofswords/Sakura-Downloads/issues) or join [Sakura Discord](https://discord.gg/kgxeMRFWDw). Include your edition/version, model format, hardware and reproduction steps. Review recordings and logs before sharing them; never post API keys, passwords or pairing codes.
