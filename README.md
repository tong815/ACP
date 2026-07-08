# AI Collaboration Protocol (ACP)

ACP Version: 1.0.1

Last Updated: 2026-07-08

## What ACP Is

AI Collaboration Protocol (ACP) is a reusable collaboration protocol for human and AI work across repositories. It helps any new AI collaborator understand a project from durable repository metadata instead of relying on previous conversations.

ACP is model-independent. A team may use ChatGPT, Codex, or other AI systems, but ACP defines generic responsibilities rather than product-specific behavior.

## Core Idea

Repository state and Metadata are the source of truth.

Previous conversations can provide helpful context, but they are not durable project state. A project using ACP should contain enough current Metadata for a new collaborator to understand the project goal, active files, semantic structure, recent changes, and validation expectations.

## Single Source Of Truth

The ACP repository is the single source of truth for the collaboration protocol.

Projects should reference the ACP repository instead of embedding a local copy of `co-ai/` by default. This keeps protocol changes centralized and avoids protocol drift across repositories.

Protocol repository: https://github.com/tong815/ACP

## Repository Structure

ACP separates reusable protocol rules from project-specific Metadata.

| Location | Owner | Purpose |
|---|---|---|
| ACP repository `co-ai/` | ACP | Reusable collaboration protocol files. |
| Project repository `co-project/` | Project | Project-specific Metadata that describes the current project state. |

In this ACP repository, `co-ai/` is the protocol source. Normal project repositories should not include `co-ai/` unless there is a deliberate reason to vendor or pin a local copy.

## Recommended Project Structure

```text
Project/
|-- co-project/
|-- src/ or data/
`-- ...
```

A normal ACP-managed project keeps its own `co-project/` metadata and references the ACP repository externally for protocol rules.

## Agent Roles

### Semantic Agent

The Semantic Agent owns semantic analysis, reasoning, dependency analysis, curriculum architecture when relevant, concept design, and Knowledge Model structure.

ChatGPT may be used as a Semantic Agent, but ACP itself does not require ChatGPT.

### Implementation Agent

The Implementation Agent owns implementation, repository updates, validation, Metadata maintenance, serialization, and code generation.

Codex may be used as an Implementation Agent, but ACP itself does not require Codex.

## How To Adopt ACP

1. Reference the ACP protocol repository: https://github.com/tong815/ACP
2. Create a `co-project/` folder in the target project repository.
3. Add the required Metadata files listed below.
4. Fill the Metadata with the current project state before asking an AI collaborator to make changes.
5. Ask AI collaborators to read the ACP repository first, then the project's `co-project/`, then only the source files relevant to the task.
6. After meaningful architecture, content, behavior, or workflow changes, update `co-project/` before committing.

## Required `co-project/` Metadata Files

| File | Owner | Purpose |
|---|---|---|
| `co-project/context-header.md` | Human + Semantic Agent | Short current orientation for AI collaborators. |
| `co-project/project-state.json` | Implementation Agent | Machine-readable current project state. |
| `co-project/project-map.json` | Semantic Agent design + Implementation Agent serialization | Machine-readable structure and concept map summary. |
| `co-project/change-log.md` | Implementation Agent | Reverse chronological record of implementation and Metadata changes. |
| `co-project/implementation-report.md` | Implementation Agent | Latest implementation summary and validation report. |

## ACP Repository Files

| File | Purpose |
|---|---|
| `co-ai/protocol.md` | Core ACP mission, scope, roles, and operating rules. |
| `co-ai/workflow.md` | General collaboration workflow and example workflow. |
| `co-ai/metadata-spec.md` | Required project Metadata files and ownership responsibilities. |
| `co-ai/semantic-agent-rules.md` | Rules for Semantic Agents. |
| `co-ai/implementation-agent-rules.md` | Rules for Implementation Agents. |
| `co-project/` | ACP's own project Metadata, because ACP is self-managed using ACP. |

## Release Status

ACP 1.0.1 is a patch-level clarification of ACP 1.0. It adds the external-reference model without redesigning the core protocol.
