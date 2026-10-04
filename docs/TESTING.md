# Testing and Verification Status

This document records the verification status reported by the Builder QA pass. It distinguishes live-preview checks from source-only checks and does not claim that unavailable checks passed.

## VERIFIED in the Builder live preview

- Homepage and Investigate page opened.
- Invalid coordinate and invalid year inputs were rejected with accessible errors.
- A real NASA POWER request returned a LIVE result.
- Insufficient-record state appeared without a slope or p-value.
- Trend output displayed source, unit, sample size, slope, p-value, and method.
- Evidence Replay opened.
- JSON export produced a parseable artifact.
- Tampered evidence was rejected by hash validation.
- Event Context remained separate from the long-term trend.
- No fabricated values appeared in the inspected flows.
- Chart labels were not clipped at the tested desktop/mobile sizes.
- Export controls did not overlap other tested controls.
- No console errors were captured in the inspected routes.
- No client-side credential was found in the inspected bundle/source paths.

## SOURCE-VERIFIED

- Honest unavailable/error handling for invalid or unavailable upstream data.
- Non-significant wording does not claim that no trend exists.
- FIRMS status vocabulary supports not-configured and unavailable states.
- Focus-visible styles exist.
- Reduced-motion CSS/JS guards exist.
- Breakpoint rules cover narrow mobile and wide desktop branches.

## NOT VERIFIED

- Complete map/table parity read-back in the final pass.
- Fresh measurements at every requested responsive width.
- Full keyboard-only traversal with a real Tab interaction.
- Real reduced-motion media emulation.
- Modal focus return in an exercised modal flow.
- A genuine imported export file in addition to the tampered-file test.

## BLOCKED or DEFERRED

- Playwright/E2E execution was not completed in the Builder environment.
- A real NASA outage was not injected during the preview pass.
- Dedicated 429 rate-limit end-to-end coverage was not completed.
- Per-user authorization and application-level rate limiting require separate deployment/security verification.

## Interpretation

This repository entry is a documentation record, not a replacement for a reproducible source checkout. Before claiming production readiness, rerun the project's tests from an exported source tree and record the exact commands and results.
