# Sakura — official downloads

Sakura by **SoulOfSwords** supports PMX, VRM and Live2D avatars on Windows, with a companion Android app for phone tracking and controls.

**Updated: 7 November 2026** · **Latest Companion, VTuber and Mobile release: 2.0**

## Download

- [Sakura Companion 2.0 — Windows x64 installer](https://github.com/soulofswords/Sakura-Downloads/releases/download/v2.0/Sakura-Companion-Setup-Windows-x64.exe)
- [Sakura VTuber 2.0 — Windows x64 installer](https://github.com/soulofswords/Sakura-Downloads/releases/download/v2.0/Sakura-VTuber-Setup-Windows-x64.exe)
- [Sakura Mobile 2.0 — Android APK](https://github.com/soulofswords/Sakura-Downloads/releases/download/v2.0/Sakura-Mobile-Android-2.0.apk)
- [2.0 release notes and checksums](https://github.com/soulofswords/Sakura-Downloads/releases/tag/v2.0)

## What changed in 2.0

- 7 November desktop security refresh fixes the twelve reported memory/parser defects. The refreshed installers include credential admission and redaction repairs, safe fact corrections/retirement, bounded source JSON and character-card parsing, and reduced embedding work. Desktop follow-up conversations and stop/wait interruption fixes are also included.

- 6 November desktop refresh includes PMX/VRM Model Settings recovery at full browser storage, cursor gaze relative to the avatar and current window, and a red halo for enabled microphone controls.
- Companion adds pronunciation rules, per-avatar emotion/motion banks, optional dialogue roles and coaching, reviewed MQTT actions, and manually marked furniture and walking routes in imported PMX rooms. Capabilities depend on configured models, speech engines and hardware.
- The signed-in cloud model browser retains nested folders and rotating PMX previews. Grok–Ms.Ani is available under random model.

- 4 November audited installer refresh: game-first 2B startup with VRAM checks, a persistent Voice matching On/Off switch, and Companion Teacher task controls with reviewed task-webpage interaction.
- Closed task webpages clear stale controls. Release packaging excludes development-only scripts and checks for source changes during the build. Both Windows installers are verified before replacing the 2.0 downloads.

- Companion installer now included: Companion chat, tracking mode and Agent workspace in one edition.
- Voice & speech has optional enrolment for up to five locally encrypted speaker profiles, including Rename and Remove. Voice matching is experimental; it is not identity authentication.
- Shared microphone controls, compact transparency shortcut, and return to the previous compact/full layout after Agent mode.
- Manual localhost pages open inside the Agent Browser even after a task completes.
- Wake-phrase setting is enabled for fresh Companion setups; the optional offline wake pack is still required. Existing saved preferences are respected.

- PMX transparent-fragment depth handling, addressing clothing holes caused by invisible fragments hiding visible material.
- Tracking/retargeting and cursor/model-control improvements.
- Live2D loading under a restricted JavaScript environment, plus expression-import validation for malformed optional metadata.
- Simultaneous YouTube + Twitch support in the Chat Reader, with separate source identities.
- Updated phone UI, tracking controls and connection functionality.
- Local-server Host validation now covers model/audio assets and pages as well as APIs.
- VTuber and Android version labels now show **2.0**.

Standalone VTuber provides avatar tracking, customization, streaming output, Chat Reader and voice-changing tools. Companion AI and Agent tasks are separate features of the Companion edition; they are not enabled in standalone VTuber.

## Audit status and remaining limits

The twelve memory/parser findings are fixed in the 7 November Windows refresh. The audit reproductions are enforced during builds, and both extracted installers check the compiled memory code. Earlier deleted or incorrectly merged facts cannot be recovered automatically. Use dedicated settings fields for credentials. Physical microphone, camera, phone and mixed-DPI behavior still need hardware testing. See the release notes and checksums for the exact refreshed downloads.

## Before installing

No personal character models or imported RVC voice weights are bundled. Import your own permitted files or use the authenticated cloud library. Accounts, MCP connections, owner cloud-storage sessions, API keys and conversations are not distributed with the installer.

Windows x64 is required for this installer. Android requires Android 9+ and a current Android System WebView. Windows is unsigned, and the APK uses the existing local testing signing identity; the **release is not marked as a prerelease**, but those signing limits remain. Hardware support and frame rate depend on your camera, phone, GPU and model. A Mac installer is not included.

The app uses a local server for its desktop interface. A localhost address is a local component of the installed app, not a public hosted service.

## Guides and support

[Existing illustrated guides](https://github.com/soulofswords/Sakura-Downloads/releases/tag/v1.0.2) cover the previous release; some controls have changed in 2.0. See the current release notes for the changes.

Report reproducible issues through [GitHub Issues](https://github.com/soulofswords/Sakura-Downloads/issues) or [Discord](https://discord.gg/kgxeMRFWDw). Include the edition, version, hardware, model format and reproduction steps. Review logs before sharing; never post account tokens or passwords.

This repository contains release artifacts and documentation. Shared application source is maintained separately; this update does not publish Companion source or claim that the public VTuber source separation is complete.
