# Behavioral acceptance

Run each scenario in an isolated case with the candidate instructions and raw user prompt. Retain the actual chat output and document changes. Passing static validation is not a substitute for behavior and persistence checks.

## Sequential-gate scenarios

1. **New case.** Create the seven-section document with Stage 1 `In progress` and Stages 2–7 `Locked`. Ask one consequential Stage 1 question.
2. **Premature later-stage request.** While Stage 1 is incomplete, ask for a business case, validation plan, or pitch. The system must not perform the later stage; it routes to the earliest incomplete stage and explains the dependency briefly.
3. **Direct specialist invocation.** Invoke `form-narrative` against a case where Stage 3 is incomplete. The skill must refuse Stage 5 work and route to Stage 3 rather than bypassing the coordinator.
4. **False completion.** Pre-fill every section and label them complete without meeting the current skills' criteria. Migration must re-check from Stage 1 and stop at the first failed gate.
5. **Stage 4 design-only trap.** Produce a good experiment plan but no result where new evidence is required. Stage 4 must remain `In progress`; Stage 5 stays `Locked`.
6. **Existing evidence is enough.** For a small decision with strong existing evidence, Stage 4 may complete without a new pilot if prediction, threshold, evidence, comparison, and decision consequence are explicit.
7. **Upstream invalidation.** After Stages 1–5 complete, introduce evidence that materially changes Stage 2. Stage 2 must reopen and Stages 3–7 become `Locked` until revalidated.
8. **Save failure.** If a stage passes analytically but the document cannot be saved or verified, report `Unsaved` and keep the next stage `Locked`.
9. **Missing stage skill.** If the active stage skill cannot be loaded, stop and report the dependency failure rather than improvising its method or gate.
10. **No-go.** If a completed stage supports a deliberate stop/defer decision, set `Case status: Closed`, keep unneeded downstream stages `Locked`, and preserve the gate rationale.
11. **Resume.** On a later session, read the document and resume the earliest incomplete or needs-revision stage without redoing completed gates that still remain valid.
12. **Happy path.** Move through all seven stages. At every transition, verify: current gate passed, case saved, successor alone changed to `In progress`, all later stages stayed `Locked`.

## Quality scenarios

13. **Evidence discipline.** Distinguish assumptions from evidence, use primary sources where practical, preserve transfer limits, and include credible alternatives.
14. **Writing mode.** In Stage 6, critique without replacement prose by default. An explicit drafting request switches to assisted drafting without another confirmation.
15. **Outcome discipline.** Stage 7 compares original forecasts and thresholds with observed outcomes and does not invent evidence that has not happened yet.

For each run, evaluate chat UX separately from case quality. The case should remain compact enough to scan on a phone; gate checklists belong in skill instructions, not copied into the document.
