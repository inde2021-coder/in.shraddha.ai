# SHRADDHA AI v0.17.0 — Unified Multi-platform Source Bundle

This bundle advances Shraddha AI with an opt-in Firebase encrypted memory vault and includes the Lia Android and MYRA desktop source trees for staged integration.

## What's in this release
- Existing Shraddha Android app and backend.
- Firebase email/password authentication and Firestore encrypted memory backup/restore.
- Firestore owner-only security rules and Firebase setup guide.
- Lia Android source preserved under `integrations/lia-android-source/`.
- MYRA ULTRA desktop/Linux/Termux source preserved under `companions/myra-desktop-source/`.
- Kids Universe and Person Memory features from v0.9.1 remain in the Android project.

## Important implementation truth
Lia and MYRA source is included, not fully merged into the Shraddha APK. Their UI frameworks, packages and operating-system capabilities differ. See `docs/MULTI_PLATFORM-INTEGRATION.md` for exact boundaries. Firebase Cloud Storage uploads and FCM notification handling are not yet wired; only Authentication + encrypted Firestore memory backup/restore are implemented in this version.

## Firebase setup
Follow `firebase/README.md`. Copy `local.properties.example` to `local.properties` in the project root and add the Firebase values from your own Firebase project. Do not upload real `local.properties` to GitHub.

## Build
Open this folder in Android Studio. Gradle dependencies must be downloadable. A Firebase project configuration is required for cloud features; the app can be built without credentials but cloud sync will report that configuration is missing. Build/debug APK and test on a real Android device after granting the relevant permissions.

## Security notes
- Firestore rules restrict each vault to its authenticated owner.
- Memory note content is encrypted client-side with AES-GCM before upload.
- Password loss means the cloud backup cannot be decrypted.
- Face/voice biometric templates, child-care records and provider API keys are not uploaded by this cloud vault.
- App Check, privacy policy, deletion/export flows, rate limiting and a full security review are required before public production release.


## v0.11.0 interface refresh
- Reworked the Android home screen into a premium command-centre layout inspired by Lia's orb/voice presentation and MYRA's multi-tool workspace concept.
- Added a holographic-workspace status panel that clearly says when no active task stream is connected; it does not fabricate screen activity.
- Added unified workspace naming and stronger depth, gradient surfaces, neon edge treatment, clearer status hierarchy and more compact module tiles.
- Existing app pages and actions remain the destinations behind the home tiles.

## Honest integration status
The Lia and MYRA codebases remain preserved companion/source trees and are not yet a single fully merged runtime. The redesigned dashboard is a native Android UI update, not proof that all external capabilities are operational. See docs/FEATURE-MATRIX.md.


## v0.12.0 update
See `docs/FEATURE-COMPLETENESS-AND-ADVANCED-ROADMAP.md` for the capability status registry, workflow safety engine, audit trail, advanced roadmap, and limitations. Roadmap entries are not claimed as implemented.

## v0.13.0 local intelligence additions
The Future Intelligence screen now includes a five-role council planning board, a local project/milestone tracker, and a user-entered searchable knowledge-memory store. These are local planning and record-keeping tools; they do not claim autonomous external execution, live multi-model debate, or automatic biometric identification.


## v0.15.0 live multi-provider council
- Future Intelligence now has a Live Multi-AI Council action that calls `POST /api/agents/council` on the configured HTTPS backend.
- Configure `GATEWAY_TOKEN` and at least two provider keys in the backend environment. The council runs five independent roles across up to five providers, then asks a council chair to reconcile the outputs.
- The endpoint is authenticated and advice-only. It does not execute Android, PC, messaging, payment, or deletion actions. Provider charges and quotas may apply.
- The local five-role plan template remains available offline and is labelled separately.

## v0.16.0 Advanced Feature Pack

The Future Intelligence workspace now includes a 36-area capability map, offline engineering calculators, creator brief templates, editable Digital Twin preferences, opt-in predictive suggestions, plugin manifest/scope validation, device health snapshot, one-shot reminders and user-triggered JSON export of selected app-managed data. The experimental desktop relay bridge is in `companions/shraddha-desktop-bridge/`.

Important: text creator briefs are not rendered media; the offline model helper verifies hashes but does not run inference; the plugin registry validates metadata but does not execute code; face/speaker biometrics and full desktop screen streaming are not shipped. See `docs/VERIFICATION-v0.16.0.md` for tested and unverified behavior.


## v0.17.0 Unified Source Consolidation
- Complete supplied Lia AI upstream source is preserved at `upstream-source/lia/`.
- Complete supplied MYRA ULTRA upstream source is preserved at `upstream-source/myra/`.
- Earlier Shraddha v0.8.3 baseline is preserved at `upstream-source/shraddha-v0.8.3/`.
- The 55-core-feature inventory, later advanced feature requests, Sonic-style voice capabilities and acceptance gates are documented in `docs/MASTER-FEATURE-LEDGER-v0.17.0.md`.
- See `INTEGRATION-AND-BUILD-TRUTH-v0.17.0.md` for exact integration boundaries.

**Important:** This release consolidates and preserves source trees; it does not represent all listed capabilities as production-complete or merged into a single APK. API credentials, model weights, hardware, permissions and separately installed companions are required for relevant features. Android APK build and real-device end-to-end tests must be completed in an Android Studio environment.

## v0.19.0 LIA + MYRA unified integration
See `README-v0.19.0-HI.md`, `docs/integration/LIA-MYRA-FULL-MERGE-v0.19.0-HI.md`, and `desktop-companion/README-SHRADDHA-MYRA-PAIRING-HI.md`.
