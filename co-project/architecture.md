# ACP Architecture

ACP Version: 1.0.1

Last Updated: 2026-07-08

## Project Identity

Name: ACP

Purpose: A reusable AI Collaboration Protocol that separates semantic reasoning from implementation while keeping repository metadata synchronized.

ACP is self-managed using ACP. This repository owns both the reusable protocol files and the project-specific metadata that describes the ACP repository itself.

## External-Reference Architecture

ACP is the single source of truth for collaboration protocol. Normal projects reference this repository externally instead of copying `co-ai/` by default.

| Repository Type | Owns | References |
|---|---|---|
| ACP repository | `co-ai/`, `co-project/`, examples, README | Itself |
| Normal project repository | `co-project/`, source or data files | ACP repository |

## ACP Repository Architecture

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

## Recommended Normal Project Architecture

```text
Project
|
|-- co-project/
|-- src/ or data/
`-- ...
```

Normal projects maintain only project-specific metadata by default. They should read protocol guidance from the ACP repository.

## Component Responsibilities

| Component | Type | Responsibility |
|---|---|---|
| `README.md` | Public entry point | Explains ACP, external reference guidance, adoption steps, agent roles, and required `co-project` metadata files. |
| `co-ai/` | Reusable protocol | Contains the model-independent ACP rules owned by the ACP repository. |
| `co-project/` | Project-specific metadata | Describes the ACP repository itself as an ACP-managed project. |
| `examples/` | Examples | Provides small example `co-project` layouts for different repository types. |

## Reusable Protocol

The `co-ai/` directory is owned by ACP and is referenced externally by normal projects.

| File | Purpose |
|---|---|
| `co-ai/protocol.md` | Defines ACP mission, scope, ownership, roles, startup order, and external-reference principle. |
| `co-ai/workflow.md` | Defines the default ACP working order and example workflow. |
| `co-ai/metadata-spec.md` | Defines required project metadata files and ownership responsibilities. |
| `co-ai/semantic-agent-rules.md` | Defines rules for Semantic Agents. |
| `co-ai/implementation-agent-rules.md` | Defines rules for Implementation Agents. |

## Project-Specific Metadata

The `co-project/` directory describes this repository, not another project.

Its metadata records that ACP is in the ACP 1.0.1 phase, is stable, and uses the external-reference model.

## Examples

The `examples/` directory intentionally references physics, exam visualizer, and game projects only as small adoption examples. These are not the identity or active state of the ACP repository.

## Architecture Rule

Reusable protocol rules belong in ACP's `co-ai/`. Normal project state belongs in each project's `co-project/`. Adoption examples belong in `examples/`. Public orientation belongs in `README.md`.
