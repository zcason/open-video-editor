# Architecture Decision Records

This directory will contain Architecture Decision Records (ADRs) for decisions that materially shape Open Video Editor.

An ADR should explain:

- the problem
- constraints
- considered options
- decision
- consequences and tradeoffs
- status

## Decisions we need to make

The initial architecture deliberately leaves several implementation choices open until we prototype them:

1. desktop application framework
2. primary implementation language(s)
3. media engine: direct FFmpeg, MLT, GStreamer Editing Services, or a combination
4. canonical project/timeline data model
5. plugin process and isolation model
6. plugin IPC protocol
7. plugin SDK language/runtime strategy
8. UI extension mechanism
9. rendering architecture
10. GPU acceleration strategy on Linux
11. local AI runtime integration strategy
12. project file format and versioning

## ADR naming

Use sequential files:

```text
0001-desktop-framework.md
0002-media-engine.md
0003-plugin-isolation.md
```

A decision should not be marked `Accepted` until we have enough evidence to defend it. Prototype results should be captured in the ADR rather than relying on assumptions.
