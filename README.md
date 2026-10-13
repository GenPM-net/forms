# @core/forms

[![genpm](https://api.genpm.net/v1/badge/@core/forms.svg)](https://genpm.net/p/@core/forms) ![license](https://img.shields.io/badge/license-MIT-blue)

> Forms and lead capture: code or admin-built forms, spam checks, GDPR consent, email alerts, signed webhooks, CSV

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/forms`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/forms
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/forms`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/forms with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Contact and lead forms end to end: forms defined in code (`defineForm` with zod) or built by editors in the admin
(`forms` content collection), anti-spam (@core/antispam), GDPR consent with a versioned text, stored submissions with
source page and campaign parameters, and background processing (@core/jobs): team alert email, auto-reply,
HMAC-signed webhook and `onSubmission` handlers. CSV export, retention and erasure helpers. Table: `form_submissions`.

## At a glance

- **GenPM dependencies** (installed with it): [@core/db](https://genpm.net/p/@core/db), [@core/antispam](https://genpm.net/p/@core/antispam), [@core/email](https://genpm.net/p/@core/email), [@core/jobs](https://genpm.net/p/@core/jobs), [@core/content](https://genpm.net/p/@core/content), [@core/contracts](https://genpm.net/p/@core/contracts)
- **npm dependencies** (proposed, never installed without asking): `zod`
- **Environment variables** (added to `.env.example`): `FORMS_NOTIFY_TO`, `FORMS_WEBHOOK_SECRET`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/forms`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
