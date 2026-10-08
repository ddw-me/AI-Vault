# Portable Vault Instructions

> `AGENTS.md` is the canonical instruction file for this vault. `cursor.md` is a small compatibility redirect for tools that look for that filename; it does not define a second set of rules.

This file describes the generic rules for working in this vault. It is intended to be portable across computers and AI tools.

## How to use this vault

- Start with [Quick Start](Cheat%20Sheets/Quick%20Start.md). It is the vault's only onboarding guide.
- Consult [Obsidian Setup](Reference/Obsidian%20Setup.md) before enabling or removing optional community plugins. They are disabled by default.
- For human daily use, read [Daily Rolling Guide](Cheat%20Sheets/Daily%20Rolling%20Guide.md).
- For AI daily operations, follow [Daily Workflow — AI Instructions](000%20Workflows/000%20Daily%20Workflow.md).
- Read [About Me](Reference/About%20Me.md) when it exists and contains useful context. If it is missing or still a blank template, continue without it.
- Read the relevant workflow or template before changing it.
- Keep daily capture in `Daily Notes/` unless a workflow says to move it elsewhere.
- Use `Active Projects/` for projects that need more than a single daily-note entry.
- Use `Templates/` for repeatable note shapes and `Cheat Sheets/` for short references.
- Use `000 Workflows/` for process instructions and `100 Agents/` for role descriptions.
- Preserve existing notes and history. Prefer small, targeted edits.
- Ask before deleting notes or changing a workflow's intent.

## AI collaboration

- Treat the vault as the user's record, not as an AI scratchpad.
- Use the existing structure and terminology before proposing new folders or systems.
- Separate suggestions from confirmed facts and completed work.
- Do not invent tasks, dates, meetings, accomplishments, or priorities.
- Review, analysis, planning, and suggestions are read-only unless the user asks to create, roll, or update a note. Recording a task does not authorize performing it. Commits, pushes, messages, publications, and other external actions require an explicit request.
- When a request is ambiguous, make the smallest reasonable change and explain the assumption.

## Note formatting

- Prefer concise, scannable Markdown.
- Use headings to separate distinct topics.
- Prefer bullets or short paragraphs over dense prose in daily notes.
- Do not hard-wrap ordinary prose or bullet text just to fit a source-file width.
- Keep code blocks and diagrams reasonably narrow so they do not require excessive horizontal scrolling.
- Use fenced code blocks only when formatting or literal syntax matters.

## Internal links

- Use relative Markdown links for vault-internal references so notes work in Obsidian, GitHub, and exported copies.
- URL-encode spaces in Markdown link targets.
- Link to a specific note rather than a bare directory.
- If a folder becomes a navigable topic with multiple notes, give it a README before linking to it.
- Validate that linked files and section anchors exist before creating links.
- Use external Markdown links for websites and other resources.
- Do not create links merely to make a note look connected; link when the destination helps the reader continue the work.

## Workflow fidelity

- When a documented workflow exists, follow it rather than inventing an alternative process.
- Keep execution instructions in workflow files and explanatory guidance in human-facing guides.
- Treat examples, background text, and templates as reference material, not as tasks to execute.
- When a workflow is missing or ambiguous, state the gap and use the smallest reasonable manual process.

## File boundaries

- Work within this vault unless the user explicitly requests an external file or repository change.
- Do not copy machine-specific paths, company context, credentials, tool configuration, or personal workflow assumptions into this vault.
- Keep reusable guidance generic enough to work with different AI tools and operating systems.

## Git and synchronization

- Use Git as a checkpoint and recovery mechanism.
- Daily notes, project notes, goals, and summaries are user content and are intended to be visible to Git. Review `git status` before committing.
- Commit meaningful changes with clear messages; do not require a commit for every note.
- Do not commit credentials, tokens, private keys, or confidential material.
- Cloud synchronization and Git solve different problems: synchronization provides device access, while Git provides history and recovery.

## Host and repository instructions

This file applies to this vault. A computer may have a separate home-level `AGENTS.md`, and a code repository may have its own repository-level instructions. More-specific instructions apply to their own scope; do not copy machine-specific or repository-specific rules into this portable vault.
