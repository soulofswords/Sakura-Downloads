# Sakura beta update — 15 October 2026

Updated Windows Companion/VTuber installers and **Sakura Mobile / Sakura VTuber Mobile 0.3.4** APKs. Install the matching app over its previous version to retain settings; do not uninstall first to preserve phone models. No character models, personal artwork, keys, conversations or imported voice weights are included.

## What changed

- **PC Cloud API checks:** Find available models for the selected provider and test actual chat generation with a small request. Gemini, OpenAI, Claude and compatible cloud routes remain separate. Listing models does not prove quota, image support or voice access. Errors now distinguish permissions, unavailable models, billing/quota and temporary rate limits, with secrets redacted.
- **Independent phone assistant:** Sakura Mobile opens with Connect to PC / Local. Local renders a phone-saved Live2D, PMX or VRM model and uses its saved Gemini/OpenAI API key for online conversation without a connected PC. Local is not an offline phone LLM engine.
- **Guided model transfer:** first-time API setup → PC connection Passed/Failed → automatic PC folder/file picker → verified download and phone loading. PMX/Live2D transfer the whole explicitly selected folder; VRM transfers one file. Saved models instead offer Use model / Add model, with remembered-PC reconnection for additions. At least one model must load before Local chat is enabled.
- **Touch and feedback:** Live2D pinch zoom, one-finger panning, button press animations, sending/preparing indicators and explicit failures. Sent appears only after the phone confirms model storage.
- **Phone controls:** saved chat, Female/Male cloud voice choices, model discovery/API checks, dictation drafts, basic phone assistant actions and permission/confirmation-based ordinary telephone calling with call-time assistant muting. The standalone VTuber Mobile keeps its controller role and has no Local assistant UI.
- **Companion behavior:** Sir/Ma'am/no-title preference, time-based greeting, six distinct 3D dance routines, shared stage-direction/asterisk speech cleanup and experimental short original vocalises. These do not reproduce full named songs.
- **Rendering and colors:** environment wheel updates, guarded rig-diagnostic startup, framebuffer allocation limits, local GPU warmup after initial rendering, and release of unused 3D surfaces during Live2D display.
- **Smaller Windows installers:** solid compression keeps runtime features and excludes personal models/data. Source is private; public builds use native compilation and first-party JavaScript obfuscation, which cannot prevent all reverse engineering.

## Testing and known limits

Cloud-routing/error, pairing/package, Java provider-error, gesture/control and model rendering regression checks passed. Windows installer install/update/payload checks verify both product editions. APK compilation, signing and integrity were checked. Browser tests use mocked native bridges/provider responses; real cloud credit, Android contacts/calls/call-end muting, permissions, camera and LAN behavior still need physical-device/account testing. Driver-specific intermittent rendering issues remain subject to tester verification.

Windows builds are unsigned; publisher metadata does not remove SmartScreen warnings. Android APKs retain their existing package names and local testing signing key. No new protected macOS DMG was built on this Windows host.

This refresh replaces assets on the existing release. Source update: `f019eaf` in the private Sakura repository. See SHA256SUMS.txt for download hashes.
