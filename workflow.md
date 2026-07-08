# AI Collaboration Workflow

ACP Version: 1.0

Last Updated: 2026-07-08

## General Workflow

```text
Human
↓
Repository
↓
co-ai
↓
co-project
↓
Semantic Agent
↓
Knowledge Model
↓
Implementation Agent
↓
Repository
↓
Metadata Update
↓
Validation
↓
Commit
```

## SPH4U Teaching Content Workflow

```text
SPH4U PDF
↓
Repository
↓
co-ai
↓
co-project
↓
Semantic Agent semantic analysis
↓
Knowledge Model
↓
Implementation Agent repository update
↓
JSON update
↓
Website render
↓
Metadata Update
↓
Validation
↓
Commit
```

## Collaboration Notes

- Human sets the goal, constraints, and acceptance criteria.
- Repository contains the current source files and Metadata.
- `co-ai` defines ACP rules that can be reused across repositories.
- `co-project` stores the project-specific state required by AI collaborators.
- Semantic Agent analyzes meaning, concepts, dependencies, reasoning, and Knowledge Model structure.
- Implementation Agent updates files, validates behavior, maintains Metadata, and prepares commits.
- Metadata must stay short enough for AI collaborators to read before opening source files.
