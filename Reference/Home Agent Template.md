# Home-Level Agent Instruction Template

Use this as a starting point for the host-specific agent instructions that accompany a portable vault. It is intentionally separate from the vault's root [AGENTS.md](../AGENTS.md).

The vault instructions describe how the vault works. A completed copy of this file describes one computer's role, tools, paths, repositories, and local safety boundaries. Create a separate completed version for each computer when those details differ.

The relative links in this template assume that the completed file remains in the vault's `Reference/` folder. If you install it somewhere else, rewrite the retained vault references for that location or use the AI tool's supported import mechanism.

## How to use this template

- Copy this file to a private location for the target computer.
- Fill in only the sections that apply to that computer and user.
- Remove unused headings, examples, and placeholders after filling it in.
- Do not duplicate the portable vault rules unless repeating a rule is important for safety.
- Keep this file small. It may be loaded for many different prompts, so irrelevant rules waste context space and can compete with task-specific guidance. Put detailed procedures in separate files and link to them conditionally: "If you need to do X, read Y."
- Review the completed file periodically and remove rules that are no longer current.

## Scope and precedence

- This file applies to AI work performed in this computer's user environment.
- Follow each tool's documented instruction discovery and precedence rules. Do not assume that every tool reads this file or gives it the same priority.
- Do not use this file to override system, user, vault, or repository-specific instructions.
- Repository-specific instructions apply when working in that repository. The portable vault instructions apply when working in the vault.

## Host profile

- Host name:
- Operating system:
- Primary AI tools:
- Default shell or terminal:
- Main vault path:
- Important workspace paths:
- Sync or backup locations:

## Task routing

| Task | Start with | Notes |
|---|---|---|
| Daily notes | | |
| Project work | | |
| Repository work | | |
| External systems | | |
| Research or reference work | | |

Use short routing pointers here. If a task needs a long procedure, put that procedure in a separate document and link to it.

## Workspace and repository map

| Location | Purpose | Read/write boundary | Additional guidance |
|---|---|---|---|
| | | | |

List only locations that help an AI choose the correct workspace or avoid crossing a data boundary.

## Tools and tool routing

- Approved tools:
- Tools that must be used for particular tasks:
- Tools that are read-only:
- Actions that require explicit approval:
- What to do when a required tool is unavailable:

If a tool has a detailed procedure, write: "If you need to use this tool, read [the tool guide](path/to/guide.md)." Do not put credentials, tokens, or secret locations in this file.

## File editing and Git

- Read a file before editing it:
- Preserve unrelated local changes:
- Preferred editing method:
- Required validation checks:
- Commit policy:
- Push policy:

## External systems and permissions

- Systems that may be queried without additional approval:
- Systems that are draft-only:
- Actions that require explicit user approval:
- Actions that must never be performed from this computer:

## Data and security boundaries

- Data allowed on this computer:
- Data that must not be copied to this computer:
- Sensitive information that must not be written into shared files:
- Approved secret or credential mechanism:

Never put credentials, tokens, private keys, confidential work instructions, or sensitive personal information in a home-level instruction file intended for sharing.

## Host-specific references

Add links to detailed local guides here. Keep the instruction file itself small and use conditional references such as:

- If you are working on daily notes, read [the daily-note guide](path/to/daily-guide.md).
- If you are working on Git recovery, read [the recovery guide](path/to/recovery-guide.md).
- If you are using a local tool, read [the tool guide](path/to/tool-guide.md).

## Maintenance

- Owner:
- Last reviewed:
- Review when:

Update this file when the computer's tools, paths, data boundaries, or workflows change.

## Installing for an AI tool

Instruction-file locations differ between tools. Use the companion [Home-Level Agent Setup Guide](../Cheat%20Sheets/Home-Level%20Agent%20Setup%20Guide.md) to choose the appropriate user-level or project-level integration.
