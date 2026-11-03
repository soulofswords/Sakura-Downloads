# Sakura VTuber + Mobile 2.0

3 November 2026. A stable GitHub release containing the standalone Windows VTuber installer and Sakura Mobile Android APK. No Companion installer is included.

## Changes

- PMX alpha-test uniform synchronization prevents zero-alpha fragments writing invisible depth over other clothing materials, including cloned materials and later threshold changes.
- Improved avatar retargeting, model controls and phone tracking integration.
- Live2D runtime compatibility and robust expression discovery: malformed model, VTube Studio and CDI/expression JSON is rejected or skipped without crashing valid expressions.
- YouTube and Twitch can run together in Chat Reader, with distinct message IDs/source labels and per-source connection state.
- Updated Mobile UI, phone controls and connections. Android versionName is 2.0, versionCode 41.
- Loopback Host validation protects static pages, model files and generated audio as well as API routes.
- VTuber product metadata, installer assembly version and Windows uninstall registration are stamped 2.0. Companion version defaults are unchanged.

## Verification

The final pre-browser-routing Python suite passed 1,814 tests (2 skipped; 253 subtests). Installer build gates include real WebGL PMX alpha/depth checks, model controls, phone-link checks and edition isolation. The installer is extracted and its packaged backend exercised before publication. Mobile passed Java compilation, R8 processing, APK signature verification and archive integrity checks.

Python and Node dependency audits reported no known advisories in the scanned environments. This does not guarantee that no vulnerabilities remain.

## Limits

No personal avatars, RVC weights, owner credentials, Google/MCP connections, Jio sessions or conversations are bundled. Optional voice/tracking/chat functionality still requires the relevant assets, hardware or account. No claim of universal 60 FPS, perfect PMX Editor parity or a physical-device regression test is made.

Windows remains unsigned. Android retains the previous local testing signing identity for compatible updates; it is not a newly provisioned production signing identity. No macOS installer or public Companion source is included. The shared implementation remains private pending a separate VTuber source export.

Check SHA256SUMS.txt before installing. Older Companion downloads remain available under v1.0.2.
