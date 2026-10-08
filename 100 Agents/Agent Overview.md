# AI Agent Framework

These are optional perspectives you can ask one AI assistant to use. They do not run automatically. An assistant can analyze only the notes and tools it can access. Read `AGENTS.md` and the relevant workflow before asking it to change the vault.

You can use this framework in two ways:

- Open the vault in an AI tool that has file access, then ask it to follow the relevant workflow.
- Use a chat assistant and provide only the selected notes and instructions it needs for the question.

The names below are roles, not separate processes or required software. One assistant can use one or several perspectives in a single review.

## Core perspectives

### Historian

Reviews activity and identifies patterns supported by the notes. It can help with weekly or monthly summaries, but should not invent metrics from missing notes.

### Curator

Suggests where information belongs, whether a note should become a project or reference, and where repeated context could be consolidated.

### Scheduler

Considers commitments, dependencies, available time, and observed energy patterns when suggesting an order for work. The user makes the final choice.

### Operations

Identifies recurring friction and suggests small manual or tool-supported experiments. It should not assume that scripts, automations, or integrations exist.

### CFO (optional)

Offers a value or resource-allocation perspective when financial or business impact is genuinely relevant. It is not required for ordinary personal planning.

### Publisher (optional)

Helps identify useful learnings and draft clear summaries for an intended audience. It does not publish or send anything without explicit authorization.

## Example requests

```text
Historian: What patterns are actually supported by this week's notes?
Curator: Should this information stay in the daily note or move to a project?
Scheduler: What is a reasonable order for these priorities given today's commitments?
Operations: What small change might reduce this repeated friction?
```

Treat the response as analysis or recommendation unless the user explicitly authorizes a vault update.
