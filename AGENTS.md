# Repository Guidelines

## Project Structure & Module Organization
This repository currently contains GitHub-facing project metadata and automation. Keep top-level files focused on contributor and process documentation.
- `.github/workflows/`: GitHub Actions workflow files.
- `.github/`: repository-level guidance (including this file).
- `docs/` (optional): longer design notes or process docs.

Use clear, purpose-based filenames, for example `ci.yml`, `release.yml`, or `security-policy.md`.

## Build, Test, and Development Commands
There is no application build step in this repository yet.
Use these commands during development:
- `git status` - confirm tracked changes before committing.
- `git diff` - review exact edits.
- `rg "pattern" .` - quickly search for references before changing shared terms.
- `npx markdownlint-cli2 "**/*.md"` (if installed) - validate Markdown formatting.

If workflows are added, include local validation commands in workflow comments or `README`.

## Coding Style & Naming Conventions
- Use Markdown with concise sections and actionable instructions.
- Prefer 80-100 character line lengths for readable diffs.
- Use lowercase, hyphenated names for workflow files (for example, `pull-request-checks.yml`).
- Use descriptive IDs and job names in Actions (`lint`, `test`, `release`).

## Testing Guidelines
This repo has no runtime test suite yet. Validate changes by:
- Checking Markdown rendering in GitHub preview.
- Running any workflow lints available locally.
- Verifying new workflow YAML with a dry run strategy before merge.

When tests are introduced, place test-related tooling config at repo root and document exact commands here.

## Commit & Pull Request Guidelines
No commit history exists yet, so use a consistent convention from the start:
- Commit format: `type(scope): short summary` (example: `docs(guidelines): add contributor guide`).
- Keep commits focused to one concern.

For pull requests:
- Provide a short problem/solution description.
- Link related issues (`Closes #<id>`) when applicable.
- Include screenshots only for UI/document rendering changes where useful.
- Confirm what was validated locally (commands and results).
