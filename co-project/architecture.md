# ACP Architecture

ACP Version: 1.0

Last Updated: 2026-07-08

## Project Identity

Name: ACP

Purpose: A reusable AI Collaboration Protocol that separates semantic reasoning from implementation while keeping repository metadata synchronized.

ACP is self-managed using ACP. This repository contains both the reusable protocol template and the project-specific metadata that describes the ACP repository itself.

## Repository Architecture

```text
ACP
|
|-- README.md
|-- co-ai/
|   |-- protocol.md
|   |-- workflow.md
|   |-- metadata-spec.md
|   |-- semantic-agent-rules.md
|   `-- implementation-agent-rules.md
|-- co-project/
|   |-- architecture.md
|   |-- context-header.md
|   |-- project-state.json
|   |-- project-map.json
|   |-- change-log.md
|   `-- implementation-report.md
`-- examples/
    |-- physics-project/
    |   `-- README.md
    |-- exam-visualizer/
    |   `-- README.md
    `-- game-project/
        `-- README.md
```

## Component Responsibilities

| Component | Type | Responsibility |
|---|---|---|
| `README.md` | Public entry point | Explains ACP, adoption steps, agent roles, and required `co-project` metadata files. |
| `co-ai/` | Reusable protocol | Contains the model-independent ACP rules that can be copied into future repositories. |
| `co-project/` | Project-specific metadata | Describes the ACP repository itself as an ACP-managed project. |
| `examples/` | Examples | Provides small example `co-project` layouts for different repository types. |

## Reusable Protocol

The `co-ai/` directory is the reusable ACP template.

| File | Purpose |
|---|---|
| `co-ai/protocol.md` | Defines ACP mission, scope, ownership, roles, and startup order. |
| `co-ai/workflow.md` | Defines the general Human to Repository workflow and keeps the included PDF workflow as an intentional example. |
| `co-ai/metadata-spec.md` | Defines required project metadata files and ownership responsibilities. |
| `co-ai/semantic-agent-rules.md` | Defines rules for Semantic Agents. |
| `co-ai/implementation-agent-rules.md` | Defines rules for Implementation Agents. |

## Project-Specific Metadata

The `co-project/` directory describes this repository, not another project.

Its metadata records that ACP is in the ACP 1.0 phase, is stable, and is the first reference implementation of the ACP workflow.

## Examples

The `examples/` directory intentionally references physics, exam visualizer, and game projects only as small adoption examples. These are not the identity or active state of the ACP repository.

## Architecture Rule

Reusable rules belong in `co-ai/`. ACP repository state belongs in `co-project/`. Adoption examples belong in `examples/`. Public orientation belongs in `README.md`.
