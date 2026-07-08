# ACP Context Header

ACP Version: 1.0

Last Updated: 2026-07-08

## Project

ACP

## Purpose

A reusable AI Collaboration Protocol that separates semantic reasoning from implementation while keeping repository metadata synchronized.

## Current Phase

ACP 1.0

## Current Status

Stable

## Current Repository Role

ACP is now self-managed using ACP. This repository contains the reusable `co-ai/` protocol template and the `co-project/` metadata that describes ACP itself.

## Source of Truth

Repository state and Metadata are the source of truth. Previous conversations should not be required for a new AI collaborator to continue work.

## Startup Order

1. Read `co-ai/protocol.md`.
2. Read `co-ai/workflow.md`.
3. Read `co-ai/metadata-spec.md`.
4. Read the role-specific rules in `co-ai/semantic-agent-rules.md` or `co-ai/implementation-agent-rules.md`.
5. Read this `co-project/` metadata.
6. Inspect only the repository files relevant to the requested task.

## Important Boundaries

- Do not redesign ACP unless explicitly asked.
- Reusable protocol rules live in `co-ai/`.
- ACP-specific project metadata lives in `co-project/`.
- Small adoption examples live in `examples/`.
- ChatGPT and Codex may appear only as compatibility examples; ACP remains model-independent.
