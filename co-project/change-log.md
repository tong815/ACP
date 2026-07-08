# ACP Change Log

ACP Version: 1.0.1

Last Updated: 2026-07-08

## 2026-07-08 - ACP 1.0.1 external-reference clarification

- Added the external-reference principle.
- Clarified that the ACP repository is the single source of truth for collaboration protocol.
- Clarified that ACP owns `co-ai/`.
- Clarified that normal project repositories own `co-project/` and should reference ACP externally.
- Clarified that normal projects no longer need local `co-ai/` copies by default.
- Updated README adoption guidance to show a normal project structure without `co-ai/`.
- Updated workflow phases to start with reading the ACP repository.
- Updated project metadata to record ACP 1.0.1 as a patch-level clarification.
- No redesign of the core protocol was performed.

## 2026-07-08 - ACP self-management milestone

- ACP became its own first ACP-managed repository.
- Added `co-project/` metadata describing the ACP repository itself.
- Added `co-project/architecture.md` to document the current repository architecture.
- Migrated repository metadata into `co-project/` and removed old project-specific state from active metadata.
- Recorded ACP 1.0 as the current phase and Stable as the current status.
- Aligned metadata with the current `co-ai/` reusable protocol template.
- Confirmed `examples/` references are intentional adoption examples, not ACP project identity.
- Repository structure aligned with ACP philosophy: reusable protocol in `co-ai/`, project metadata in `co-project/`, examples in `examples/`, and public orientation in `README.md`.

## 2026-07-08 - ACP 1.0 release polish

- Added root `README.md` as the public entry point.
- Moved reusable protocol files into `co-ai/`.
- Renamed role-specific files to model-independent names:
  - `co-ai/semantic-agent-rules.md`
  - `co-ai/implementation-agent-rules.md`
- Kept ChatGPT and Codex only as compatibility examples.

## 2026-07-08 - ACP 1.0 release

- Created ACP Version 1.0.
- Generalized protocol language around Semantic Agent and Implementation Agent roles.
- Added metadata ownership guidance.
- Added small example `co-project` layouts under `examples/`.
