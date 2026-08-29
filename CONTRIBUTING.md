# Contributing

Open Video Editor is in an early architecture phase. Contributions should optimize for learning and architectural clarity rather than feature count.

## Before implementing major components

For changes that materially affect the architecture, open an issue or Architecture Decision Record first.

Examples include:

- changing the media backend
- introducing a desktop framework
- defining the plugin IPC protocol
- changing the timeline data model
- introducing a new plugin runtime
- changing project file formats

## Architectural invariants

Contributions should preserve these principles unless an accepted ADR changes them:

- plugins are first-class applications inside the editor
- plugins interact with editor state through stable APIs
- timeline/project mutations flow through editor commands
- the core editor does not depend on the AI plugin
- cloud services are optional
- editing remains usable locally
- AI-generated edits remain inspectable and undoable

## Documentation

Canonical architecture documentation lives under `docs/`.

When implementation and documentation disagree, either update the implementation or explicitly update the canonical document and explain the architectural change.

## Current phase

Before broad implementation begins, the project needs prototypes and ADRs for the major unresolved technical choices listed in `docs/decisions/README.md`.
