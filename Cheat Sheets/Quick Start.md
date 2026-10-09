# Quick Start

This is the main workflow onboarding guide for the vault. Start small: daily notes are enough for the first week. Add projects, reviews, and AI assistance as they become useful.

## 1. Install and open the vault

1. Install [Obsidian](https://obsidian.md/) on the computer or device you will use most often.
2. If you received an archive, extract it first. In Obsidian, choose **Open folder as vault** and select the folder containing `README.md`. Do not open one of its subdirectories as the vault.

## 2. Verify Daily Notes

The vault ships with Daily Notes and Templates settings. Verify these settings in Obsidian, and change them only if you want a different layout.

In Obsidian, open Settings and review Daily notes:

- **New file location:** `Daily Notes`
- **Template file location:** `Templates/Daily Notes Template.md`
- **Date format:** `YYYY-MM-DD`, unless you have a reason to change it

In Settings → Files and Links, set the default attachment location to a subfolder named `Attachments` under the current folder. This keeps pasted images and files beside the note that uses them.

For this vault's portability-oriented link behavior, also set:

- **Use Wikilinks:** off
- **New link format:** Relative path to file

See [Obsidian Commands and Settings](./Obsidian%20Commands%20and%20Settings.md) for portable command names and setup locations. To run a command, open Obsidian's command palette, search for the command name, and select it. Shortcuts vary by operating system and personal configuration.

## 3. Create the first note

In the command palette, choose **Daily notes → Open today's daily note**. If the settings are correct, Obsidian creates today's note using the configured template. Then:

1. Review the previous daily note, if one exists.
2. Choose one Daily Frog and a small number of realistic priorities.
3. Capture requests, decisions, ideas, and observations in today's note.
4. At the end of the day, decide what is complete, what carries forward, and what no longer matters.

You do not have to create a daily note every day. Sometimes you will be busy, sick, traveling, or handling something more important. A gap is not a failure and does not require reconstructing every missed day. When you return, start with today's note and review the most recent useful earlier note. Backfill a missed day only if it would help, using remembered or verified information. Do not let catching up keep you from returning to the notes.

For a project or review note, first create and open a blank destination note. Place the cursor in that note, then use **Templates → Insert template** and choose the appropriate template. This is separate from creating a daily note. The [Project Workflow](../000%20Workflows/Project%20Workflow.md) explains when to create a project and how to close or archive it.

Read the human-facing [Daily Rolling Guide](./Daily%20Rolling%20Guide.md) for the morning, daytime, and end-of-day cycle. AI tools should follow the [AI Daily Workflow](../000%20Workflows/000%20Daily%20Workflow.md) when rolling or updating notes.

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

For the reasoning behind the cycle and the Daily Frog, read [Time Management and Using This Vault](./Time%20Management%20and%20Using%20This%20Vault.md). For a fictional example of the system in practice, read [Time Management in Practice](./Time%20Management%20in%20Practice.md). For optional AI perspectives, see [Agent Overview](../100%20Agents/Agent%20Overview.md).

## 5. Add structure gradually

During the first week, focus on capturing and reviewing. After that, add only the structure that solves a real problem:

- create an active project when work spans multiple days or has several steps;
- use the [Project Workflow](../000%20Workflows/Project%20Workflow.md) to keep its status and completion condition clear;
- use the [Weekly Review](../000%20Workflows/Weekly%20Review.md) to see what is drifting and plan the next week;
- use the [Monthly Review](../000%20Workflows/Monthly%20Review.md) to look at longer arcs and adjust the system;
- create a goal note from the [Goal Template](../Templates/Goal%20Template.md) when you need to track a longer-term objective;
- use Git for checkpoints when the notes are valuable enough to preserve.

The optional plugins included with this vault are described in [Obsidian Setup](../Reference/Obsidian%20Setup.md). They are disabled by default; enable only what you want.

## Optional extensions

### A. Synchronization and mobile capture

The vault may live in Dropbox or another synchronized folder for access from multiple computers. Set it up and test it on one computer first. Mobile syncing has platform-specific limitations; consult Obsidian's [sync guide](https://obsidian.md/help/sync-notes) or use Obsidian Sync before relying on Dropbox for mobile access.

A phone or tablet can make the vault useful for capturing a quick idea, reminder, or task while you are away from your computer. Keep mobile capture simple: add a short item to today's daily note or another temporary capture note, then do more structured organization later on a computer.

Some people use a separate quick-capture app such as Google Keep when opening the vault is inconvenient. That can work as a temporary inbox, but it creates another place to check. Transfer useful captures into the vault when you return to your computer; keep the vault as the durable record.

Synchronization and Git provide different things: synchronization provides access, while Git provides history and recovery. Read the [Recovery Guide](./Recovery%20Guide.md) before relying on either system as a backup. If you do not use Git, make periodic copies or archives of the entire vault and test that a copy can be opened before relying on it as a backup.

### B. Git and recovery

Git is optional for getting started, but it becomes increasingly valuable as the vault accumulates useful notes. Commit related files whenever you reach a meaningful checkpoint. Some people commit several times during the day. When starting out, committing the useful work from a whole day is also fine.

The important habit is to commit regularly enough that you have a recent point to return to if you make a mistake. Commit before making a major reorganization, bulk edit, or workflow change. Review the changed files and staged diff before committing.

A local commit provides history and recovery. Push or copy the repository elsewhere if you also want protection from computer loss or disk failure. A private GitHub repository is one option for personal notes, provided you are comfortable storing them there and configure access carefully. See the [Recovery Guide](./Recovery%20Guide.md) for practical commands.

### C. AI assistance

> Before opening this vault in an AI-enabled editor or connecting an AI assistant, read [AGENTS.md](../AGENTS.md). It defines what the AI may read, suggest, change, and do automatically.

AI is optional, but recommended. It can help analyze notes, suggest smaller next actions, or prepare a review, but it should not silently invent tasks or decide what you value. Useful starting prompts include:

- “Review the most recent previous daily note and suggest possible carry-forwards. Do not create today's note yet.”
- “Help me choose a Daily Frog from today's open items.”
- “Summarize this week's notes and identify work that needs a deliberate next step.”

For more bounded examples, see [AI Prompts](./AI%20Prompts.md).

For a first AI interaction, if the assistant has file access, ask it to read `AGENTS.md` and the relevant workflow before working and to identify which notes it can access. If it does not have file access, provide the relevant instructions and selected notes yourself. Ask for a draft or recommendation first; a response in chat does not mean that a note was saved.

### D. Personal context and host setup

If you want AI assistance to reflect your background and working preferences, fill in [About Me](../Reference/About%20Me.md). This is optional: leave the template blank if you do not want to provide personal context. Do not put passwords, credentials, private keys, or other secrets in it.

If this computer needs host-specific AI instructions, use the optional [Home-Level Agent Setup Guide](./Home-Level%20Agent%20Setup%20Guide.md) and its [instruction template](../Reference/Home%20Agent%20Template.md).

For a fuller daily note with calls, code, design, sharing, reflection, and context preparation sections, use the [Daily Notes Extended Template](../Templates/Daily%20Notes%20Extended%20Template.md). Start with the standard template unless the additional structure is useful.

## If the system feels heavy

Return to the smallest useful pattern: one daily note, one Daily Frog, a few priorities, and a short end-of-day cleanup. The system is working when it helps you remember and focus, not when every section is filled in.
