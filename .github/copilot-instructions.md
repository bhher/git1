# Copilot / AI Agent Instructions — Minimal placeholder repo

Summary
- This repository is a minimal/placeholder project that currently contains three text files: `work1.txt`, `work2.txt`, and `work3.txt`.
- There is no build system, runtime, or CI configured by default. The repo structure is simple and intentionally minimal.

Big picture & architecture
- Current components:
  - `work1.txt`, `work2.txt`, `work3.txt` — simple text artifacts. Each file is a single-line entry representing a small unit of content.
  - `.git/` — repository metadata.
- Why structure is minimal: This repository appears to be a placeholder or an early-stage workspace; there are no services, libraries, or dependencies.

How AI agents can be productive here
- Validate the repository contents: check `work1.txt`, `work2.txt`, and `work3.txt` for missing or erroneous content.
- When adding new code, follow the project's implied minimal structure: add a top-level directory named after the language or feature (e.g., `src/` for code, `tests/` for tests, `docs/` for docs).
- If you add a language-specific project (Python, Node, etc.), add standard manifests (`pyproject.toml`, `package.json`, etc.) and update this file with the relevant build/test commands.

Developer workflow (Windows PowerShell examples)
- Create a new branch and commit a change:
```powershell
# Create a feature branch
git checkout -b feature/add-work4
# Edit or add work4.txt
New-Item work4.txt -Value "4"
# Stage and commit
git add work4.txt
git commit -m "feat: add work4.txt"
# Push
git push -u origin feature/add-work4
```

- Create PRs with descriptive titles and short descriptions. If you add new directories or build files, include quick usage or test commands in the PR description.

Conventions & Patterns
- File naming: existing files follow the `workN.txt` naming pattern; retain this pattern for similar artifacts.
- Minimal commits: keep each commit focused (one logical change per commit), with a short title and optional extended description.
- Branch naming: `feature/*`, `fix/*`, `chore/*` is preferred for changes.
- Tests: There are no tests in the repo. If you add code, add tests under `tests/` and include commands for running tests in the `README.md`.

Integration points & external dependencies
- There are none currently. If you add an integration with an external service or CI, document it in `README.md` and update this instruction file to list environment variables, required secrets, and any setup steps.

When to suggest changes to humans
- If you want to introduce a build system, CI, or dependencies, propose those changes via a PR and include the following:
  - A brief rationale (why the change is needed)
  - The minimal set of files to add (e.g., `pyproject.toml` + `requirements.txt` or `package.json`) and UX for running and testing
  - Any required GitHub Actions or workflow files (`.github/workflows/`)

Examples
- Add a new work file and update repo:
```powershell
New-Item work4.txt -Value "4"
git add work4.txt
git commit -m "feat: add work4.txt"
git push -u origin feature/add-work4
```
- Add a README if adding code or tests (when you add `src/` or `tests/`):
```powershell
New-Item README.md -Value "# Project Title`nShort description and run instructions."
git add README.md
git commit -m "docs: add README"
```

Rules for AI agents
- Maintain minimal, incremental changes — don’t propose sweeping restructures without discussion.
- Document any new commands, external integrations, or architecture additions in `README.md` and `README.md` or this file.
- Keep the repository stable: if you add build files, ensure they are minimal and reversible in a single commit.
- If you are unsure about a structural choice, leave a PR comment explaining the reasoning and a suggested approach.

Questions for maintainers
- Is this repo intended as a placeholder for a larger project or small content store? Knowing the intended direction helps prioritize next steps (e.g., add CI, language-specific layout).
- Preferred branching & PR review policy (reviewers, required approvals)?

If you want a more opinionated Copilot/AI agent behavior for specific languages (Python/Node/C#), tell me which languages or frameworks you expect in this repository and I’ll add more concrete commands and conventions.
