# SHRADDHA AI v0.14.0 — Live Multi-Provider Council

## Implemented in source
- Added authenticated `POST /api/agents/council` backend endpoint.
- Runs five independent roles (Planner, Researcher, Specialist, Critic, Verifier) across 2–5 selected configured providers in parallel.
- Adds a council-chair synthesis step; preserves individual role outputs and provider failures rather than hiding disagreements.
- Enforces a configured `GATEWAY_TOKEN` for the council endpoint, validates provider names and goal size, applies a per-IP six-call/10-minute council limit, and limits provider fan-out to five role calls plus one synthesis call.
- Added Android Future Intelligence UI to call the HTTPS endpoint, display synthesis and individual role outputs, and write metadata-only local audit events.
- Kept local offline council plan as a separate feature and labelled it accurately.
- Bumped Android version to 0.14.0 (versionCode 16) and backend package version to 0.9.0.

## Setup
- Deploy `backend/` with Node.js 20+.
- Set `GATEWAY_TOKEN` and at least two provider API keys (for example `GEMINI_API_KEY`, `OPENAI_API_KEY`) in the backend environment.
- In the app's Future Intelligence page, enter the HTTPS backend URL, same gateway token, two or more configured provider IDs, and a goal.
- Provider calls may incur charges and are subject to provider quotas. The council returns advice only; it does not execute phone, PC, payment, messaging or deletion actions.

## Verification limits
- Node syntax and endpoint contract tests are run for this source package.
- A live provider round-trip requires real provider keys and network access and is not claimed unless separately tested.
- Full Android APK build/device test requires Gradle dependencies and a physical/emulated Android device.
