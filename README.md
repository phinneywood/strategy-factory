# Strategy Factory

A ChatGPT-native workspace for developing an idea into a decision-ready strategic case.

The first workflow is **Idea Development**. It is designed to improve the user's strategic judgment rather than merely generate polished proposals.

## Idea Development workflow

1. **Sharpen** — define the problem, outcome, audience, constraints, and assumptions.
2. **Frameworks** — find established frameworks that fit the problem before inventing a new one.
3. **Prior art** — research analogous implementations and credible alternatives, including doing nothing.
4. **Value** — turn benefits into explicit, measurable value hypotheses with costs and uncertainty.
5. **Test** — identify the weakest important assumption and design the smallest useful experiment.
6. **Narrative** — build a decision-oriented argument for a specific audience and ask.
7. **Review** — compare predictions with outcomes and record what changed in the user's judgment.

The workflow is deliberately non-linear. New evidence can send a case back to an earlier stage.

## Principles

- Coach judgment; do not replace it.
- Separate facts, assumptions, estimates, and decisions.
- Research factual claims and preserve sources.
- Existing approaches beat invented frameworks when outcomes are comparable.
- "Do not pursue" is a valid outcome.
- Do not create a pitch before the value case survives challenge.
- Keep the smallest useful case record; avoid building a case-management system prematurely.

## Repository structure

- `plugin/coach/SKILL.md` — entry point and routing behavior.
- `plugin/skills/*/SKILL.md` — specialized workflow stages.
- `cases/templates/case.md` — resumable case checkpoint.
- `evals/scenarios.md` — behavioral acceptance scenarios.

## V1

V1 is intentionally skills-first. There is no database, custom web UI, autonomous orchestration service, or workflow builder. ChatGPT is the interface and provides research/tool use. The repository defines the method and its reusable skills.
