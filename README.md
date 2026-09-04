# Enterprise Infrastructure Orchestrator v1.3.4 — Public submission kit

This repository is prepared for the **OpenAI public Plugin Directory submission route** for a **skills-only plugin**.

## Why this route

A personal Plus account cannot use the managed-workspace GitHub marketplace import path as a private web-distribution shortcut. Public publication is the route that can make this plugin installable from the universal Plugins Directory and therefore invokable with `@` on supported ChatGPT web surfaces after approval and installation.

## Repository contents

- `.codex-plugin/plugin.json` — publication-oriented plugin manifest.
- `skills/enterprise-infrastructure-orchestrator/` — the final v1.3.4 Skill bundle.
- `assets/` — publication icons.
- `docs/` — GitHub Pages-ready website, privacy policy, terms, and support pages.
- `submission/` — copy/paste listing text, starter prompts, 5 positive tests, 3 negative tests, and release notes.
- `configure-publisher.ps1` — replaces publisher placeholders with your GitHub username and verified publisher name.
- `validate-submission.ps1` — local structural/preflight validation.
- `build-zips.ps1` — creates final plugin and skill ZIPs after publisher configuration.

## Prepare the repository

1. Run:
   `powershell -ExecutionPolicy Bypass -File .\configure-publisher.ps1 -GitHubUsername "YOUR_USERNAME" -PublisherName "YOUR VERIFIED NAME"`
2. Create a GitHub repository named `enterprise-infrastructure-orchestrator` and upload/push this folder.
3. Enable GitHub Pages from the `/docs` folder on your default branch.
4. Confirm these URLs load publicly:
   - `/`
   - `/privacy.html`
   - `/terms.html`
   - `/support.html`
5. Run:
   `powershell -ExecutionPolicy Bypass -File .\validate-submission.ps1`
6. Run:
   `powershell -ExecutionPolicy Bypass -File .\build-zips.ps1`

## Submit to OpenAI

In the OpenAI Platform plugin submission portal:

1. Ensure the publishing organization gives you **Apps Management: Write** permission.
2. Complete individual or business developer identity verification.
3. Create a new **Skills only** plugin submission.
4. Use `submission/listing-and-urls.md` for listing fields.
5. Upload `dist/enterprise-infrastructure-orchestrator-skill-v1.3.4.zip` on the Skills tab.
6. Add the starter prompts from `submission/starter-prompts.md`.
7. Add the five positive and three negative tests from `submission/test-cases.md`.
8. Choose supported countries/regions.
9. Paste `submission/release-notes.md` into the release notes field.
10. Complete the policy attestations and submit for review.

After OpenAI approves the submission, publish it from the portal. Once published, it appears in the universal Plugins Directory. Install it in ChatGPT web, then invoke it with `@Enterprise Infrastructure Orchestrator` where the `@` plugin control is supported.

## Important

The policy/terms pages are publication-ready drafts but are not legal advice. Review them before publishing under your identity.
