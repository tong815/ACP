# ACP 1.0 Implementation Report

ACP Version: 1.0

Last Updated: 2026-07-08

## Why ACP 1.0 Exists

ACP 1.0 establishes a public, reusable collaboration protocol for repositories that need durable AI handoff context. Its main promise is that Repository state and Metadata, not previous conversation, are enough for a new AI collaborator to continue work responsibly.

## Major Design Principles

- Model-independent roles replace product-specific assumptions.
- Semantic Agent owns meaning, reasoning, concepts, dependencies, and Knowledge Model design.
- Implementation Agent owns repository edits, validation, serialization, Metadata maintenance, and reporting.
- Metadata belongs to the Repository and must remain current across collaborators.
- Existing Concept IDs and reusable semantic structures must be preserved.

## Files Changed

- Added `README.md` as the public entry point for ACP 1.0.
- Moved `protocol.md` to `co-ai/protocol.md`.
- Moved `workflow.md` to `co-ai/workflow.md`.
- Moved `metadata-spec.md` to `co-ai/metadata-spec.md`.
- Renamed `chatgpt-rules.md` to `co-ai/semantic-agent-rules.md`.
- Renamed `codex-rules.md` to `co-ai/implementation-agent-rules.md`.
- Updated `implementation-report.md` with release-polish validation details.
- Kept the small example README files under `examples/`.

## Structure Decision

ACP 1.0 uses Option A: protocol files live inside `co-ai/`. In this repository, `co-ai/` is the source template that should be copied into future repositories adopting ACP.

The repository root now contains the public README, implementation report, examples, and the `co-ai/` protocol template.

## Breaking Changes From Previous Draft

- ChatGPT and Codex are no longer protocol roles.
- ChatGPT is now treated as one possible Semantic Agent.
- Codex is now treated as one possible Implementation Agent.
- Workflow now centers Repository, Metadata, Knowledge Model, and explicit validation.
- Metadata specification now includes ownership responsibilities.
- Role-specific file names are now model-independent.

## Future Compatibility

ACP 1.0 can be used with future AI tools because it defines responsibilities rather than vendor-specific behavior. Repositories can adopt new Semantic Agents or Implementation Agents while preserving the same `co-ai/` and `co-project/` structure.

## Validation Performed

- Confirmed Markdown files are split into readable headings, paragraphs, bullet lists, tables, and fenced code blocks.
- Confirmed ACP protocol files consistently include `ACP Version: 1.0` and `Last Updated: 2026-07-08`.
- Confirmed internal references use final paths and file names under `co-ai/`.
- Checked for legacy file references to `chatgpt-rules.md` and `codex-rules.md`.
- Checked for JSON examples; none are included in this repository.

## Known Risks

- Existing adopters of the previous draft may need to update references from root-level protocol files to the new `co-ai/` paths.
