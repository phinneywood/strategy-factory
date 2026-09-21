# ChatGPT installation

## Verified status — 2026-09-21

The existing core `strategy-factory` personal skill was discoverable and its full instructions loaded in ChatGPT Work. Its title/display metadata were aligned with the repository. The seven specialists were then installed through Work's native personal-skill workflow. All eight saved instruction files match repository version 0.1.1.

**This verifies a native skill path in Work, not the complete plugin or ordinary ChatGPT/iPhone availability.** The current conversation's cached skill reader did not expose the newly installed specialist tested. Fresh-session specialist discovery remains unverified.

See [the execution record](../evals/work-validation-2026-09-21.md) for evidence, coaching smoke tests, and limitations. No coaching instructions or package version changed.

## Native personal skills

Work's built-in skill-creator provides a supported route to create, update, and install personal skills. In this session it could update the existing core in place and install the remaining canonical `skills/*/SKILL.md` files. Installation is separate from the repository plugin manifest.

Maintain the methodology in this repository. Imported copies are deployment artifacts: changing GitHub alone does not update them. Do not create host-specific copies of the coaching method.

The earlier standalone-upload launch failure remains unexplained. Successful loading in Work does not identify its cause. The observed naming mismatch is not evidence of causation.

## Complete plugin: documented local route, not executed here

The root `plugin.json`, shared `skills/`, and `.agents/plugins/marketplace.json` follow the documented package structure. The package is skills-only and does not require an MCP server.

OpenAI documents this marketplace-registration command:

```sh
codex plugin marketplace add phinneywood/strategy-factory --ref main
```

This command registers a source; it does not by itself prove installation or invocation. The documented local route then uses the supported ChatGPT desktop plugin directory to select the marketplace and install the plugin.

The Work environment tested here had no `codex` executable, no exposed plugin-creator skill, and no custom repository-registration action. The command was not executed. Installing a CLI into this remote environment would not establish ordinary-chat or iPhone availability.

Do not upload the complete repository into the standalone-skill uploader or infer that local marketplace registration syncs to another client.

## Surface boundaries and remaining check

Current documentation describes plugin-provided skills across supported Chat and Work surfaces, including mobile. Its standalone-skill availability description is narrower. These general descriptions do not establish that this account's personal upload is available in ordinary iPhone chats.

For the outstanding mobile check, use one new ordinary ChatGPT conversation in the same account/workspace. Check whether `strategy-factory` appears in the `@` picker and, if selected, whether its instructions actually load. Do not use coaching fluency as the loading test.

Workspace import and public-directory publication are separate distribution routes. Neither was performed. No plan upgrade, repeated reinstall, or additional infrastructure is justified by this evidence.

## Sources

Checked 2026-09-21:

- [Native skills and creation](https://learn.chatgpt.com/docs/build-skills)
- [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins)
- [Package and marketplace documentation](https://developers.openai.com/plugins/build/plugins)
- [Complete-plugin testing](https://developers.openai.com/plugins/deploy/connect-chatgpt)
