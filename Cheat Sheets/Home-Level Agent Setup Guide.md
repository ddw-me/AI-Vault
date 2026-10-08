# Home-Level Agent Setup Guide

This guide explains how to create and install a host-specific AI instruction file using the [Home-Level Agent Instruction Template](../Reference/Home%20Agent%20Template.md).

The template is a fill-in framework. The completed home-level file is an agent instruction set describing the computer's role, local tools, paths, repositories, and safety boundaries. It should not become a second copy of the portable vault instructions.

## Keep the home-level instruction file small

The completed home-level instruction file may be loaded broadly, so keep it limited to rules that are useful across many tasks on that computer. Every irrelevant rule consumes context space and can distract the AI from the current prompt or compete with task-specific instructions. Prefer a short routing instruction over a long procedure.

Use conditional references:

- If you need to update a daily note, read [the Daily Rolling Guide](Daily%20Rolling%20Guide.md).
- If you need to perform AI daily operations, read [the AI Daily Workflow](../000%20Workflows/000%20Daily%20Workflow.md).
- If you need to recover Git changes, read [the Recovery Guide](Recovery%20Guide.md).
- If you need a tool-specific procedure, read the relevant tool guide.

The instruction file should say where to find detailed guidance, not reproduce every command or workflow. This reduces duplicated instructions, keeps unrelated rules out of the active context, and makes stale guidance easier to find and remove.

Before adding a rule, ask:

- Does this apply to most tasks on this computer?
- Is it important enough to load even when the current prompt is unrelated?
- Could it be moved to a task-specific guide and referenced only when needed?

If the answer to the last question is yes, move the detail out of the home-level instruction file.

## Create the completed guide

1. Copy [Home Agent Instruction Template](../Reference/Home%20Agent%20Template.md) to a private location for the computer.
2. Fill in the host profile, task routing, workspace map, tools, permissions, and data boundaries.
3. Remove sections that do not apply and replace every remaining placeholder.
4. Add conditional references for detailed workflows instead of expanding the home-level instruction file.
5. Review the result for credentials, tokens, private keys, confidential work information, private contact information, and unnecessary absolute paths.
6. Record an owner and review date.

## Ask an AI tool to help complete the template

An AI tool can help gather the relevant host facts, identify missing sections, and propose a concise completed instruction set. Use plan mode or another read-only planning mode first. The AI should read this setup guide and the template before asking questions or proposing content.

You can use a prompt like this:

```text
Switch to plan mode or read-only planning mode. Read the Home-Level Agent Setup Guide and the Home-Level Agent Instruction Template before proceeding.

Help me complete the template for this computer. First, explain the sections that need information and inspect only safe, relevant host facts. Do not read, print, or search credentials, tokens, private keys, confidential work files, or sensitive personal information.

Keep the completed instruction file small. Put detailed procedures in separate referenced files using conditional guidance such as, "If you need to do X, read Y." Do not duplicate the portable vault instructions. Distinguish confirmed facts, suggested defaults, and questions for me.

Propose a filled-out version of the template for my review. Do not make changes during this planning pass. After I approve the plan, you may write the completed private instruction file, install the supported integration, configure the AI tool, create a symlink if appropriate, and verify the result. Inspect existing files and settings first, preserve unrelated configuration, and do not overwrite an existing instruction file without explaining the impact.
```

The AI can help with the complete setup. After the planning pass is approved, it should write the completed private instruction file, check that it contains no sensitive information, install it using the tool's supported mechanism, configure any required settings, and verify that the AI tool can discover and apply it. Installation and configuration are appropriate follow-on actions when they are included in the user's request; they should not be treated as prohibited merely because they change local AI-tool configuration.

## Do not assume every AI tool reads the same file

Instruction-file support and precedence differ between tools. Check the current documentation for the installed version and verify the result with a harmless read-only test.

### Codex

Codex discovers instruction files from supported user-level locations and from the repository path to the current working directory. It merges applicable files by scope, with more-specific instructions later in the path able to refine broader instructions. Use the [Codex prompting guide](https://developers.openai.com/cookbook/examples/gpt-5/codex_prompting_guide) for the current discovery behavior.

Do not assume that a file at `~/AGENTS.md` is automatically used in every repository context. Confirm which user-level location and project-level files the installed Codex environment supports.

### Cursor

Cursor has global User Rules and version-controlled project rules under `.cursor/rules`. Cursor's CLI also reads project-root `AGENTS.md` and `CLAUDE.md` when present. The older root `.cursorrules` file remains supported but is deprecated. See the [Cursor rules documentation](https://docs.cursor.com/context/rules).

Use Cursor User Rules for genuinely global preferences, `.cursor/rules` for project-specific rules, and a project-root `AGENTS.md` for portable repository guidance. Do not assume that a `~/AGENTS.md` symlink is Cursor's global instruction mechanism.

### Claude Code

Claude Code uses `~/.claude/CLAUDE.md` for user-wide instructions and `CLAUDE.md` for project instructions. It can also import another file from those instructions. See the [Claude Code memory documentation](https://docs.anthropic.com/en/docs/claude-code/memory).

If the completed home-level instruction file is maintained separately, use Claude Code's documented import mechanism rather than assuming that Claude Code will discover `~/AGENTS.md`.

## Unix-like symlinks

Some tools or local workflows may support a home-level symlink such as:

```text
ln -s /path/to/completed-home-agent-guide.md ~/AGENTS.md
```

Treat this as a tool-specific integration choice, not a universal standard. A symlink does not make a tool read the file if that tool does not search that location.

## Verify the setup

After installing the completed guide, use a harmless read-only prompt in the target tool:

```text
Identify the user-level, project-level, and vault-level instruction files you can see for this working directory. Summarize their scope and precedence. Do not edit files or run commands.
```

Check that the tool identifies the intended files, does not report secrets from the guide, and does not treat examples or reference notes as executable tasks. If the tool does not discover the file, use its documented user-level or project-level instruction mechanism instead.

## Maintain the guide

Review the completed guide when the computer changes, a tool changes its instruction mechanism, a repository moves, or an instruction is repeatedly misunderstood. Remove stale rules rather than accumulating exceptions. Keep detailed procedures in referenced documents and keep this guide focused on routing, boundaries, and host-specific facts.
