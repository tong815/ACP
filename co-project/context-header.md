# ACP Context Header

ACP Version: 1.0.1

Last Updated: 2026-07-08

## Project

ACP

## Purpose

A reusable AI Collaboration Protocol that separates semantic reasoning from implementation while keeping repository metadata synchronized.

## Current Phase

ACP 1.0.1

## Current Status

Stable patch clarification

## Current Repository Role

ACP is the protocol source of truth. This repository owns the reusable `co-ai/` protocol files and also keeps `co-project/` metadata because ACP is self-managed using ACP.

## External-Reference Model

- ACP is the protocol source.
- Normal projects reference ACP externally.
- Normal projects keep only `co-project/` metadata by default.
- Normal projects should not copy `co-ai/` unless they intentionally vendor or pin a protocol version.

## Source of Truth

Repository state and Metadata are the source of truth. Previous conversations should not be required for a new AI collaborator to continue work.

## Startup Order

1. Read the ACP repository protocol files in `co-ai/`.
2. Read the target project repository.
3. Read the target project's `co-project/` metadata.
4. Inspect only the repository files relevant to the requested task.
5. Design, implement, validate, and update metadata according to ACP.

## Important Boundaries

- Do not redesign ACP unless explicitly asked.
- Do not remove `co-ai/` from the ACP repository.
- Do not delete ACP's own `co-project/` metadata.
- Reusable protocol rules live in ACP's `co-ai/`.
- Project-specific metadata lives in each project's `co-project/`.
- Small adoption examples live in `examples/`.
- ChatGPT and Codex may appear only as compatibility examples; ACP remains model-independent.
