# Windows beta — 2026-10-14

Separate protected installers for Sakura Companion and Sakura VTuber. No character models or personal data are bundled.

Companion includes the latest fixes for rendering during voice initialization, conversation continuity, repeated introductions and unsolicited screen reactions. The speech-loading progress animation is static on native rendering surfaces to reduce repaint pressure.

Verification passed: installer extraction, packaged file checksums, native application imports, product isolation, empty model libraries, and update preservation of settings and artwork. Functional regression checks cover tracking, model switching, physics, expressions, speech and Chat Reader behavior. These checks do not guarantee the absence of intermittent driver-specific rendering issues.

Install the matching product update into its existing folder. Keep Companion and VTuber installations separate.

The installers are compiled and obfuscated, not Authenticode-signed. macOS packages are not part of this release.
