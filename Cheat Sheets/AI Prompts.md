# AI Assistant Prompts

These prompts are starting points, not a replacement for the workflow instructions. The [Daily Workflow — AI Instructions](../000%20Workflows/000%20Daily%20Workflow.md) and the user's current request determine what the AI may change.

Unless a prompt explicitly asks for a vault update, treat the result as analysis or a draft for review. Use only facts available in the vault or supplied by the user. Label assumptions, proposals, and missing context instead of filling them in. Do not send messages, publish content, commit changes, or perform external actions unless the user explicitly asks.

## Daily Workflow Prompts

The complete execution rules are in [Daily Workflow — AI Instructions](../000%20Workflows/000%20Daily%20Workflow.md). The human-facing explanation is in the [Daily Rolling Guide](./Daily%20Rolling%20Guide.md).

### Morning Roll
```
Good morning. Roll today's daily note using the AI Daily Workflow. Review the most recent previous note, available projects and planning context, carry forward relevant work, and propose a Daily Frog and priorities for my review.
```
**Result**: Reviews available context, updates or creates today's note when requested, proposes a Daily Frog and priorities, and reports unresolved items or missing context

### Morning Review Without Changing Notes
```
Review the most recent previous daily note and available planning context. Suggest possible carry-forwards, a Daily Frog, and today's priorities, but do not create or change today's note yet.
```
**Result**: Produces a proposed plan for review without changing the vault

### End-of-Day Cleanup
```
Close out today's daily note using the AI Daily Workflow. Review completed work and every open item, propose a disposition for each item, and leave a useful starting point for tomorrow. Show me the proposed changes first unless I explicitly ask you to update the note.
```
**Result**: Proposes outcome records, identifies unresolved work, and prepares deliberate carry-forwards. The note is changed only when the user authorizes the update.

### Targeted Daily Note Update
```
Update the named daily note [date or note path] using the AI Daily Workflow. Read that target note first and change only [requested section or change]. Preserve its existing plan and unrelated content. Do not roll another date or perform a full daily cleanup. Recommend related project or summary changes, but do not make them unless I authorize them.
```
**Result**: Makes a bounded update to the requested note or reports why the target cannot be resolved

### Planning and Prioritization
```
Help me plan my day. Review my known commitments, priorities, available time, and any relevant context. Suggest a realistic sequence and explain the tradeoffs; do not decide my priorities for me or change my notes.
```
**Result**: Analyzes tasks and suggests a realistic ordering based on the available context, difficulty, and energy levels

### Task Analysis
```
Analyze my incomplete tasks and help me understand what's causing the persistence. What should I prioritize?
```
**Result**: Reviews carry-forward patterns and suggests priority adjustments

## Meeting and Communication

### Meeting Summarization
```
Could you draft a summary of our [meeting type] from today's notes in a manner suitable for sharing with the wider [audience] team? Use only the available notes, identify unresolved items, and do not send or publish it.
```
**Result**: Professional summary with executive overview, key points, and action items

### Email/Message Drafting
```
Based on today's meeting notes about [topic], help me draft a [type of communication] for [audience] focusing on [key points]. Use only supported facts, mark anything needing confirmation, and do not send it.
```
**Result**: Professional communication draft with key information

### Stakeholder Updates
```
Draft a brief stakeholder update for [project/initiative] based on this week's progress notes. Separate completed work, current status, risks, and next steps. Use only supported facts and do not send or publish it.
```
**Result**: Concise status update highlighting progress, challenges, and next steps

## Analysis and Review

### Weekly Review
```
Follow the [Weekly Review Workflow]. Review the requested Monday-through-Sunday period, or the most recently completed week if I do not specify a range. State which daily notes, active projects, goals, waiting items, and existing summaries you reviewed. Distinguish missing sources from sources unavailable to you. Summarize accomplishments, open commitments, recurring friction, decisions, and learning without inventing facts or metrics. Recommend a small set of possible next-week priorities, clearly labeled as recommendations. Search for and reuse an existing summary for the period before proposing a new one. Do not create or overwrite a summary until I approve it.
```
**Result**: An evidence-limited weekly draft with source coverage, missing context, open commitments, and clearly labeled recommendations

### Pattern Analysis
```
Analyze my [time period] notes for patterns in [specific area: productivity, energy, decision-making, etc.]. Distinguish observed evidence from interpretation, and do not invent metrics from missing notes.
```
**Result**: Evidence-based observations about trends and possible areas for improvement, with uncertainty called out

### Friction Point Analysis
```
Operations agent: Review my recent notes and identify the biggest friction points in my workflow. What can we systematically eliminate?
```
**Result**: Specific recommendations for process improvements and automation opportunities

## Planning and Strategy

### Monthly Planning
```
Based on the past month's daily notes and summaries, help me:
- Identify emerging themes and priorities
- Create next month's strategic focus areas
- Optimize my workflow based on observed patterns
- Set realistic goals aligned with larger objectives

Use only supported facts and distinguish observations from interpretations and recommendations. Do not invent missing objectives, metrics, deadlines, or outcomes. Do not create or update notes until I approve the proposed plan.
```
**Result**: Evidence-limited planning support with clearly labeled recommendations

### Project Creation and Planning

**New Project Setup:**
```
Create a draft project note named "[Project Name]" in "Active Projects/" using
"Templates/Project Template.md". Use only the details I provide and information
already in the vault. Leave unknown fields blank. Label proposed milestones,
dates, estimates, and assumptions as proposed; do not invent stakeholders,
deadlines, outcomes, or completed work. Show me the draft before making further
changes.
```
**Result**: A clearly labeled project draft that can be completed by the user.

**Project Planning:**
```
Help me break down [project name] into actionable steps. Separate known commitments from proposed sequencing, estimates, and dates. Do not invent deadlines or dependencies.
```
**Result**: A project plan with clearly labeled known facts, open questions, and proposals

### Goal Setting
```
Based on the information I provide and any supported context in the vault, help me draft realistic [weekly/monthly/quarterly] goals. Separate known objectives from proposed goals, dates, measures, and assumptions. Do not invent missing priorities or update notes unless I authorize it.
```
**Result**: Clearly labeled goal proposals aligned with supported context

## Agent-Specific Prompts

### Historian Agent
```
Historian: What patterns are actually supported by my notes over the last [time period]? Distinguish observations from interpretations and hypotheses. Do not calculate completion rates, correlations, or other metrics unless the source supports them.
```

```
Historian: Generate a summary of my key achievements this [week/month] for my performance review. Use only supported evidence, identify missing context, and do not invent metrics or outcomes.
```

### Curator Agent
```
Curator: Review my recent notes and suggest how to better organize this information for long-term reference.
```

```
Curator: What information am I capturing repeatedly that should be systematized or templated?
```

### Scheduler Agent
```
Scheduler: Based on my stated commitments, constraints, and any observed energy patterns, suggest a realistic schedule for tomorrow's tasks. Label assumptions and recommendations; do not change my notes.
```

```
Scheduler: Analyze my calendar and task list for next week. What scheduling conflicts or optimization opportunities do you see?
```

### Operations Agent
```
Operations: What are the biggest bottlenecks in my current workflow, and what specific steps can eliminate them?
```

```
Operations: How can I simplify or streamline the processes I do most frequently? Suggest manual or tool-supported changes, and do not assume scripts exist.
```

### CFO Agent (Business Focus)
```
CFO: Based on documented effort and outcomes this month, what activities appear to have had the most useful impact? Distinguish evidence from assumptions, do not invent ROI or financial metrics, and suggest what I might do more or less of.
```

```
CFO: Based on documented time allocation, commitments, and outcomes, what strategic adjustments could I consider? Label recommendations and missing information; do not claim to have measured value that the notes do not support.
```

### Publisher Agent (Content/Communication)
```
Publisher: What insights from my recent work would be valuable to share with [specific audience]?
```

```
Publisher: Help me identify the most important learnings from [project/period] and how to communicate them effectively.
```

## Specialized Analysis

### Process Improvement
```
Compare my workflow from [earlier period] to now. What improvements have worked, and what new optimizations should I try?
```

### Energy Optimization
```
Analyze the energy observations and task context in my notes. How might I better align challenging work with periods that appear more suitable? Distinguish evidence from interpretation and do not infer task completion rates or causal relationships that the notes do not support.
```

### Decision Quality Review
```
Review the major decisions I've made this [week/month]. What decision-making patterns are serving me well, and what should I adjust?
```

### Learning and Development
```
Based on my recent activities and challenges, what skills or knowledge areas should I prioritize for development?
```

## Quick Reference Commands

### Task Status Updates
```
Review [task/project] and propose whether it is complete, should carry forward, move to a project, be delegated, scheduled, dropped, or needs a decision. Do not update the note unless I explicitly authorize that change.
```

### Context Switching
```
I'm switching from [current task] to [new task]. Help me capture my current state and set up context for the new task.
```

---

## Tips for Effective AI Interaction

1. **Be Specific**: Include relevant context and timeframes
2. **Use Agent Names**: Direct requests to specific agent roles when appropriate
3. **Ask for Analysis**: Don't just ask for summaries, ask for insights and patterns
4. **Request Recommendations**: Ask for specific next steps and process improvements
5. **Combine Multiple Perspectives**: Ask multiple agents to contribute to complex decisions
6. **Follow Up**: Ask clarifying questions and dive deeper into interesting insights
