# SHRADDHA AI v0.19.0 — Unified Android + MYRA PC Companion

यह v0.18.0 का updated source है। Android पर केवल SHRADDHA AI app/launcher है। LIA का Android voice/Compose experience उसी APK में internal Activity के रूप में जोड़ा गया है। MYRA का Windows/Linux companion `desktop-companion/` में है और SHRADDHA के Device Universe से pair किया जाना है।

## मुख्य स्थान
- `app/src/main/java/in/shraddha/ai/` — SHRADDHA core, Universal App Operator, security, Firebase, device link, vision.
- `app/src/main/java/com/Lia/assistant/` — उसी APK में merged LIA voice, Compose UI, live audio, memory/personality, Forge, accessibility agent.
- `desktop-companion/MYRA_ULTRA_APP/` — MYRA Ultra desktop companion, MYRA Coder and Website Forge.
- `docs/integration/LIA-MYRA-FULL-MERGE-v0.19.0-HI.md` — merge ledger and boundaries.
- `desktop-companion/README-SHRADDHA-MYRA-PAIRING-HI.md` — MYRA PC setup.

## Build
Open this project root in Android Studio. Use JDK 17 and Android SDK 35. Allow Gradle to download dependencies, then run `:app:assembleDebug`. Build has not been verified in this execution environment because Gradle distribution download was blocked by DNS/network. Configure Firebase and AI provider keys using the documented local configuration; never commit secrets.

## Required device permissions
Microphone, notifications, Accessibility Service, overlay, camera, and media access are requested only for features that need them. Enable Accessibility manually in Android Settings for cross-app automation. PC control needs a paired MYRA desktop companion.

## Important
Source integration is not a claim that every capability works without credentials, permissions, network, desktop companion, or external provider APIs. See `docs/BUILD-TEST-REPORT-v0.19.0.md` for what was and was not verified.
