# Design record

## Hypothesis and users
Evaluation leads need a path from an aggregate regression to an inspectable decision. This is a hypothesis, not a finding from completed interviews. Supporting users: annotator and investigating engineer.

## Tradeoffs
Comparison beside rubric reduces context switching but creates density; mobile stacks run details. Machine verdicts and human adjudication stay separate because exact-string checks are evidence, not final judgment. Required rationale adds friction in exchange for inspectability. Counts and denominators reveal small samples. Regression/pending filters prioritize review. Validated import/export keeps the prototype portable but cannot provide shared trusted records.

## Iteration record
v0.1: three precomputed fixtures, decision log.
v0.2: eight fixtures, deterministic engine, authoring, executable rules, validation, imports/exports, case fingerprints and 17 tests; native Figma screens. Changes respond to product completeness, not invented user feedback.

## Error and recovery states
No matches: clear filters. Empty suite: create a case. Invalid import: retain current state. Storage error: keep memory state, export to preserve. Duplicate ID: explain, retain entered values. Whitespace rationale: reject. Revised review: preserve older events. Reset: explicit confirmation.

## Planned usability study
Recruit 3–5 consenting evaluators. Ask them to find an authorization regression, resolve it, add a case, recover an exported workspace and distinguish rule pass from human approval. Observe completion, errors and hesitation without coaching. No outcomes are reported until sessions occur.

## Production handoff
Authenticated actors and permissions, durable data, append-only server events, idempotent writes, suite versioning, actual model connectors and authorized exports. Calibrated domain rubrics instead of substring heuristics where needed. Browser/accessibility QA, storage recovery, concurrency and integration tests are required before real evaluation operations.
