# Point-and-Click Dual-Renderer Engine

<img width="1800" height="1000" alt="image" src="https://github.com/user-attachments/assets/f485e5b9-3493-4207-b60f-c23d9217a360" />


> A professional, content-neutral foundation for building point-and-click adventures with Babylon and Three behind one renderer-neutral contract, shipping to browser and desktop, and remaining fully playable offline.

This repository package presents the **Release Paper v4.0** as a clean, recruiter-ready and collaborator-ready README entrypoint. The original PDF remains the normative source.

---

## Executive summary

The blueprint defines one platform-neutral TypeScript core, one canonical content model, one `RendererPort`, a Babylon provider, an optional Three provider, and a `RendererOrchestrator` that selects and owns exactly one provider per live viewport.

The default product path is deliberately conservative:

- Babylon is the base renderer.
- Three is a lazy-loaded specialist provider.
- A Babylon-only build must contain **0 bytes of Three**.
- The simulation is deterministic and renderer-neutral.
- Browser and Tauri desktop builds share the same core.
- Local gameplay remains fully offline by default.

---

## Runtime architecture

<img width="1800" height="1180" alt="image" src="https://github.com/user-attachments/assets/69c317b3-8b88-40af-93a2-48bbc4d836a0" />


The core never imports Babylon, Three, or Tauri directly. Renderer construction and disposal belong exclusively to the orchestrator. Renderer parity means equivalent game behavior and state - not pixel-identical output.

---

## What v4 adds

Version 4 keeps the strong v3 architecture and adds the production systems needed for a fundable, auditable and legally shippable program:

- measurable KPIs and budgets;
- deterministic time, seeded randomness and replayable state hashes;
- typed error contracts and append-only error codes;
- structured 9-vector logging;
- telemetry consent and privacy controls;
- performance device tiers and dynamic quality;
- internationalization, RTL and text-expansion support;
- SemVer, deprecation and compatibility policy;
- STRIDE threat modeling and supply-chain controls;
- privacy, age-rating and legal release gates;
- CI/CD, staged rollout, rollback and safe-mode recovery;
- phase gates, risk owners and implementation estimates.

---

## Non-negotiable invariants

- The core never imports a renderer or Tauri.
- Commands and conditions remain serializable data.
- Local gameplay never needs a server.
- Save writes are versioned, verified and crash-safe.
- Exactly one provider owns a viewport.
- No wall-clock API drives simulation.
- Boundary failures return typed coded results.
- Every meaningful state change emits a structured log event.
- Dependencies are pinned, attributed and included in the SBOM.

---

## Quality and delivery targets

| Metric | Target |
|---|---:|
| Browser cold time to interactive | <= 3.0 s |
| Simple-scene frame time | <= 16.7 ms |
| Three bytes in Babylon-only build | 0 |
| Autosave serialize + write p95 | <= 250 ms |
| Save/reload state divergence | 0 |
| Core line coverage | >= 90% |
| High/critical CVEs at release | 0 |
| WCAG 2.2 AA violations | 0 |
| Crash-free session rate | >= 99.5% |

---

## Security and compliance posture

The webview holds no secrets or signing keys. Privileged actions cross into Rust through a narrow, validated, least-privilege command surface. Release artifacts include an SBOM, provenance, dependency and license checks, signature verification, and tested rollback.

Telemetry is off by default and gated by granular, revocable consent. Privacy, age ratings, legal documents, accessibility and license clearance are all treated as release gates.

---

## Implementation roadmap

The release paper defines ten gated phases:

1. Foundations
2. Core simulation
3. Babylon provider
4. Adventure systems
5. Browser / desktop platform parity
6. Optional Three provider
7. Quality and observability
8. Security and compliance
9. Release dry run
10. Accessibility and internationalization

No phase begins until the previous exit gate is green.

---

## Full README overview

<img width="1800" height="1100" alt="image" src="https://github.com/user-attachments/assets/93c85989-6364-4884-ba28-242092404253" />


---

## Included source

```text
Point-and-Click-Dual-Renderer-Engine_Blueprint_v4.0_ReleasePaper.pdf
```

Use the PDF for the full 17-page release paper and this README as the public repository entrypoint.
