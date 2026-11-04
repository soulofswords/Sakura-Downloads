# Sakura Companion, VTuber and Mobile 2.0

Updated 4 November 2026. Stable release; Companion now joins the existing VTuber installer and Mobile APK under the same 2.0 release.

## Companion additions and fixes

- Audited Windows rebuild: startup checks for games already running, including background games in recognised installation folders, before local-model warmup. It selects the game model (Qwen3-VL 2B by default), checks VRAM headroom, and uses the saved cloud fallback when enabled and available. Otherwise local AI pauses while the app remains open. The universal model preference is preserved.
- Voice & speech → Recognised voices now has a persistent **Voice matching On/Off** switch. Turning it off keeps saved profiles and does not change the microphone or wake-phrase switches.
- Teacher chat can select, inspect, pause/resume, cancel and confirm deletion of existing Agent tasks. Deletion removes task/history records, not workspace files. Task pages can be inspected with screenshots and used through reviewed click/fill/scroll/drag tools; servers must be running. Browser sessions are isolated, and private-network/secret-field restrictions remain in place.
- Closed task pages hide stale screenshots and controls. Game settings/status now name the actual game profile.
- Packaging excludes development-only probe/patch scripts, retains verification reports, and checks that sources do not change during the build. The refreshed Windows assets are extracted and checked before upload; user models, voices and owner sessions remain excluded.

- Companion installer refreshed on 4 November: selecting Full access and running tasks under it no longer shows duplicate Windows confirmation dialogs. Full access remains session-only and keeps workspace validation.
- Clean-checkout GitHub Actions packaging checks no longer require downloaded speech weights or compiled camera DLLs; actual installer builds still verify both.

- Voice & speech → Recognised voices: record a short sentence, save up to five named voice profiles, rename profiles and remove them. The optional CPU recognition runtime is a separate download. Enrolled profiles filter browser microphone transcription and native wake commands; similarity is experimental and cannot prove identity. No speaker recordings or profiles are bundled.
- The compact mic, chat mic and main listening control share one state. Turning off wake listening does not start continuous recording. Changing window size no longer stops an active conversation.
- Agent mode returns to the compact/full Companion layout it was opened from. Maximise remains available for full-window mode.
- Compact opaque mode has a round transparency shortcut beside the microphone.
- Manual localhost links can display in the in-app Browser with completed tasks or without a task. The local server must still be running and permit framing. Public-site automation keeps its existing approval rules.
- Fresh Companion setups enable the wake-phrase preference. The optional offline wake pack must be installed; existing saved choices are kept.
- The optional speaker runtime uses updated CPU dependencies and tensor-only checkpoint loading.

## Existing VTuber and Mobile changes

PMX transparent-fragment depth fixes, tracking and model controls, Live2D compatibility and malformed-expression validation, simultaneous YouTube + Twitch Chat Reader, phone UI and connection updates, and loopback Host validation. Standalone VTuber keeps tracking, Chat Reader and voice changing; Companion AI and Agent tasks belong to Companion.

## Verification and limits

Windows packages are checked by extraction, clean install/upgrade and packaged backend checks. This refresh retains the existing 2.0 Mobile APK without rebuilding Android. The published checksums identify the exact downloads. A dependency scan found no known advisories in the scanned installed Python environment; this is not a guarantee of no vulnerabilities.

The Python audit run passed 1,860 tests with two skipped and 253 subtests. The Windows release gates additionally cover browser controls, PMX/Live2D rendering, phone permissions, microphone routing, approval handling and edition isolation.

No personal avatars, RVC weights, API keys, owner Jio sessions, MCP connections or conversations are included. Windows installers are unsigned. Mobile keeps the existing testing signing identity for updates. Physical phone/camera and real-voice recognition still require testing on the user's hardware. No macOS installer is included. Companion source remains private. Weight-space programming is excluded from this update.
