# AI Collaboration Protocol

ACP Version: 1.0

Last Updated: 2026-07-08

## Mission Statement

Repository state should be sufficient for any new AI collaborator to continue work without relying on previous conversations.

## Protocol Scope

ACP is a reusable collaboration protocol for any repository that needs humans and AI agents to share durable project context. It defines the separation between universal collaboration rules in `co-ai/` and project-specific working knowledge in `co-project/`.

ACP is model-independent. A repository may use ChatGPT, Codex, or other tools, but the protocol defines generic roles instead of depending on any single product.

## Agent Roles

### Human

The Human sets goals, constraints, priorities, and acceptance criteria.

### Semantic Agent

The Semantic Agent owns semantic analysis, curriculum architecture, dependency analysis, reasoning, concept design, and Knowledge Model design.

ChatGPT is one possible Semantic Agent when it is useful to name a concrete example.

### Implementation Agent

The Implementation Agent owns implementation, repository updates, validation, Metadata maintenance, serialization, and code generation.

Codex is one possible Implementation Agent when it is useful to name a concrete example.

## Semantic Ownership

- Semantic structures belong to the Semantic Agent.
- Implementation belongs to the Implementation Agent.
- Metadata belongs to the Repository.
- The Repository is the source of truth for current project state.
- The Knowledge Model connects semantic design to implementation work.

## Universal vs Project-Specific Separation

| Folder | Purpose |
|---|---|
| `co-ai/` | Reusable ACP protocol files shared across repositories. |
| `co-project/` | Repository-specific Metadata, project state, maps, reports, and history. |

## Core Principles

- Repository state is the source of truth.
- Code is for computers. Metadata is for AI collaborators.
- AI collaborators read Metadata before source code.
- Structured Metadata is the communication layer between AI agents.
- Knowledge Model before implementation.
- Every meaningful implementation must update Metadata.
- New collaborators should be able to continue from Repository state alone.

## Operating Rule

AI collaborators must not treat previous conversation as the source of truth. The Repository and its Metadata files define the current project state.

## Standard Startup Order

1. Read the universal protocol in `co-ai/`.
2. Read project Metadata in `co-project/`.
3. Inspect only the source files relevant to the current task.
4. Preserve existing Concept IDs and Knowledge Model structure.
5. Implement the requested change.
6. Validate the change.
7. Update project Metadata.
8. Commit and report results when requested.
