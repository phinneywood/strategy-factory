# strategy-factory

A source-based strategic coach for ChatGPT Work built as a strict seven-stage state machine. One living Markdown document carries the case; one stage skill owns each section, method, and exit gate.

## Use

Ask `@strategy-factory` to develop or resume an idea. The coordinator reads the case, finds the earliest incomplete stage, and delegates to that stage's skill.

Later stages cannot start early. A filled section or user request to skip ahead does not satisfy a gate. The active stage skill must pass its own exit criteria, save the result, and verify persistence before the next stage unlocks.

## Seven stages

1. **Problem and decision** → `sharpen-idea`
2. **Evidence and alternatives** → `evidence-and-alternatives`
3. **Value and adoption** → `model-value`
4. **Validation** → `design-experiment`
5. **Narrative structure** → `form-narrative`
6. **Working draft and critique** → `write-with-an-llm`
7. **Outcome and learning** → `review-outcome`

The coordinator owns routing and the shared case contract. It does **not** own stage methods or exit criteria.

## Case states

Stages use only `Locked`, `In progress`, `Complete`, and `Needs revision`. An active case has one `In progress` stage; every later stage is `Locked`.

A substantive upstream change reopens the earliest affected stage and locks downstream work. A deliberate no-go/defer may close the case without forcing irrelevant later stages.

The case stays readable on a phone: a compact opening, seven sections, and a one-line gate rationale for completed stages. Full gate checklists live in the skills rather than the artifact.

## Package

The repository contains the coordinator plus seven stage skills. Stage 2 combines framework discovery, prior art, and options appraisal in one skill because they share one section and one gate.

[Case template](cases/templates/case.md) · [Acceptance scenarios](evals/scenarios.md)

Native Work installation and portable source packaging are separate. Complete-plugin registration and ordinary Chat/iOS execution are not implied by repository validation.

## License

Apache-2.0 for this package; linked works retain their own rights. Method instructions are concise original adaptations.
