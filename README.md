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
2. Read [Quick Start](Cheat%20Sheets/Quick%20Start.md). It is the only onboarding guide.
3. Read the human-facing [Daily Rolling Guide](Cheat%20Sheets/Daily%20Rolling%20Guide.md).
4. AI tools should follow the [Daily Workflow — AI Instructions](000%20Workflows/000%20Daily%20Workflow.md).
5. Create a daily note from the [Daily Notes Template](Templates/Daily%20Notes%20Template.md).
6. Commit useful checkpoints with Git when convenient.

The vault can live in Dropbox or another synchronized folder for access from multiple devices. Git commits are still best made from a computer where Git is configured.

## AI tools

`AGENTS.md` contains the portable vault guidance. `cursor.md` is a compatibility redirect for Cursor and does not add separate rules. Do not replace a computer's host-level `AGENTS.md` with this file unless that is an intentional choice.

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
