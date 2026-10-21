# Sakura Windows Beta — 21 October 2026

New Windows x64 installers for **Sakura Companion** and **Sakura VTuber**. This is a new dated release; the previous release remains available. This release updates the PC applications only. It does not include a newly built Android APK or macOS installer.

## Rendering, model controls and appearance

- Added frame protection during Companion resize/quality changes and final model preparation, plus GPU preparation checks when switching models. These address paths that could reveal a blank or incomplete canvas.
- Bounded animation/physics time steps after a delayed frame to reduce sudden bone jumps, particularly in VRM speech/animation.
- Updated block-style model-switch transitions, material transparency handling, Taffy front-hair rendering, clothing-bone safeguards and saved bone controls.
- Updated Companion and VTuber branding, including app/taskbar artwork and mode-specific logos.

## Companion conversation and speech

- Added checks against invented personal backstories and unsupported claims that a topic was discussed earlier. Repetitive or evasive replies receive one bounded retry, including near-identical answers across turns.
- Chats now last for the current app session and clear when Sakura exits. Model settings and imported artwork are separate from conversation history.
- Simplified Hindi instructions, added Hindi/Romanized Hindi common-question handling, and linked Hindi/Hinglish voice selection to Hindi microphone recognition. English microphone input uses an explicit English recognition hint.
- Improved short-command recognition with the base Whisper model and command/location vocabulary; uncertain short fragments and silence are rejected instead of being treated as reliable speech.
- Improved speech text cleanup so emoji, stage directions and formatting are not read as ordinary dialogue. Kokoro voices remain bundled for offline speech.
- Added a retargeted greeting animation, speech-linked gestures and recorded laughter for supported 3D avatars. Live2D movement remains limited by the parameters authored into each model.

## Commands and video/audio context

- Timer and alarm confirmations no longer speak internal IDs; internal timer management remains available.
- Improved command routing for app opening, clocks, timers, alarms, current weather and location/topic news. News speech avoids reading source URLs and raw publication metadata aloud; source details remain available in text.
- While screen/game computer-audio context is enabled, automatic microphone commands require the configured wake phrase with the command. Video narration remains observed context for reactions. The explicit microphone button retains its existing behavior.
- Computer-audio prompts explicitly distinguish video/narrator speech from a user request.

## Installation and verification

Choose the installer for your existing product. Install into that product's existing folder to retain settings and imported models; keep Companion and VTuber in separate folders. Character models, user API keys, conversations and imported RVC weights are not bundled. Local AI model weights remain optional downloads.

The release uses a compiled native application core and obfuscated first-party JavaScript. The source repository remains private. This raises the effort required for inspection but does not prevent all reverse engineering. Windows installers are unsigned.

Verification includes Python regression tests, JavaScript regression/syntax checks, real PMX/VRM/Live2D browser rendering/audio checks, and install/update plus extracted-runtime smoke tests for both Windows editions. SHA-256 checksums accompany the downloads.

## Known limits

- The exact intermittent native Qt flicker was not visually reproduced in the final browser checks. Driver/compositor-specific behavior still needs testing on affected PCs; this release does not promise flicker can never occur.
- The installed 4B local model can still produce awkward or irrelevant Hindi in general conversation. Common questions were checked, but prompt changes are not a guarantee of Hindi fluency.
- The microphone guard is not speaker identification: media containing the wake phrase can still trigger recognition. It applies while computer-audio context is enabled.
- Real cloud-provider replies and physical phone/LAN behavior were not revalidated for this PC release.

Feedback: [Sakura Discord](https://discord.gg/kgxeMRFWDw) or [GitHub Issues](https://github.com/soulofswords/Sakura-Downloads/issues).
