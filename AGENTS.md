# Project instructions

Read docs/PROJECT.md, docs/MILESTONES.md and docs/WORKFLOW.md before making changes.

## Scope
Build a fresh LegitimateHosting website and customer platform. Do not reuse the old Phox theme, plugins or executable code. The existing hosting services must remain operational.

## Development
- Work on a task branch; inspect current files before editing.
- Keep changes small and document the purpose and verification in a pull request.
- Check current official documentation before selecting framework versions.
- The production host has no confirmed usable Node.js runtime or shell access. Do not require either for the deployed website without revisiting the deployment plan.
- Never assume a PHP dropdown proves framework compatibility.
- Keep the public web directory separate from application code, secrets and storage.
- Use synthetic data in development.
- Keep credentials, .env files, customer exports, database dumps and hosting backups out of Git, including private repositories.
- Do not connect live Paystack, WHM or registrar credentials during initial development.
- Verify HTTPS and correct account routing before testing credentials or payment workflows on staging.
- Do not deploy to production, migrate customer accounts, change DNS or trigger hosting suspension/deletion as part of routine code changes.

## Handoff
Report changed files, verification results, unresolved limitations and the exact next task.
Do not claim payment, provisioning, SSL, backups or deployment work unless actually verified.
