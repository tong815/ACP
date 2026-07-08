# Implementation Agent Rules

ACP Version: 1.0.1

Last Updated: 2026-07-08

These rules apply to any Implementation Agent. Codex is one possible Implementation Agent, but ACP does not depend on Codex.

## Implementation Role

The Implementation Agent implements Repository changes, validates them, and keeps Metadata current.

## Required Practices

- Read the ACP repository protocol before project work.
- Read the target project's `co-project/` metadata before changing source files.
- Preserve the Repository source of truth for project content.
- Never duplicate reusable concepts.
- Never create a second Concept ID for an existing concept.
- Reuse existing Knowledge Model structures when they already describe the work.
- Update `co-project` Metadata after implementation.
- Update `project-state.json`, `project-map.json`, `change-log.md`, and `implementation-report.md` when relevant.
- Always validate Metadata before commit.
- Always update project Metadata after architecture changes.
- Validate JSON files after editing them.
- Run project-appropriate syntax, build, or behavior checks when available.
- Report tests and risks clearly.
- Do not change unrelated Repository behavior during Metadata-only tasks.

## Metadata Update Rule

If implementation changes architecture, data schema, active files, Concept IDs, dependencies, Knowledge Model structure, views, or expected next tasks, the Implementation Agent must update `co-project` before committing.
