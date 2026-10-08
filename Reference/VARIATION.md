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

## Variation policy

Create a variation branch from `main` when a use case needs additional folders or guidance. Keep generic fixes on `main`, then merge them into the variation deliberately. Record the variation's purpose and branch-specific changes in this file.

## Provenance

The initial seed was a source snapshot provided by Mark Bakke. This file records
adaptation choices; it is not a claim that the resulting vault is an unmodified
copy.
