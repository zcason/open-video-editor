# Open Video Editor

An open-source, plugin-first video editor for Linux.

The project is built around a small editing core and a first-class plugin runtime. Plugins should be capable of behaving like applications inside the editor: owning UI, managing state, registering commands, running background jobs, integrating local or cloud services, and manipulating projects through stable editor APIs.

The goal is not to rebuild every feature in Premiere Pro or DaVinci Resolve. The goal is to build a programmable editing platform where users install the workflows and capabilities they actually need.

## Core principles

1. **Plugin-first architecture**
   The editor should remain small. Specialized workflows belong in plugins whenever possible.

2. **Plugins are applications inside the editor**
   A plugin is not limited to an effect or side panel. It may provide its own interface, state, commands, workflows, background jobs, and integrations.

3. **Plugins extend the editor, but do not bypass it**
   Human UI actions, plugins, scripts, and AI all manipulate projects through the same editor command layer.

4. **Local-first, not local-only**
   Core editing must work locally. AI and external services may run locally or in the cloud, but the architecture must never require cloud infrastructure.

5. **Non-destructive and auditable editing**
   Editor operations should be deterministic, undoable, inspectable, and reproducible.

6. **Linux first**
   Linux is the initial platform and design constraint, not necessarily the permanent limit of the project.

## MVP

The initial MVP focuses on:

- media import and project management
- timeline playback
- video and audio tracks
- cut, split, trim, move, and ripple delete
- basic transforms and audio controls
- undo and redo
- rendering and export
- plugin runtime and SDK
- command API
- one flagship AI editing plugin

The first plugin will focus on transcript-based editing.

## Canonical documentation

- [MVP architecture](docs/architecture/mvp-architecture.md)
- [Plugin runtime](docs/architecture/plugin-runtime.md)
- [AI editor plugin](docs/plugins/ai-editor.md)
- [Transcript editing workflow](docs/workflows/transcript-editing.md)
- [Architecture decisions](docs/decisions/README.md)

## Project status

This repository is currently in the architecture and MVP-definition phase. Technical choices that have not been validated are intentionally documented as candidates rather than commitments.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
