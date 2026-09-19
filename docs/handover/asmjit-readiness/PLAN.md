# AsmJit Readiness Plan — Point-and-Click-Dual-Renderer-Engine

Status: PREPARED_ONLY
Branch: `prep/asmjit-readiness-2026-09-19`
Relevance: LOW / CONDITIONAL

## Current assessment
The current dual-renderer/browser-desktop architecture does not require native JIT code generation.

## Activation triggers
Revisit only if the engine adds:
- a native scripting VM with runtime compilation,
- a CPU expression/behavior compiler,
- dynamically specialized simulation kernels,
- or a desktop-only execution backend where runtime codegen is demonstrably useful.

## Evaluation path
Profile -> define neutral IR -> static/native baseline -> isolated AsmJit prototype -> cross-architecture tests -> measured decision.

## Constraints
Renderer abstraction must remain independent of JIT. Browser path must never depend on executable native memory.

No implementation, dependency addition, PR, or merge is authorized by this branch.
