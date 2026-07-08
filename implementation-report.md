# ACP 1.0 Implementation Report

ACP Version: 1.0

Last Updated: 2026-07-08

## Why ACP 1.0 Exists

ACP 1.0 establishes a public, reusable collaboration protocol for repositories that need durable AI handoff context. Its main promise is that Repository state, not previous conversation, is enough for a new AI collaborator to continue work responsibly.

## Major Design Principles

- Model-independent roles replace product-specific assumptions.
- Semantic Agent owns meaning, reasoning, concepts, dependencies, and Knowledge Model design.
- Implementation Agent owns repository edits, validation, serialization, Metadata maintenance, and reporting.
- Metadata belongs to the Repository and must remain current across collaborators.
- Existing Concept IDs and reusable semantic structures must be preserved.

## Breaking Changes From Previous Draft

- ChatGPT and Codex are no longer protocol roles.
- ChatGPT is now treated as one possible Semantic Agent.
- Codex is now treated as one possible Implementation Agent.
- Workflow now centers Repository, Metadata, Knowledge Model, and explicit validation.
- Metadata specification now includes ownership responsibilities.

## Future Compatibility

ACP 1.0 can be used with future AI tools because it defines responsibilities rather than vendor-specific behavior. Repositories can adopt new Semantic Agents or Implementation Agents while preserving the same `co-ai/` and `co-project/` structure.

## Validation

- Protocol files were updated with `ACP Version: 1.0`.
- Protocol files were updated with `Last Updated: 2026-07-08`.
- Terminology was aligned around Semantic Agent, Implementation Agent, Knowledge Model, Metadata, and Repository.
- Example `co-project` layouts were added for physics, exam visualizer, and game repositories.
