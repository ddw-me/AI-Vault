# Quick Start

This is the only onboarding guide for the vault. Start small: daily notes are
enough for the first week. Add projects, reviews, and AI assistance as they
become useful.

## 1. Install and open the vault

1. Install [Obsidian](https://obsidian.md/) on the computer or device you will
   use most often.
2. Open the repository's root directory as an Obsidian vault. Do not open one
   of its subdirectories as the vault.
3. Read [AGENTS.md](../AGENTS.md) for the portable rules.

The vault may live in Dropbox or another synchronized folder for access from
multiple devices. Git commits are best made from a computer where Git is
configured. Synchronization and Git provide different things: synchronization
provides access, while Git provides history and recovery.

## Optional: add personal context

If you want AI assistance to reflect your background and working preferences,
fill in [About Me](../Reference/About%20Me.md). This is optional: leave the
template blank if you do not want to provide personal context. Do not put
passwords, credentials, private keys, or other secrets in it.

## 2. Configure Daily Notes

In Obsidian, open Settings and configure Daily notes:

- **New file location:** `Daily Notes`
- **Template file location:** `Templates/Daily Notes Template.md`
- **Date format:** `YYYY-MM-DD`, unless you have a reason to change it

In Settings → Files and Links, set the default attachment location to a
subfolder under the current folder. This keeps pasted images and files beside
the note that uses them.

## 3. Create the first note

Create today's daily note using the configured template. Then:

1. Review the previous daily note, if one exists.
2. Choose one Daily Frog and a small number of realistic priorities.
3. Capture requests, decisions, ideas, and observations in today's note.
4. At the end of the day, decide what is complete, what carries forward, and
   what no longer matters.

Read the human-facing [Daily Rolling Guide](./Daily%20Rolling%20Guide.md) for
the morning, daytime, and end-of-day cycle. AI tools should follow the
[AI Daily Workflow](../000%20Workflows/000%20Daily%20Workflow.md) when rolling
or updating notes.

## 4. Learn the basic structure

| Folder | Use it for |
| --- | --- |
| `Daily Notes/` | Daily capture, planning, and reflection |
| `Active Projects/` | Work that needs more than one day's attention |
| `Goals/` | Longer-term objectives and aspirations |
| `Summaries/` | Weekly and monthly review outputs |
| `Templates/` | Repeatable note shapes |
| `Cheat Sheets/` | Short references and practical guidance |
| `000 Workflows/` | How the recurring processes work |
| `100 Agents/` | Optional AI role descriptions |

For the reasoning behind the cycle and the Daily Frog, read [Time Management
and Using This Vault](./Time%20Management%20and%20Using%20This%20Vault.md).

## 5. Add structure gradually

During the first week, focus on capturing and reviewing. After that, add only
the structure that solves a real problem:

- create an active project when work spans multiple days or has several steps;
- use the [Weekly Review](../000%20Workflows/Weekly%20Review.md) to see what is
  drifting and plan the next week;
- use the [Monthly Review](../000%20Workflows/Monthly%20Review.md) to look at
  longer arcs and adjust the system;
- use Git for checkpoints when the notes are valuable enough to preserve.

## Optional AI assistance

AI is optional. It can help analyze notes, suggest smaller next actions, or
prepare a review, but it should not silently invent tasks or decide what you
value. Useful starting prompts include:

- “Review yesterday's daily note and suggest possible carry-forwards. Do not
  create today's note yet.”
- “Help me choose a Daily Frog from today's open items.”
- “Summarize this week's notes and identify work that needs a deliberate next
  step.”

## If the system feels heavy

Return to the smallest useful pattern: one daily note, one Daily Frog, a few
priorities, and a short end-of-day cleanup. The system is working when it helps
you remember and focus, not when every section is filled in.
