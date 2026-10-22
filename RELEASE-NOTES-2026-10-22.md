# Sakura update — 22 October 2026

This release includes fresh Windows Companion and VTuber installers and Sakura Mobile 0.3.20. The source remains in the private Sakura repository; this public repository contains release notes and protected downloads.

## Calendar scheduling from chat

- Companion chat can prepare a Google Calendar event from a natural-language request after Google Calendar is connected. Sakura asks for missing times, shows the exact title and time range, and waits for confirmation before saving.
- Fixed title extraction so spoken commands such as “I have an interview, add that to the calendar” create an event titled “Interview” instead of copying the whole instruction into the title. Person/company details in the event subject are kept.
- Sakura confirms a save only after Google Calendar reports success. If a save cannot be confirmed, it tells the user to check Calendar before retrying to avoid duplicates.
- On Mobile, calendar requests prepare a draft in the phone’s Calendar app. Review the draft and tap Save there; Sakura does not claim that it was saved before that confirmation.

## Companion and AI behavior

- Added the Agent workspace to the Companion window with approval before file edits, shell commands, and connected-tool actions. The avatar remains visible while the workspace is open.
- Added Google sign-in for Calendar and approved Drive, Docs, and Sheets actions in Agent mode. Account permissions depend on the scopes the user approves and whether Google OAuth is configured for the build.
- Improved speech-linked facial expressions and gestures, response interruption, clock and PC status responses, web-search confirmation, attachment summaries, and grounding of hardware claims.
- Added show/hide controls for authored Irida wings, horns, and top clothing. Updated relaxed 3D arm poses and maintained the imported greeting animation.

## Sakura Mobile 0.3.20

- Same `app.sakura.mobile` package and signing identity; install over the existing app to retain phone data.
- Updated the calendar title parser and increased version code to 26 / version 0.3.20.
- Includes the combined phone-local assistant, PC connection, model transfer, camera modes, wake phrase, and shared Companion/VTuber features described in earlier release notes.

## Build and verification

- Windows editions passed the configured unit, frontend, installation, settings-preservation, and backend-isolation checks.
- Android Java compilation, R8 processing, APK signature and archive checks passed. The APK remains signed with the local testing key; install it directly rather than through Play Store.
- No new macOS installer is included. Windows installers are unsigned. Character models and personal account data are not bundled.

## Downloads

See the [22 October 2026 release](https://github.com/soulofswords/Sakura-Downloads/releases/tag/windows-beta-2026-10-22) for Sakura Companion, Sakura VTuber, and Sakura Mobile files and SHA-256 checksums.
