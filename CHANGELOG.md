# Changelog

This file records notable changes to the published starter-vault snapshots. It is a release history, not an automatic upgrade guide. Once a vault has been customized, review later changes and adopt them selectively.

## v0.9.2

- Consolidated the bundled third-party license text into `Reference/THIRD-PARTY-NOTICES.md`, including the required MIT, GPL-3.0, MPL-2.0, and Tag Wrangler notices.
- Pinned upstream license links to the commits corresponding to the bundled plugin and theme versions.
- Added release identity and snapshot-history guidance to `Reference/VARIATION.md`.
- Added this changelog so published snapshots have a concise release history.

## v0.9.1

- Clarified in the README that the vault is a customizable starter snapshot rather than a package with an automatic upgrade path.
- Updated `VERSION` to identify this release candidate.

## v0.9.0

- Published the first tagged release-candidate snapshot of the generic Durable Context starter vault.
- Included the portable daily, weekly, and monthly workflow guidance, templates, recovery guidance, optional AI workflow, provenance notes, and third-party notices assembled in the baseline.
- Added `VERSION` to identify the starter snapshot.

### Earlier Changes

Before the first tagged snapshot, the baseline was refined through several review / test cycles:

- Reworked the daily, weekly, and monthly workflows to separate human guidance from AI instructions, preserve user authorization, use resolved target notes, surface scheduled work, and tolerate missed days without pressure.
- Added practical guidance for time management, daily rolling, projects, AI assistance, synchronization, Git checkpoints, remote recovery, and Obsidian setup.
- Added project and goal templates, an extended daily template, personal-context and home-agent templates, and a visual README introduction.
- Added reference notes, licensing and provenance documentation, and a clearer onboarding path.
- Added friction-reduction guidance so the system favors small, useful improvements over unnecessary automation or process overhead.
- Established a generic branch and variation model so the public vault can remain a starter snapshot while personal editions diverge.

### Changes from Mark's Original Implementation

The public vault began with the August 2025 snapshot of Mark Bakke's AI-native Obsidian workflow. It retained the core idea of daily notes supported by weekly and monthly review, templates, lightweight agents, AI prompts, project organization, and Git checkpoints.

The public baseline adapted that material into a generic, directly usable vault:

- Removed personal and company context.
- Removed dated example content.
- Removed Cursor/Windsurf-specific assumptions.
- Removed setup scripts, HTML bookmark management, bookmark automation, and other workflow-specific tooling.
- Added portable `AGENTS.md` guidance and a repository README.
