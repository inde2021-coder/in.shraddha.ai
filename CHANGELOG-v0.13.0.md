# SHRADDHA AI v0.13.0 — Local Intelligence Workbench

## Added
- Multi-Agent Council Planner: transparent five-role planning board (Planner, Researcher, Specialist, Critic, Verifier). It is a local plan generator, not a live multi-model agent runtime.
- Local Project Workspace: create/replace a project plan, persist milestones on-device, mark the next milestone complete, and view progress.
- Personal Knowledge Graph starter: explicitly save user-entered memory nodes and search labels/categories/notes locally. No automatic biometric or sensitive inference.
- Capability catalog now distinguishes these implemented local tools from their still-unbuilt cloud/automation extensions.

## Safety and scope
- Project tracking does not execute tasks in the background.
- Council planning does not contact external AI providers.
- Knowledge memory is explicit and local; relationship extraction, semantic indexing and automatic identity matching are not implemented.
- Existing permissions, provider setup and desktop companion requirements remain.
