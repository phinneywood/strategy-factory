# Cross-platform compatibility

Strategy Factory's portable contract is the Agent Skills content under `skills/`. Essential methodology must not depend on host-specific configuration.

## Target hosts

| Capability | ChatGPT | GitHub Copilot | Claude app |
|---|---|---|---|
| Discover portable `SKILL.md` guidance | Test | Test | Test |
| Run the complete Idea Development method | Test | Test | Test |
| Select a specialist skill from user intent | Test | Test | Test |
| Research with available host tools | Test | Test | Test |
| Preserve facts vs assumptions vs judgments | Test | Test | Test |
| Reach stop/defer as a valid conclusion | Test | Test | Test |
| Resume from a case checkpoint | Test | Test | Test |

## Acceptance rule

A host is compatible when the behavioral scenarios in `scenarios.md` produce materially equivalent strategic behavior. Exact wording, tool calls, and plugin packaging do not need to match.

## Design constraints

- Keep essential behavior in portable skills.
- Do not require one skill to explicitly invoke another.
- Add host-specific adapters only for a demonstrated capability gap.
- Do not fork the methodology by host.
- Treat marketplace/install metadata as packaging, not product logic.
