# AI Collaboration Workflow

ACP Version: 1.0.1

Last Updated: 2026-07-08

## Default Working Order

```text
Phase 0: Read ACP repository
Phase 1: Read project repository
Phase 2: Read co-project metadata
Phase 3: Read task-specific materials
Phase 4: Design / implementation / validation according to ACP
```

## General Workflow

```text
Human
-> ACP repository
-> Project repository
-> co-project
-> Semantic Agent
-> Knowledge Model
-> Implementation Agent
-> Repository
-> Metadata Update
-> Validation
-> Commit
```

## Example Teaching Content Workflow

```text
PDF
-> ACP repository
-> Project repository
-> co-project
-> Semantic Agent semantic analysis
-> Knowledge Model
-> Implementation Agent repository update
-> JSON update
-> Website render
-> Metadata Update
-> Validation
-> Commit
```

## Collaboration Notes

- Human sets the goal, constraints, and acceptance criteria.
- ACP repository defines reusable protocol rules.
- Project repository contains the current source files and project Metadata.
- `co-project` stores the project-specific state required by AI collaborators.
- Semantic Agent analyzes meaning, concepts, dependencies, reasoning, and Knowledge Model structure.
- Implementation Agent updates files, validates behavior, maintains Metadata, and prepares commits.
- Metadata must stay short enough for AI collaborators to read before opening source files.
