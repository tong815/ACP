# Project Metadata Specification

ACP Version: 1.0

Last Updated: 2026-07-08

Project-specific Metadata belongs in `co-project/`.

## Required Files

| File | Owner | Purpose | Update When |
|---|---|---|---|
| `co-project/context-header.md` | Human + Semantic Agent | Short current orientation for AI collaborators. | Every meaningful project phase or goal change. |
| `co-project/project-state.json` | Implementation Agent | Machine-readable current project state. | Architecture, source-of-truth, active files, features, risks, or next task changes. |
| `co-project/project-map.json` | Semantic Agent (design); Implementation Agent (serialization) | Machine-readable structure and concept map summary. | Course, unit, chapter, concept, dependency, or file structure changes. |
| `co-project/change-log.md` | Implementation Agent | Reverse chronological record of protocol, architecture, and implementation changes. | Every implementation or Metadata change. |
| `co-project/implementation-report.md` | Implementation Agent | Latest implementation summary and validation report. | Every completed implementation task. |

## Ownership Responsibilities

- Human provides goals, constraints, and corrections to the current Repository state.
- Semantic Agent designs semantic structures, Concept IDs, dependencies, and Knowledge Model relationships.
- Implementation Agent serializes agreed structures, updates Repository files, validates Metadata, and records implementation results.
- Repository owns Metadata as durable project state. Metadata should remain current even when previous conversations are unavailable.

## Metadata Rules

- Metadata should summarize current state, not duplicate full source content.
- Project Metadata should point AI collaborators to the right source files.
- JSON Metadata must remain valid JSON.
- Concept IDs and dependency relationships should be summarized in `project-map.json`, while detailed teaching content remains in data files.
- Every implementation that changes behavior, data, architecture, Knowledge Model structure, Concept IDs, or workflow must update the relevant Metadata files.
