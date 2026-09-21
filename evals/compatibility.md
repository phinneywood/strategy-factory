# Cross-platform compatibility

The portable contract for `strategy-factory` is the Agent Skills content under `skills/`. Essential methodology must not depend on host-specific configuration.

## Installation preflight

Validate these gates separately and in order:

1. **Package:** confirm the skill directory, frontmatter `name`, and top-level heading use the same lowercase, hyphen-separated name. Validate archive structure and integrity.
2. **Upload/install status:** inspect the host's actual installed and review status. An upload-success notification alone does not pass this gate.
3. **Availability:** confirm the skill is exposed to a new conversation in the intended account, workspace, and client. Record the client and model used; do not assume availability carries between surfaces.
4. **Explicit invocation:** select the skill in the host's supported picker and confirm that its instructions were actually loaded. A plausible answer or a model saying it used the skill is not sufficient evidence on its own.
5. **Automatic selection:** only after explicit invocation works, start a separate fresh conversation with a relevant request that does not name the skill.
6. **Behavior:** only after loading is established, run the coaching scenarios.

Record the evidence and outcome of each gate as passed, failed, or not verified. A failure at an earlier gate leaves later gates not verified; it does not establish that a description or coaching prompt is defective.

### ChatGPT checks

OpenAI documents separate installed/created skill views, post-upload scanning, and possible Needs Review or Blocked states. It also notes that availability and syncing can vary by surface. Inspect those states before changing the package. OpenAI documents explicit skill selection through @-mentions; test that before relying on automatic selection.

Sources, checked 2026-09-21:
- https://help.openai.com/en/articles/20001066-skills-in-chatgpt
- https://openai.com/academy/skills/

These checks describe how to test installation, not a claim that any particular account has passed.

## Work verification — 2026-09-21

The existing native core loaded through the Work skill reader. All eight canonical skills are now saved as personal skills; fresh-session discovery of the seven newly installed specialists remains unverified. Coaching smoke tests were run after core loading. The complete plugin and ordinary ChatGPT/iPhone paths remain unverified. See [the detailed evidence](work-validation-2026-09-21.md).

The matrix below refers to full intended-host compatibility, not the narrower Work result.

## Target hosts

| Capability | ChatGPT | GitHub Copilot | Claude app |
|---|---|---|---|
| Discover portable `SKILL.md` guidance | Not verified | Not verified | Not verified |
| Run the complete idea-development method | Not verified | Not verified | Not verified |
| Select a specialist skill from user intent | Not verified | Not verified | Not verified |
| Research with available host tools | Not verified | Not verified | Not verified |
| Preserve facts vs assumptions vs judgments | Not verified | Not verified | Not verified |
| Reach stop/defer as a valid conclusion | Not verified | Not verified | Not verified |
| Resume from a case checkpoint | Not verified | Not verified | Not verified |

## Acceptance rule

A host is compatible when the behavioral scenarios in `scenarios.md` produce materially equivalent strategic behavior. Exact wording, tool calls, and plugin packaging do not need to match.

## Design constraints

- Keep essential behavior in portable skills.
- Keep the core method usable without specialist loading. Supported bundled-entry coordination is allowed; do not fork the methodology by host.
- Add host-specific adapters only for a demonstrated capability gap.
- Do not fork the methodology by host.
- Treat marketplace/install metadata as packaging, not product logic.
