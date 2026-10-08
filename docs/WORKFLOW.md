# Collaboration and local setup

## Responsibilities
- Project owner: business content, account access, team invitations and production decisions.
- Coding assistant: implementation, documentation, reviews and clear next tasks.
- Team member: assigned task branches and pull requests.
- Antigravity: local editing and execution environment using this repository.

## Open the foundation branch
1. In GitHub Desktop, select this repository and click Fetch origin.
2. Use Current Branch to choose setup/project-foundation.
3. Open the repository folder in Antigravity.
4. Read AGENTS.md and the documents under docs/.

The foundation branch is not yet merged into main. Do not discard or overwrite local uncommitted work when switching branches; report it first.

## First local check
In the terminal on your own computer (not cPanel), run each command separately:

```text
git --version
php --version
composer --version
node --version
npm --version
```

Send the outputs or the exact missing-command errors. These commands inspect installed tools. Do not install or upgrade software until the results establish what is needed.

## Daily collaboration
Start from the agreed base branch, fetch/pull the latest work, and create a branch named feature/short-description or fix/short-description. Agree who owns a task before editing the same feature. Review changed files, commit the work, push the branch, and open a pull request with the problem, changes and verification. Merge reviewed work through the agreed owner.

A commit records changes locally; a push uploads commits to GitHub; a pull downloads and integrates remote changes. Antigravity edits are not visible on GitHub until pushed. GitHub does not automatically share this chat history with Antigravity.

## Deployment
No automatic production deployment is configured. Source checkout and web deployment are separate. Never upload the entire repository into public_html. public/ is reserved for intended web-visible files; dependencies and secrets require the selected backend's verified layout.

## Team access
The owner can invite the teammate using GitHub repository access settings. Use individual GitHub accounts rather than shared credentials. Making the repository private later still allows explicitly invited collaborators to work on it. No invitation has been sent by the assistant.
