# Work validation — 2026-09-21

## Scope and result

A native personal-skill execution path for `strategy-factory` is verified in ChatGPT Work. The complete repository plugin is **not** verified as an installed plugin. The user subsequently tested the ordinary iPhone Chat picker: typing `@st` showed Study but did not show `strategy-factory`. That picker check did not pass. Instruction loading in ordinary iPhone Chat remains unverified.

Source inspected: `main` at `bb17e5427e4800e3ca9534c6ed6cf7efa63ddbce`, plugin version `0.1.1`. No repository-local `AGENTS.md` was present in the recursive tree. All eight skills, manifests, installation guidance, case template, and evaluation criteria were read. This report does not change the methodology or package version.

## Observable loading and installation

Before any changes, the Work session advertised the existing personal `strategy-factory` skill. An actual `skills.read` call returned its complete instructions, and `skills.list` returned its name, description, and resource. This is tool-return evidence of instruction loading, independent of the quality of a coaching answer.

That existing copy differed from the canonical core only in its Markdown title. Its display metadata also used spaces. The title and display metadata were updated in place; the existing skill was not uninstalled. This does not establish that naming caused the earlier launch failure.

The seven canonical specialist skills were installed through the native personal-skill workflow. Each install was saved separately and checked after reconciliation. The final stored and local `SKILL.md` content for all eight matched the pinned canonical source byte for byte.

The current conversation retained cached skill resources: after the core update, `skills.read` still returned the previous heading, while the saved and filesystem copies contained the corrected heading. A direct resource read for a newly installed specialist returned “skill package is not available.” New-session discovery of those seven specialists is therefore not verified. The current session can read their installed files directly.

## Validation gates

| Gate | Result | Evidence / boundary |
|---|---|---|
| Eight skill files | Passed | Official minimal validator ran on each actual installed directory; YAML, required fields, and names passed. |
| Canonical content integrity | Passed | Git blob hashes matched fetched GitHub metadata; installed content equaled canonical content. |
| Standalone archive construction | Passed for reconstructed archives | Eight in-memory ZIPs each contained exactly `<name>/SKILL.md`; CRC and content checks passed. The historical uploaded ZIP was unavailable. |
| Portable manifest | Static checks passed | JSON parsed; present fields checked against published Agent Plugins 1.0 schema constraints. This was a manual constraint check, not a host acceptance test. |
| Marketplace | Static checks passed | Plugin identity, `./` source path, root manifest, policy fields, and eight skills were consistent. |
| Native skill storage | Passed | Existing core updated and seven specialists saved; stored contents verified after reconciliation. |
| Core Work availability/loading | Passed | Initial session catalog plus actual `skills.list` and `skills.read` results. |
| New specialist catalog loading | Not verified | Current skill reader did not expose the newly installed specialist tested. |
| iPhone Chat picker | Did not pass | User screenshot shows `@st` with Study as the only visible suggestion; no `strategy-factory` entry. This does not establish the cause. |
| Try in chat after update | Not verified | No new observation of this control. |
| Complete plugin install | Not verified | No custom repository-registration tool or plugin-creator skill exposed; `codex` absent from PATH; directory search found no matching plugin. |
| Ordinary ChatGPT / iPhone | Not verified | Work evidence cannot pass these gates. |
| Copilot / Claude consumer app | Not verified | No runtime tests on those hosts. |

Core canonical SHA-256: `1c3bb295fe907fc722606b733db99f2eff3a4eea3fc1826f801619c9ff550937`.

## Coaching smoke tests

Tests used fresh Work subagents with no inherited conversation history and the installed core instructions. These are bounded behavior checks, not proof of mobile availability or a complete compatibility certification. The precise runtime model identifier was not independently exposed; no model-specific compatibility claim is made.

### 1. Solution-first opening

Prompt: “I want to build a service that helps homeowners keep track of all their home maintenance. Help me develop this idea.”

Output asked for a concrete maintenance situation and how the homeowner handled it, rather than endorsing a product. One substantive question was asked. The test reported loading the installed file through a successful shell read; its subsequent file hash matched the canonical core.

### 2. Weak value case and premature pitch

Prompt supplied eight staff, estimated savings of 10–30 minutes each weekly, a 120–200-hour build, 2–4 hours weekly ownership, an adequate checklist, no owner, and no measured operational benefit. It requested an executive pitch and asked whether to seek approval.

Output: “No—don’t ask for build approval on the current evidence.”

The response calculated 1.3–4 gross hours saved weekly and approximately −2.7 to +2 net hours after ownership. It labeled the inputs as estimates, distinguished staff hours from economic value, and recommended deferral. The favorable 60–100-week effort recovery scenario was explicitly conditional. It supplied a defer recommendation instead of manufacturing a build pitch.

A follow-up supplied the decision to defer and requested a checkpoint. The response retained the estimates, evidence gaps, alternatives, reopening conditions, owner/adoption requirements, and next move.

### 3. Research and existing alternatives

Prompt: a 12-person volunteer club misses recurring chores; investigate established methods and existing implementations with assignment, due dates, recurrence, and low setup.

The response researched GTD and Kanban, compared Microsoft To Do, ClickUp, and Trello, recommended testing an existing tool, distinguished proposed success thresholds from findings, and asked whether someone could own the weekly review.

The test reported actual web search, open, and find calls. Research was performed rather than delegated back to the user. Limitation: several product feature/plan claims rested on primary-source search excerpts because opened pages did not expose supporting text. This passes the research-action check, not a comprehensive source-audit gate.

### 4. Checkpoint resumption and pilot criteria

A separate fresh test received a supplied checkpoint of the deferred dashboard case. New information assigned an owner for one hour weekly, without new savings measurements. The proposed pilot success criterion was “dashboard completed and viewed by everyone.”

The response retained deferral, identified the gap between the owner's one-hour capacity and the estimated 2–4-hour burden, rejected completion/views as evidence of incremental value, and proposed baseline, outcome, capacity, and decision criteria. It ended with one consequential question.

### 5. Implicit selection probe

A fresh test received only a short homeowner-service idea prompt, without the skill name or path. It reported selecting `strategy-factory` and reading it with `skills.read`, and produced a relevant one-question opening.

This is encouraging but remains **limited evidence**: the parent received the child's execution report, not an independently exported full child tool trace. Do not treat the answer or self-report alone as a passed automatic-discovery gate. No UI-selected invocation was tested.

## Next verification

The useful execution path today is the installed core in Work. No repeated upload or reinstall is indicated by these results.

The requested ordinary iPhone Chat picker check has now been performed and did not expose the skill. Do not ask the user to repeat it without a material installation or registration change. The next investigation concerns the complete plugin's account/workspace registration and distribution.

Keep the seven specialists' fresh-session discovery and complete-plugin registration as separate checks. Do not interpret native-skill installation as plugin installation, and do not interpret a repository change as an update to an imported copy.

## Sources

- [Build skills](https://learn.chatgpt.com/docs/build-skills): native skill creation and instruction loading.
- [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins): explicit and implicit use.
- [Package your plugin](https://developers.openai.com/plugins/build/plugins): portable manifests and local marketplace registration.
- [Connect and test your plugin](https://developers.openai.com/plugins/deploy/connect-chatgpt): separate installed-plugin testing.
- [Agent Plugins manifest schema](https://agent-plugins.org/schemas/1.0.0/plugin.schema.json): static manifest constraints.

## Registration investigation follow-up

The live ChatGPT Plugins page opened in the dedicated cloud browser, but the browser was signed out. Account-specific management controls cannot be assessed until secure sign-in completes. This browser limitation is not evidence of an account restriction or the cause of the iPhone issue.

Current official documentation separates three routes:

- Local/repository marketplaces: supported local development and testing; not proof of ordinary iPhone availability.
- Workspace publication/import: workspace-managed distribution; publication requires workspace administration rights.
- Public directory: skills-only submissions are supported, but require publisher verification, listing materials, review, and publication. This route has not been initiated.

For personal use, public-directory publication is additional work, not a demonstrated prerequisite. Check the account's actual management options before choosing a distribution route. No package rewrite, MCP service, subscription upgrade, or repeat ZIP upload is justified by the current evidence.

Sources: [packaging and workspace publication](https://developers.openai.com/plugins/build/plugins), [public submission](https://developers.openai.com/plugins/deploy/submission).
