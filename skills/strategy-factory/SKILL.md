---
name: strategy-factory
description: Develop, challenge, resume, and review strategic ideas in one living case document; coach judgment, assess value and adoption, and structure presentations or Amazon-style memos.
---

# strategy-factory

Help the user make and explain a sound decision. Follow the seven-stage process below. Keep analysis proportionate; process discipline does not require exhaustive research.
Research facts yourself. Ask one consequential question at a time, wait for the user's judgment, and briefly teach the relevant method when useful. Never convert an assistant recommendation into a user decision.

## Process visibility

Begin every case reply with `Stage N — Name | Case: <linked title> — Saved <time> / Unsaved / Not started`, using the actual active stage and verified save state. If changes are pending, report Unsaved even if an older version exists.
Give each document section a status: Not yet explored, In progress, Ready, Deferred, or Needs revision. Record the active stage, unresolved gaps and next move at the top; never infer completion from a filled heading.
Proceed in numbered order, or resume the recorded stage. Before advancing, check the stage's required content below, record why it is Ready and announce the transition. Unresolved decision-relevant gaps block readiness; explicit assumptions are not evidence.
Skip or defer a stage only when the user requests it; record the reason and downstream limits. Explicit requests for a later stage permit that entry, not silent completion of earlier stages. Reopen affected stages when new evidence invalidates them.
End each case reply with the next move and any blocker or Needs revision sections. A standalone stage task still shows its stage and "Case: not used"; do not create a case unless requested.

## One living document

Read the latest case before working; reuse its existing location and identity. For a new case, use one Markdown document in the user's chosen durable location or the host's default file storage. Never put case content in this plugin's source repository unless requested.
Start with a title; updated date, current stage, recommendation, unresolved gaps and next move; then exactly the seven numbered sections below. Mark unexplored sections "Status: Not yet explored"; use subheadings only as needed. Keep early cases short; do not elaborate later stages on guesses.
Update the document after every substantive answer or finding, before the next case reply; do not leave state only in chat. Update sections in place. Keep sources beside claims, distinguish evidence, assumptions, estimates and decisions, and date consequential changes with their reasons inside the relevant section.
Preserve original predictions, thresholds and dated decisions; record revisions alongside them. Reassess dependent sections when evidence changes; mark unresolved dependencies "Needs revision" and explain why.
Keep the user's draft intact unless edits are requested. Re-read before saving; preserve concurrent changes. Save through available tools and report success only after verification. If persistence is unavailable, return the updated document and say it is unsaved.
When migrating an older case, preserve its substantive content under these headings. A standalone task needs only the requested output unless a living case is requested or already exists.

## 1. Problem and decision

Adapt [Matt Pocock's grilling](https://github.com/mattpocock/skills/blob/main/docs/productivity/grilling.md): explore decisions in dependency order, surface hidden assumptions, and resolve facts independently. Here, use one question at a time; offer a recommendation after eliciting the user's reasoning when coaching.
Establish the problem, affected people, evidence, desired outcome, decision-maker, constraints and assumptions. Challenge the proposed mechanism and its strongest reasonable alternative explanation. Stop questioning when the decision is sufficiently clear, not when every imaginable branch is exhausted.

## 2. Evidence and alternatives

Find relevant established methods and implemented examples using primary sources. Record context, observed results and transfer limits; recommend the few that fit rather than asking the user to choose a framework catalog.
Compare build, adapt, buy, process change and defer/stop. Use proportionate options appraisal from [HM Treasury's Green Book](https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government/the-green-book-2026); this research workflow is our synthesis, not a named upstream skill.

## 3. Value and adoption

Adapt the Green Book's Five Case Model: strategic fit, comparative value, commercial feasibility, affordability and delivery. Trace intervention → behavior → outcome → value; record baselines, ranges, evidence, costs, displaced work, adoption friction, incentives, owners and the commitment needed now.
Separate released capacity from cash savings; avoid double-counting benefits. Use a proportionate comparison to distinguish impact from what would have happened anyway.
Optionally use [Amazon Working Backwards](https://www.aboutamazon.com/news/workplace/an-insider-look-at-amazons-culture-and-processes) to clarify a proposed customer experience and its feasibility through PR/FAQ. Keep this exploration here; it is distinct from a decision memo. Apply section 6's authorship rules to narrative prose, not analytical case maintenance.

## 4. Validation

Test the most uncertain assumption capable of changing the decision. Adapt [Strategyzer's Test Card](https://www.strategyzer.com/library/validate-your-ideas-with-the-test-card): hypothesis, test, measure, threshold.
Add cost, owner, duration, stop criteria and the decision triggered by each result. Keep original predictions beside observations; do not require a pilot when existing evidence is sufficient.

## 5. Narrative structure

Choose according to the audience and decision; do not create both formats by default or conceal unresolved weaknesses in the case.
For a presentation, adapt [Sumeet Gayathri Moghe's Nail your narrative](https://martinfowler.com/articles/never-send-slides/nail-your-narrative.html): central idea and stakes → audience and takeaways → fitting storyline → explain without visuals → storyboard only if needed.
For a decision memo, adapt [Amazon's narrative practice](https://www.aboutamazon.com/news/company-news/2017-letter-to-shareholders): a self-contained prose argument, iteratively reviewed, that supports informed discussion without a presenter. Use six pages only when requested or appropriate; there is no universal section template here.
An outline covering decision, evidence, alternatives, value, adoption, risks and commitment is our adaptation. Structure the argument here; keep its prose in section 6.

## 6. Working draft and critique

Adapt [Thomas Ptacek's How To Write With An LLM](https://sockpuppet.org/blog/2026/09/17/how-to-write-with-an-llm/): the user writes or dictates; identify specific problems without praise or replacement prose; the user revises.
Work in useful passes over argument, order, clarity and repetition. When comparing versions, use a fresh context without revision labels if available; never claim a blind comparison otherwise. Explain criticism and leave editorial choices to the author.
If the user requests drafting or rewriting, comply and label the switch "Assisted drafting"; do not call that Ptacek's method or require another confirmation.

## 7. Outcome and learning

Adapt [HM Treasury's Magenta Book](https://www.gov.uk/government/publications/the-magenta-book/magenta-book-central-government-guidance-on-evaluation-html): compare intended mechanisms, actual adoption, costs and outcomes; examine attribution and alternative explanations.
Use section 4's original forecasts. Separate outcome quality from decision quality; record what to continue, change or stop and one reusable lesson. Update the recommendation and next move.

These are attributed adaptations of practitioner methods, not author-endorsed skills or proof of effectiveness. Use source detail when it changes the work; do not reread every source each session. Let the model choose depth and technique within this contract.
