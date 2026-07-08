# AI Collaboration Protocol (ACP)

ACP Version: 1.0

Last Updated: 2026-07-08

## What ACP Is

AI Collaboration Protocol (ACP) is a reusable repository structure for human and AI collaboration. It helps any new AI collaborator understand a project from the repository itself instead of relying on previous conversations.

ACP is model-independent. A team may use ChatGPT, Codex, or other AI systems, but ACP defines generic responsibilities rather than product-specific behavior.

## Core Idea

Repository state and Metadata are the source of truth.

Previous conversations can provide helpful context, but they are not durable project state. A repository using ACP should contain enough current Metadata for a new collaborator to understand the project goal, active files, semantic structure, recent changes, and validation expectations.

## Repository Structure

ACP separates reusable protocol rules from project-specific Metadata.

| Folder | Purpose |
|---|---|
| `co-ai/` | Reusable ACP protocol template copied into repositories that adopt ACP. |
| `co-project/` | Project-specific Metadata that describes the current repository state. |

In this ACP repository, `co-ai/` is the source template. To adopt ACP in another repository, copy this `co-ai/` folder into that repository and create a matching `co-project/` folder for the project Metadata.

## Agent Roles

### Semantic Agent

The Semantic Agent owns semantic analysis, reasoning, dependency analysis, curriculum architecture when relevant, concept design, and Knowledge Model structure.

ChatGPT may be used as a Semantic Agent, but ACP itself does not require ChatGPT.

### Implementation Agent

The Implementation Agent owns implementation, repository updates, validation, Metadata maintenance, serialization, and code generation.

Codex may be used as an Implementation Agent, but ACP itself does not require Codex.

## How To Adopt ACP

1. Copy `co-ai/` into the target repository.
2. Create a `co-project/` folder in the target repository.
3. Add the required Metadata files listed below.
4. Fill the Metadata with the current project state before asking an AI collaborator to make changes.
5. Ask AI collaborators to read `co-ai/` first, then `co-project/`, then only the source files relevant to the task.
6. After meaningful architecture, content, behavior, or workflow changes, update `co-project/` before committing.

## Required `co-project/` Metadata Files

| File | Owner | Purpose |
|---|---|---|
| `co-project/context-header.md` | Human + Semantic Agent | Short current orientation for AI collaborators. |
| `co-project/project-state.json` | Implementation Agent | Machine-readable current project state. |
| `co-project/project-map.json` | Semantic Agent design + Implementation Agent serialization | Machine-readable structure and concept map summary. |
| `co-project/change-log.md` | Implementation Agent | Reverse chronological record of implementation and Metadata changes. |
| `co-project/implementation-report.md` | Implementation Agent | Latest implementation summary and validation report. |

## Protocol Files

| File | Purpose |
|---|---|
| `co-ai/protocol.md` | Core ACP mission, scope, roles, and operating rules. |
| `co-ai/workflow.md` | General collaboration workflow and SPH4U example workflow. |
| `co-ai/metadata-spec.md` | Required project Metadata files and ownership responsibilities. |
| `co-ai/semantic-agent-rules.md` | Rules for Semantic Agents. |
| `co-ai/implementation-agent-rules.md` | Rules for Implementation Agents. |

## Release Status

ACP 1.0 is intended as a stable public release template for future repositories.
