# Sakura beta — 15 October 2026

Updated protected Windows installers for Sakura Companion and Sakura VTuber, plus Android 0.2.3 APKs for Sakura Mobile and Sakura VTuber Mobile. No character models, user settings, conversation history, keys, pairing credentials or personal artwork are included.

## Companion and AI changes

- Cloud provider selection now supports Gemini, OpenAI, Anthropic, OpenRouter, Groq, xAI, DeepSeek and compatible endpoints. Recognizable key prefixes can select a provider; ambiguous keys need a manual choice. A custom endpoint must be explicitly configured. Keys are not trial-sent to multiple providers.
- Local mode disables saved cloud fallback on startup. Local screen/camera images are never sent to Gemini as an inference-error fallback. Game mode preserves the selected provider, model and context instead of forcing a different Qwen model.
- Built-in timers, alarms and current-time replies understand more natural spoken requests. Timers and alarms persist across app restarts; keep Sakura open and the PC awake for timely alerts.
- Stronger checks for looping passages, repeated introductions, unrelated appearance flattery and incomplete output. Hindi replies have a larger local generation allowance. Invalid retries produce an error rather than spoken canned filler or a saved failed answer.
- Hindi/Hinglish voices select Hindi microphone recognition instead of guessing the language. Uploaded microphone audio is resampled to 16 kHz. Computer/game audio retains automatic language detection.
- Optional Companion camera viewing supports questions about visible objects, with a separate option for occasional reactions. Camera viewing is off by default and is separate from face tracking.
- A rolling ten-minute screen timeline provides sampled earlier observations for questions about a video after the current scene changes. Timeline notes stay in RAM, expire, and clear with Clear memory or app exit. This is not complete video memory or continuous video inference.
- A separate saved VTuber name is used for AI VTuber chat and gameplay comments. Assistant name and wake phrase remain separate. Avatar self-presentation supports Auto, Feminine, Masculine and Neutral, including Hindi self-reference.

## Animation, game and window changes

- Explicit hand-showing commands present both hands in front with bent elbows and open palms; left/right requests use the character's own side. Requires a rigged PMX/VRM avatar; it does not override webcam tracking or invent unprovided Live2D arm motions.
- Clearly classified game wins can trigger a brief celebration jump, and losses a short head-down reaction. Result watching is separate from normal comment cooldowns, and repeated result screens are suppressed. Character physics continues during motion.
- Repeated Companion minimize clicks stay in compact mode instead of creating a tiny native Windows title bar. Compact mode defaults to the usable bottom-right corner and remembers a dragged/resized placement.
- Relaunching brings the existing window forward. Rendering/startup handling, model repair persistence and controls also received updates.

## Android 0.2.3

- **Sakura Mobile:** Companion camera sharing is separate from Start camera tracking. Pairing alone does not enable tracking. Camera and tracking uses are mutually exclusive and stop when the app goes into the background.
- Both mobile products retain their existing names, package IDs and testing signing key. Front/rear camera selection, expressions, pairing and remembered-device controls remain available.
- Companion camera images are sent only through an authenticated, paired LAN connection, are size-limited, and expire quickly on the PC. The standalone VTuber PC product rejects Companion camera-image requests.

## Verification and limits

Automated checks cover provider routing, local-only vision, timers, Hindi microphone routing, response quality checks, screen timeline, phone pairing/camera endpoint isolation, game transitions, PMX/VRM gesture geometry, result suppression, window placement and packaged product isolation. Release packaging verifies the compiled native core, obfuscated first-party JavaScript, extracted file hashes and empty model libraries. Android checks cover compilation, APK archive integrity and signature verification.

The installed local vision model recognized synthetic VICTORY and DEFEAT result screens. Live Valorant capture, short-banner timing, driver-dependent flicker and the new physical phone-camera path still need tester verification. Screen sampling and AI inference can miss events. Qwen 2B remains limited for nuanced Hindi; 4B was clearer in spot checks but can still answer incorrectly.

Windows installers are not Authenticode-signed. APKs are signed with a testing key. Compilation and obfuscation are not irreversible encryption. No updated macOS package is included.

Install each matching product update over its existing folder to preserve settings and artwork. Keep Companion and VTuber in separate folders. Update both the PC app and matching phone APK for the new camera controls.

---

# Windows beta — 2026-10-14

Separate protected installers for Sakura Companion and Sakura VTuber. No character models or personal data are bundled.

Companion includes the latest fixes for rendering during voice initialization, conversation continuity, repeated introductions and unsolicited screen reactions. The speech-loading progress animation is static on native rendering surfaces to reduce repaint pressure.

Verification passed: installer extraction, packaged file checksums, native application imports, product isolation, empty model libraries, and update preservation of settings and artwork. Functional regression checks cover tracking, model switching, physics, expressions, speech and Chat Reader behavior. These checks do not guarantee the absence of intermittent driver-specific rendering issues.

Install the matching product update into its existing folder. Keep Companion and VTuber installations separate.

The installers are compiled and obfuscated, not Authenticode-signed. macOS packages are not part of this release.
