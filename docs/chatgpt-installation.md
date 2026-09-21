# ChatGPT installation

## Status

Version 0.1.1 adds a repository marketplace and explicit OpenAI display metadata. The eight skill instructions are unchanged. The repository root is the complete skills-only plugin; no MCP server, hosted backend, or credential is required by this package.

**This is packaging work, not a verified fix for standalone-skill launch failures.** Local metadata checks are not a ChatGPT runtime test. No public directory submission or account installation has been performed.

## Documented local test route

OpenAI documents repository marketplaces for Work mode or Codex in the ChatGPT desktop app. With Codex CLI available, register this repository as a marketplace source:

```sh
codex plugin marketplace add phinneywood/strategy-factory --ref main
```

Restart the ChatGPT desktop app. In its supported local Work/Codex interface, open the Plugins Directory, select `strategy-factory-local`, and install `strategy-factory`. The marketplace points to `./`, the repository root, which contains the manifest and all eight skills. The path is relative to the marketplace root, not to `.agents/plugins/`.

The marketplace's required authentication policy is metadata. This skills-only package has no connected service to authenticate.

Do not upload the entire repository to the standalone Skills uploader. That is a different installation route. Do not assume a local desktop installation syncs to ordinary web or iPhone chats.

## End-to-end acceptance

First verify the installed plugin can be selected and that its skill instructions actually load. Only then test coaching and automatic selection. Use `evals/compatibility.md` and `evals/scenarios.md`; retain client, model, package version, prompt, and observable loading evidence. A fluent response alone does not prove skill invocation.

## Other distribution routes

Workspace publication requires the appropriate workspace administration access. Public-directory distribution requires a separate submission and review. Neither happens by committing this repository. Ordinary iPhone availability remains unverified; no plan upgrade is recommended on the basis of packaging alone.

## Sources

Checked 2026-09-21:

- [Package and marketplace documentation](https://developers.openai.com/plugins/build/plugins)
- [Complete-plugin testing](https://developers.openai.com/plugins/deploy/connect-chatgpt)
- [Public submission](https://developers.openai.com/plugins/deploy/submission)
- [Standalone Skills and surface availability](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)
