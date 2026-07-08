# ACP Implementation Report

ACP Version: 1.0.1

Last Updated: 2026-07-08

## Summary

ACP 1.0.1 adds a patch-level clarification for the external-reference model. ACP remains the single source of truth for collaboration protocol, and normal projects should reference ACP externally while maintaining their own `co-project/` metadata.

No redesign of the core protocol was performed.

## Files Updated

- `README.md`
- `co-ai/protocol.md`
- `co-ai/workflow.md`
- `co-project/architecture.md`
- `co-project/context-header.md`
- `co-project/project-state.json`
- `co-project/project-map.json`
- `co-project/change-log.md`
- `co-project/implementation-report.md`

## Metadata Synchronized

The metadata now records:

- ACP Version: 1.0.1
- Current phase: ACP 1.0.1
- Current status: Stable patch clarification
- External-reference principle added
- ACP repository owns `co-ai/`
- Normal project repositories own `co-project/`
- Normal projects no longer need local `co-ai/` copies by default

## Architecture Verified

ACP itself still contains both `co-ai/` and `co-project/` because it is the protocol source and first self-managed ACP repository.

Normal ACP-managed projects should use this default structure:

```text
Project
|-- co-project/
|-- src/ or data/
`-- ...
```

## Validation Performed

- Confirmed `co-ai/` remains in the ACP repository.
- Confirmed ACP's own `co-project/` remains in the ACP repository.
- Validated `co-project/project-state.json` as JSON.
- Validated `co-project/project-map.json` as JSON.
- Checked that metadata paths reference existing files.
- Checked internal references for the external-reference model and current `co-ai/` file names.
- Confirmed the update is a patch-level clarification, not a protocol redesign.

## Remaining Future Improvements

- Add an adoption template for creating a new project `co-project/` without copying `co-ai/`.
- Add automated Markdown link checking if the documentation set grows.

## Known Risks

- Existing projects that copied `co-ai/` may need manual cleanup or a decision to treat their local copy as an intentional pinned version.
