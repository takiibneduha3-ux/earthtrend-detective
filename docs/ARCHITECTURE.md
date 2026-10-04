# Architecture Overview

The completed prototype is described as a frontend investigation interface backed by server-side application functions and shared scientific modules.

## Main flow

```text
User case inputs
  -> server-side NASA/source functions
  -> validation and quality gate
  -> annualization and reference climatology
  -> anomaly and trend analysis
  -> significance and spatial/event context
  -> Evidence Replay and export
```

## Design boundaries

- Scientific calculations are intended to remain server-side and authoritative.
- The interface renders validated results rather than independently recomputing them.
- NASA POWER retrieval metadata and returned coordinates are part of provenance.
- Event context is kept separate from long-term trend statistics.
- Evidence snapshots preserve method, source, timestamp, and limitation metadata.

## Repository status

This repository currently contains the project README, license, methodology note, presentation, and documentation added during the handoff. It does not contain the complete Builder-generated application source tree because source export was unavailable in the originating workspace.

The architecture description is therefore a high-level handoff document, not a substitute for source-code documentation generated from a complete checkout.
