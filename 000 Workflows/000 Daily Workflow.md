# Daily Workflow — AI Instructions

This file is the execution contract for an AI assistant working in this vault.
It describes what the assistant should do when the user asks it to roll the
daily notes, plan the day, capture work, or close out the day.

The human-facing explanation is in [Daily Rolling Guide](../Cheat%20Sheets/Daily%20Rolling%20Guide.md).
Do not treat the explanatory guide, examples, or templates as work items.

## Scope and authority

Follow these rules when the user asks for a morning roll, daily plan, daily
note update, carry-forward review, or end-of-day cleanup.

- Work from the vault root and use the existing folders and templates.
- Treat the current user request as the highest-priority source of intent.
- Preserve existing notes. Do not silently delete, rewrite, or relocate user
  content.
- Do not invent tasks, dates, commitments, meetings, priorities, or outcomes.
- The AI may analyze context and propose a plan. When the user explicitly asks
  for a roll or update, it may create or update the appropriate daily note.
- Keep recommendations visible as recommendations until the user accepts or
  changes them. Do not present an AI suggestion as a user decision.

## Date and time

Before creating or rolling a dated note:

1. Determine the current date and weekday from the host environment or an
   available time/date tool.
2. Do not calculate the date from memory or assume that the system date in a
   previous note is current.
3. Use the user's local timezone when it is known. If the timezone is unknown
   and the date affects the result, state the assumption.

If a date or weekday cannot be established reliably, do not create a note with
an uncertain date. Report the problem and ask the user.

## Context discovery

Use the following context, in this order:

1. The current user request and explicit commitments.
2. [About Me](../Reference/About%20Me.md), if it exists and contains useful
   context.
3. Today's daily note, if it already exists.
4. Calendar commitments and fixed deadlines, when available.
5. Yesterday's daily note and its open items.
6. Notes in `Active Projects/` and `Goals/`.
7. The most recent weekly review, if available.
8. The current monthly review or plan, if available.

Higher-level planning informs recommendations but does not override an urgent
commitment or an explicit user decision.

### Fail-open context rule

Missing context must reduce the information available to the AI, not stop the
workflow.

- If there is no monthly plan, continue with weekly reviews, projects, goals,
  daily notes, and the current request.
- If `Reference/About Me.md` is missing or still a blank template, continue
  without personal context. Do not infer personal preferences or ask the user
  to fill it in as a condition of running the workflow.
- If there is no weekly review, continue with projects, goals, and daily notes.
- If there are no projects or goals, continue with the current request and
  daily notes.
- If yesterday's note is missing, start a new note without reconstructing work
  that is not available.
- Do not invent missing priorities. Mention missing context only when it
  materially affects the recommendation.

## Morning roll

When the user asks to roll the daily notes or prepare the day, follow these
steps.

### 1. Read the source notes

Read yesterday's note completely before deciding what to carry forward. Also
read today's note if it already exists. Look for:

- unchecked tasks and incomplete priorities;
- `Tomorrow` and `Carry-Forward` sections;
- `Quick Wins`;
- `Waiting / Delegated` items and promised follow-ups;
- calls, commitments, and action items;
- project work that needs another step;
- user instructions beginning with `(AI Assistant:)` in the daily note.

Do not rely only on unchecked checkboxes. Important work may be recorded as
plain text, a follow-up, a decision, or an instruction.

### 2. Classify every open item

For each item that may continue into today, assign one disposition:

- **Complete:** already finished or no longer open.
- **Carry forward:** still relevant and has a clear next action.
- **Move to project:** needs multiple steps or will span several days.
- **Delegate / Waiting:** another person or external event owns the next step.
- **Schedule:** belongs on a later date or depends on a fixed commitment.
- **Drop:** no longer needed, duplicated, or deliberately abandoned.
- **Needs decision:** the available context is insufficient; surface it to the
  user rather than guessing.

Do not silently drop an item. If an item is not carried forward, report its
disposition in the result or record the decision in the daily note.

### 3. Create or update today's note

If today's note does not exist, create it from
[Daily Notes Template](../Templates/Daily%20Notes%20Template.md). If it exists,
preserve its content and update only the relevant planning or carry-forward
sections.

Carry forward enough context to make each item actionable. Do not copy an
entire old note into today's note, and do not copy an item merely because it
was unchecked.

Keep these categories distinct:

- the user's priorities and commitments;
- AI suggestions;
- waiting or delegated work;
- notes and observations captured during the day.

### 4. Prepare the daily plan

Use available commitments, time, project context, and open items to prepare:

- one proposed Daily Frog;
- a small set of proposed priorities;
- a realistic sequence or time allocation;
- any blocker, dependency, or conflict that should be visible.

The AI may choose a strong candidate and explain why, or offer several
candidates for review. The user may accept, change, or reject the proposal.
Do not fill the day beyond its available capacity.

The Daily Frog should usually be a concrete next action that removes friction,
unblocks work, or handles an important avoided task. It does not need to be
the largest or most difficult project task, and persistence is context rather
than a score or a reason to shame the user.

### 5. Verify the result

Before reporting completion, check that:

- today's note has the correct date and template structure;
- every relevant open item has a visible disposition;
- Quick Wins and Waiting / Delegated items were not silently lost;
- user instructions were not mistaken for ordinary tasks;
- proposed priorities fit known commitments and available time;
- no invented facts, dates, meetings, or outcomes were added.

Report the note created or updated, the proposed Daily Frog and priorities,
items carried forward, items needing a decision, and any missing context that
limited the analysis.

## During-day support

When the user asks to capture or process something during the day:

- add requests, decisions, observations, and outcomes to today's note;
- use **Delegate, Record, or Do** for new work;
- record the owner and follow-up when work is delegated or waiting;
- move multi-step work to `Active Projects/` when appropriate, preserving a
  pointer in the daily note;
- keep AI suggestions visibly separate from confirmed user decisions;
- do not turn a casual observation into a task without the user's intent.

Treat `(AI Assistant: ...)` entries as instructions to process during the next
relevant AI interaction. Preserve them until they are handled or the user
explicitly removes them.

## End-of-day review

When the user asks to close out the day or prepare tomorrow:

1. Review today's note and identify completed work, partial progress, and open
   items.
2. Record meaningful outcomes rather than only marking checkboxes.
3. Give every open item a disposition: carry forward with a next action, move
   to a project, delegate, wait, schedule, drop, or ask for a decision.
4. Prepare a short starting point for tomorrow.
5. Do not claim that an item is complete merely because it was discussed.

## Boundaries

This workflow does not require bookmarks, HTML files, custom scripts, a named
automation framework, a monthly plan, or a specific AI product. If a local
installation provides additional tools, use them only when the user requests
that capability and the vault documents it.

For weekly and monthly synthesis, use the [Weekly Review](./Weekly%20Review.md)
and [Monthly Review](./Monthly%20Review.md) workflows rather than expanding
the daily roll into a long-term planning process.
