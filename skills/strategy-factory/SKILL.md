---
name: strategy-factory
description: Orchestrate a seven-stage strategic case; route work to the active stage skill and enforce sequential gates.
---

# strategy-factory

Orchestrate the case. Do not perform a stage's method or decide that a stage is complete yourself. Each stage skill owns its method, section contract, and exit criteria.

## Stage map

1. Problem and decision → `sharpen-idea`
2. Evidence and alternatives → `evidence-and-alternatives`
3. Value and adoption → `model-value`
4. Validation → `design-experiment`
5. Narrative structure → `form-narrative`
6. Working draft and critique → `write-with-an-llm`
7. Outcome and learning → `review-outcome`

## State machine

Each stage has one status: `Locked`, `In progress`, `Complete`, or `Needs revision`. An active case has exactly one stage that is `In progress`; every later stage is `Locked`.

1. Read the latest case before doing work. For a new case, create the standard seven-section document with Stage 1 `In progress` and Stages 2–7 `Locked`.
2. The active stage is the earliest stage that is not `Complete`. If a completed upstream stage becomes invalid, mark the earliest affected stage `Needs revision`, lock every downstream stage, then make that stage `In progress` when work resumes.
3. Load and follow the active stage skill. A request for a later stage does not bypass this rule. Briefly state the dependency and continue with the earliest incomplete stage.
4. Only the active stage skill may mark its stage `Complete`, and only after all of its exit criteria pass. Check structural and factual criteria directly. When completion depends on a substantive judgment, use the user's stated decision; do not convert an assistant recommendation into the user's decision and do not add a separate approval ceremony when the user has already made the judgment.
5. Save and verify the completed stage before unlocking its successor. If persistence fails, report `Unsaved` and keep the successor `Locked`.
6. After verified completion, set the successor to `In progress` and keep all later stages `Locked`.
7. A substantive change to a completed stage invalidates every dependent downstream completion. Reopen from the earliest affected stage rather than patching later sections in place.
8. A deliberate no-go or defer decision may close the case. Record `Case status: Closed`, keep all unneeded downstream stages `Locked`, and retain the completed gate that produced the decision. Reopening restores normal sequencing.

Never treat a filled section, an old status label, or a user request to skip ahead as proof that a gate passed.

## Conversation

Begin case replies with: `Stage N/7 · Name · [Case](verified link) · Saved / Unsaved / Not started`.

Keep chat short and decision-focused. Default to a brief interpretation and one consequential question or next action. Research facts independently when useful; do not repeatedly ask the user for facts that can be resolved another way.

## Case document

Maintain one Markdown document per case. Keep exactly seven numbered stage sections plus a compact opening:

- `Case status`
- `Decision`
- `Current view`
- `Next`

Do not print full gate checklists in the case. The stage skill owns the checklist. When a stage completes, add one short `**Gate:** Passed — ...` rationale under that stage. When blocked, record only the decision-relevant gap.

Preserve claim-level sources, user decisions, estimates, forecasts, thresholds, and material caveats. Keep current conclusions concise rather than accumulating a transcript. Re-read before saving and preserve concurrent changes.

## Migration

For cases created under earlier versions, do not trust `Ready`, `Deferred`, filled headings, or prior progression. Starting at Stage 1, verify each completed-looking stage against the current stage skill's exit criteria. Stop at the first failed or uncertain gate, set it to `In progress`, and lock every later stage.
