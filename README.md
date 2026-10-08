# Shareable AI Notes Workflow

This repository is a small, generic Obsidian vault for daily notes, lightweight project organization, regular review, and AI-assisted reflection.

It started from Mark Bakke's AI-native Obsidian workflow. The source material was adapted into a portable baseline rather than copied as a personal or company-specific system.

## Getting started

1. Open this repository's root directory as an Obsidian vault.
2. Read [Quick Start](Cheat%20Sheets/Quick%20Start.md). It is the only onboarding guide.
3. Read the human-facing [Daily Rolling Guide](Cheat%20Sheets/Daily%20Rolling%20Guide.md).
4. AI tools should follow the [Daily Workflow — AI Instructions](000%20Workflows/000%20Daily%20Workflow.md).
5. Create a daily note from the [Daily Notes Template](Templates/Daily%20Notes%20Template.md).
6. Commit useful checkpoints with Git when convenient.

The repository includes optional Obsidian community plugins, but they are disabled by default. See [Obsidian Setup](Reference/Obsidian%20Setup.md) before enabling or removing them.

The vault can live in Dropbox or another synchronized folder for access from multiple computers after the setup is tested on one computer. Mobile syncing has platform-specific limitations; see the sync guidance in [Quick Start](Cheat%20Sheets/Quick%20Start.md). Git commits are still best made from a computer where Git is configured.

## Branches and variations

- `main` is the generic starter vault.
- A `shea` branch can add folders and guidance for Shea without changing the baseline.
- Future `engineering` or `advanced` branches can be created from `main` when needed.

Each branch is intended to be a complete vault. Open the branch's working tree directly in Obsidian and archive it with Git when you want to share or distribute it. See [VARIATION](Reference/VARIATION.md) for the branch metadata convention.

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

From the repository root, archive a clean committed branch from its parent directory:

```text
git archive --format=tar.gz --prefix=shareable-vault/ --output=../<variation>.tar.gz <variation>
```

Before sharing an archive, check `Reference/VARIATION.md` and `Reference/PROVENANCE.md`, confirm source attribution and licensing for adapted material, remove private material, and verify that the branch contains no credentials, company-specific notes, or personal history. Git archives include committed files only, so review `git status` and the archive contents before distributing it.
