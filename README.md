# Shareable AI Notes Workflow

This repository is a small, generic Obsidian vault for daily notes, lightweight project organization, regular review, and AI-assisted reflection.

It started from Mark Bakke's AI-native Obsidian workflow. The source material was adapted into a portable baseline rather than copied as a personal or company-specific system.

## Branches

- `main` is the generic starter vault.
- A `shea` branch can add folders and guidance for Shea without changing the baseline.
- Future `engineering` or `advanced` branches can be created from `main` when needed.

Each branch is intended to be a complete vault. Open the branch's working tree directly in Obsidian and archive it with Git when you want to share or distribute it.

## Getting started

1. Open this repository's root directory as an Obsidian vault.
2. Read `AGENTS.md` and `Cheat Sheets/Quick Start.md`.
3. Review `000 Workflows/000 Daily Workflow.md`.
4. Create a daily note from `Templates/Daily Notes Template.md`.
5. Commit useful checkpoints with Git when convenient.

The vault can live in Dropbox or another synchronized folder for access from multiple devices. Git commits are still best made from a computer where Git is configured.

## AI tools

`AGENTS.md` contains the portable vault guidance. `cursor.md` is a Cursor-specific adapter; other tools can use `AGENTS.md` or their own small adapter file. Do not replace a computer's host-level `AGENTS.md` with this file unless that is an intentional choice.

## Updating a variation

Keep generic improvements on `main`. To bring them into a variation:

```text
git switch <variation>
git merge main
```

Review the merge before publishing the variation. Keep branch-specific files and folders clearly separated from generic workflow files.

## Publishing a branch

From the repository's parent directory:

```text
git archive --format=tar.gz --output=<variation>.tar.gz <variation>
```

Before sharing an archive, check `Reference/VARIATION.md`, remove private material, and verify that the branch contains no credentials, company-specific notes, or personal history.
