# SHRADDHA AI v0.18.0 — Universal App Operator & Learning Lab

## Added in this source update
- Per-app training profiles keyed by Android package name.
- Semantic anchors for buttons, fields, labels, menus, tabs and upload controls using resource ID, visible text, content description and widget class.
- Confidence-scored UI matching; ambiguous/low-confidence targets stop rather than tapping guessed coordinates.
- Workflow authoring with reusable variable keys, expected visible result checks and per-step screen re-observation.
- Adaptive workflow runner that resolves targets again on each screen and verifies after every action.
- File access panel for user-granted folders using Android Storage Access Framework persisted URI grants.
- Exact filename search in MediaStore and user-granted document trees; duplicate matches are reported as ambiguous.
- SELECT_FILE workflow step that can choose a named file from supported Android system picker screens when the target app exposes the filename to Accessibility.
- Central safety policy blocks password/OTP/PIN/CVV/recovery phrase automation and requires approval for destructive/external actions.
- Operator workflow audit metadata; no screenshots, passwords, file contents or biometrics are logged.
- Hindi speech-recognition command input and local natural-language routing to a previously taught workflow.
- Operator console links to Training Lab, File Access and saved workflow execution.
- Version code 19 / version name 0.18.0.

## Existing project capabilities retained
- Gemini/OpenAI/Claude/Groq/Perplexity provider configuration and multi-agent council scaffolding.
- Firebase Auth/Firestore/Storage integration points, encrypted local vault, accessibility service, screen sharing, remote camera consent service, paired-device relay, keyboard, overlay, reminders, engineering calculators and expert workspaces.

## Important boundaries
- This is semantic workflow learning, not model fine-tuning. It stores app-specific anchors and user-authored recipes.
- It does not guarantee every third-party app can be controlled. Apps may hide accessibility nodes, use custom canvases, block automation, require captchas/biometrics, or change UI.
- File lookup is limited to MediaStore items allowed by Android permissions and folders the user explicitly grants through the system folder picker. Android scoped storage is not bypassed.
- File selection in a third-party app works only when its Android picker exposes the named file to Accessibility. Some pickers/apps will require a manual step or cannot be automated.
- No payment, purchase, public post, destructive delete, OTP, PIN, password, CVV or recovery phrase is executed by this runner.
- A configured AI provider can help interpret requests, but the current local workflow runner executes saved recipes; it is not an unrestricted autonomous planner for arbitrary unseen tasks.
