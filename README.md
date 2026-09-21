# strategy-factory

A small, source-based strategic coach for ChatGPT Work. One living Markdown document per case; no executable code, database, server, or model-specific prompt machinery.

## Use

Ask `@strategy-factory` to develop an idea or resume its existing document. It reads the latest case, works on the next useful decision, and updates that same document.
The host supplies research and durable file access. A conversation alone is not saved state. Keep personal cases in your chosen storage, not this plugin repository unless explicitly intended.

## One document, seven stages

1. Problem and decision — Matt Pocock's grilling, adapted for one question at a time.
2. Evidence and alternatives — primary-source research and proportionate Green Book options appraisal.
3. Value and adoption — Green Book Five Case Model; optional Amazon Working Backwards PR/FAQ.
4. Validation — Strategyzer Test Card.
5. Narrative structure — Moghe's *Nail your narrative* or Amazon decision memo practice.
6. Working draft and critique — Ptacek's *How To Write With An LLM*.
7. Outcome and learning — Magenta Book evaluation.

The [core skill](skills/strategy-factory/SKILL.md) contains the complete method and source links. These are our adaptations, not author-endorsed skills or demonstrated plugin effectiveness.
Stages are a map, not mandatory gates. Forecasts and decisions retain their history; changed evidence triggers review of dependent sections. Writing defaults to critique; explicit drafting requests switch to assisted drafting.

## Package

The core is self-contained. Existing named specialists and `write-with-an-llm` are short entry points into it; they require the core to be readable. Do not install those entry points alone.
[Case template](cases/templates/case.md) · [Acceptance scenarios](evals/scenarios.md) · [0.2.0 release record](evals/release-0.2.0.md).

Native Work installation and portable source packaging are separate. Complete-plugin registration and ordinary Chat/iOS execution are not implied by Work tests. Previous verification records describe 0.1.1, not this release.
There is no automatic upstream update service. Review source changes when they are relevant; keep model behavior flexible rather than prescribing a script.

## License

Apache-2.0 for this package; linked works retain their own rights. Method instructions are concise original adaptations. Naming uses lowercase hyphenated skill names.
