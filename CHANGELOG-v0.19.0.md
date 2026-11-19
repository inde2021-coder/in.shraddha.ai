# v0.19.0 — LIA + MYRA Integration
- Merged LIA Android main + direct source trees into the single SHRADDHA `:app` source set.
- Renamed the LIA launcher activity to `com.Lia.assistant.MainActivity (internal Activity)`; SHRADDHA remains the only launcher/application ID.
- Added Compose compiler plugin and required Compose, Navigation, DataStore, WebKit and SplashScreen dependencies.
- Merged LIA foreground voice service, Accessibility service and share intents into SHRADDHA manifest.
- Added SHRADDHA home entry for the integrated LIA voice experience and MYRA PC Command Center.
- Kept MYRA Windows/Linux/Python/Node systems as the paired desktop companion under `desktop-companion/`.
- Removed duplicate upstream app trees from `upstream-source` to avoid presenting LIA/MYRA as separate mobile apps.
- Added Hindi integration and setup docs.
