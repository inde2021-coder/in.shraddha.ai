# v0.17.0 Integration and Build Truth

This release is a consolidated source bundle based on the v0.16.0 primary project. It preserves the complete supplied upstream sources for Shraddha v0.8.3, Lia AI and MYRA ULTRA alongside the existing staged integration trees.

## Source layout
- `app/`, `backend/`, `firebase/`: primary Shraddha Android/backend/Firebase source.
- `integrations/lia-ai-source/`, `integrations/lia-android-source/`: Lia integration snapshots carried in v0.16.
- `companions/myra-desktop-source/`, `desktop-companion/`: MYRA/desktop companion snapshots carried in v0.16.
- `upstream-source/lia/`: complete supplied `lia-ai-master(1).zip` source tree, preserved without claiming a full package merge.
- `upstream-source/myra/`: complete supplied `myra-ultra-main.zip` source tree.
- `upstream-source/shraddha-v0.8.3/`: earlier Shraddha Android source baseline.
- `docs/MASTER-FEATURE-LEDGER-v0.17.0.md`: 55-feature inventory, advanced features and Sonic-style capability acceptance gates.

## What is not claimed
- The Lia and MYRA upstream projects are not merged into one Android APK. Their package names, UI frameworks, build configurations and desktop OS APIs differ.
- No Sonic proprietary model is included. Streaming speech-to-speech requires a selected provider, credentials, network and supported SDK/API.
- Face/voice biometric matching is not activated.
- Offline model inference, true video rendering, full CAD, isolated plugin execution, smart-home physical control and live screen streaming are not complete solely by including source code or a capability entry.
- A successful ZIP integrity check is not an Android APK build or end-to-end device test.

## Build requirements
Use Android Studio with a compatible JDK/Gradle installation and network access for dependencies. Configure Firebase only for cloud features. Configure provider API keys on the backend, never in the APK. Install and pair the relevant desktop companion on each target PC before remote operations.

## Safety
All remote actions must be authenticated, scoped, time-limited, visible to the user and revocable. Sensitive actions require explicit confirmation. Biometrics require informed consent and a documented security/privacy review.
