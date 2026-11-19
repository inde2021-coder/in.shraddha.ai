# SHRADDHA AI v0.15.0 — Secure Device Approval & Gateway Hardening

## Implemented in source
- Added a server-mediated remote-control request/approval flow. The receiving device must have its remote-control consent enabled and explicitly approve each request.
- Remote-control grants are scoped to the requesting paired device and expire after at most five minutes.
- Turning off remote-control sharing revokes all active control grants on that device.
- Added Android UI for requesting control and approving/denying incoming requests.
- Added gateway authentication as mandatory for all AI/provider routes. A missing server token now denies access rather than silently leaving AI routes public.
- Added a shared per-IP AI gateway rate limit (30 requests / 10 minutes); the stricter Council-specific limit remains in place.
- Added 45-second provider request timeouts.
- Malformed JSON now returns HTTP 400 and oversized request bodies return HTTP 413.
- Capability inventory text now reflects time-limited per-session remote-control approval.

## Not claimed as complete
- Remote control still requires both devices paired, connected, the Android accessibility service enabled on the receiving phone, and a deployed HTTPS/WSS relay.
- A physical-device end-to-end test has not been run in this environment.
- No APK is included; Android Gradle build still needs a working Gradle distribution and Android SDK environment.
- Face/voice biometric identification, offline LLM runtime, fully merged Lia/MYRA runtime, signed plugin marketplace, creator generation backends, predictive automation and smart-home integrations remain incomplete and are not represented as working features.
