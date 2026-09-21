# strategy-factory

A portable agent-skills toolkit for developing an idea into a decision-ready strategic case.

The first workflow is **idea-development**. It is designed to improve the user's strategic judgment rather than merely generate polished proposals. The canonical methodology lives in portable Agent Skills so the same core can run across ChatGPT, GitHub Copilot, and the Claude app.

## idea-development workflow

1. **sharpen-idea** — define the problem, outcome, audience, constraints, and assumptions.
2. **find-frameworks** — find established frameworks that fit the problem before inventing a new one.
3. **investigate-prior-art** — research analogous implementations and credible alternatives, including doing nothing.
4. **model-value** — turn benefits into explicit, measurable value hypotheses with costs and uncertainty.
5. **design-experiment** — identify the weakest important assumption and design the smallest useful experiment.
6. **form-narrative** — build a decision-oriented argument for a specific audience and ask.
7. **review-outcome** — compare predictions with outcomes and record what changed in the user's judgment.

The workflow is deliberately non-linear. New evidence can send a case back to an earlier stage.

## Principles

- Coach judgment; do not replace it.
- Separate facts, assumptions, estimates, and decisions.
- Research factual claims and preserve sources.
- Existing approaches beat invented frameworks when outcomes are comparable.
- "Do not pursue" is a valid outcome.
- Do not create a pitch before the value case survives challenge.
- Keep the smallest useful case record; avoid building a case-management system prematurely.
- Keep essential behavior portable; host-specific packaging must not become product logic.

## Naming

Use lowercase, hyphen-separated names everywhere a project, workflow, or skill is named: `strategy-factory`, not `Strategy Factory`. Each skill's directory, frontmatter `name`, top-level Markdown heading, and archive base name must agree. Use the same spelling for any host-specific display-name metadata added later. Standard filenames such as `SKILL.md`, `README.md`, and `LICENSE` retain their required or conventional spelling.

## Repository structure

- `plugin.json` — Agent Plugins 1.0 package metadata for compatible hosts.
- `skills/strategy-factory/SKILL.md` — overall method and coaching contract.
- `skills/*/SKILL.md` — independently discoverable specialist skills.
- `cases/templates/case.md` — resumable case checkpoint.
- `evals/scenarios.md` — behavioral acceptance scenarios.
- `evals/compatibility.md` — cross-platform compatibility matrix, installation preflight, and acceptance rule.

## Platform strategy

The `skills/` directory is the canonical product. ChatGPT, GitHub Copilot, and Claude should consume the same methodology. Host-specific adapters may be added only when testing demonstrates a real capability gap.

Compatibility means materially equivalent strategic behavior against the same eval scenarios, not identical packaging, wording, or tool calls. A successful upload is not proof of availability or invocation. Complete the installation preflight in `evals/compatibility.md` before evaluating automatic selection or coaching quality.

## V1

V1 is intentionally skills-first. There is no database, custom web UI, autonomous orchestration service, workflow builder, or speculative host adapter. The host provides the conversational interface and available research tools; this repository defines the method.

## License

Apache-2.0. See `LICENSE`.
