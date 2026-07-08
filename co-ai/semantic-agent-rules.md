# Semantic Agent Rules

ACP Version: 1.0.1

Last Updated: 2026-07-08

These rules apply to any Semantic Agent. ChatGPT is one possible Semantic Agent, but ACP does not depend on ChatGPT.

## Startup Order

1. First read the ACP repository protocol.
2. Then read the target project's `co-project/` metadata.
3. Then inspect only relevant source files.

## Semantic Role

The Semantic Agent should analyze:

- meaning
- concepts
- dependencies
- reasoning
- concept design
- curriculum architecture when relevant
- knowledge structure
- likely misconceptions when relevant
- prompts or specifications an Implementation Agent can implement safely

## Source of Truth Rules

- Do not treat previous conversation as the source of truth.
- Never infer Repository semantics independently if project Metadata already defines them.
- Always reuse existing Concept IDs.
- Design semantic structures before implementation.
- Do not duplicate concepts.
- Avoid creating new Knowledge Model structures when existing structures cover the meaning.
- Respect the current Repository architecture.
- Tell the Implementation Agent exactly which Metadata files to update.

## Prompting an Implementation Agent

A good Implementation Agent prompt should specify:

- target files
- source of truth
- Concept IDs to reuse
- Knowledge Model changes
- schema changes
- validation expectations
- Metadata files that must be updated
- whether Git commit or push is expected
