# Vault Variation

## Identity

- **Variation:** Generic starter baseline
- **Branch:** `main`
- **Base:** An AI-native workflow created by Mark Bakke, adapted for a portable vault
- **Audience:** Anyone who wants a small daily-note and review system

## Purpose

This branch is the stable, generic starting point for complete vault variations. It should remain small enough to understand and useful without personal history, company context, or specialized tooling.

## Changes from the source

- Flattened the vault contents to the repository root so the repository is directly usable as an Obsidian vault.
- Kept daily, weekly, and monthly review ideas, templates, lightweight agents, and Git guidance.
- Removed personal/company context and bookmark-management automation.
- Added portable `AGENTS.md` guidance and branch/publishing documentation.
- Kept optional community plugins in the edition but disabled them by default; see [Obsidian Setup](Obsidian%20Setup.md).

## Branch model

- `main` is the generic starter vault.
- A variation branch can add folders and guidance for a specific use case without changing the baseline.
- Future specialized branches can be created from `main` when needed.

Each branch is intended to be a complete vault. Open the branch's working tree directly in Obsidian, and archive it with Git when you want to share or distribute it. Keep the branch's purpose and branch-specific changes recorded in this file.

## Variation policy

Create a variation branch from `main` when a use case needs additional folders or guidance. Keep generic fixes on `main`, then merge them into the variation deliberately.

## Updating a variation

Keep generic improvements on `main`. To bring them into a variation:

```text
git switch <variation>
git merge main
```

Review the merge before publishing the variation. Keep branch-specific files and folders clearly separated from generic workflow files.

## Publishing a branch

This section is for users who are comfortable with Git. Beginners can use a checked-out branch or an archive prepared by someone else without needing to manage variations themselves.

From the repository root, archive a clean committed branch from its parent directory:

```text
git archive --format=tar.gz --prefix=durable-context/ --output=../<variation>.tar.gz <variation>
```

Before sharing an archive, check `Reference/VARIATION.md` and `Reference/PROVENANCE.md`, confirm source attribution and licensing for adapted material, remove private material, and verify that the branch contains no credentials, company-specific notes, or personal history. Git archives include committed files only, so review `git status` and the archive contents before distributing it.

## Provenance

The initial seed was a source snapshot provided by Mark Bakke. This file records adaptation choices; it is not a claim that the resulting vault is an unmodified copy.
