# Tracework

Independent, AI-assisted developer-tool product study for Juan Emilio Mier. October 2026.

## Quick start
Python 3: `python3 -m http.server 8080 --directory dist`, then open http://localhost:8080.
Node 18+: `node --test tests/engine.test.mjs`.
Use a static server, not a file:// URL, because the app uses ES modules.

## Product flows
Create a case; inspect baseline/candidate fixtures; execute rubric rules; search/filter regressions; record/revise evidence-backed reviews; import/export workspaces; export results; reset with confirmation.

## Evaluation semantics
require_text / forbid_text: case-insensitive substring checks over output.
require_event / forbid_event: exact match against named trace events.
max_latency / max_cost: supplied metric <= threshold.
All criteria must pass. This engine is not an LLM judge or proof of semantic correctness.
Demo: 8 cases; baseline 6/8 passes, candidate 4/8, 4 regressions, 2 improvements. These are synthetic outcomes, not actual model measurements.

## Persistence and import
localStorage key: tracework-workspace-v2. Review events contain caseId, canonical case fingerprint, disposition, rationale and timestamp. Case changes invalidate prior current-status reviews; revisions remain in history. Device-local storage is not an authenticated audit log. Export before clearing browser data.
Imports: 2 MB limit, 100 cases, 1–10 rules/case, 100 events/run, 5,000 review events. Validation precedes replacement. Rendered user text is HTML-escaped.

## Validation
17 Node behavioral tests, syntax checks, HTML ID/target checks. Native Figma desktop/mobile layouts visually inspected. Browser visual and end-to-end UI testing pending because the browser connection was unavailable. Do not describe the app as production-ready or perfectly tested.

## Design artifacts
https://www.figma.com/design/MhClnHfTxHwm9x74lPeRe9?node-id=4-34
Editable rationale boards, desktop/mobile native design explorations, reusable components, bound colors and text styles. They are not pixel-matched browser captures.

## Attribution and application readiness
Initiated for Juan Emilio Mier; ChatGPT/Codex generated initial implementation and documentation. Candidate ownership requires reviewing, editing and independently demonstrating the work. No live inference, customers, user-research results, prior design employment or Claude Code usage is claimed.
This artifact does not create years of experience or independent proficiency. Explain its limits, modify a case, edit a design screen and accurately describe your contribution before using it in an application. Anthropic requests candidate-authored first drafts and permits AI refinement: https://www.anthropic.com/candidate-ai-guidance.
