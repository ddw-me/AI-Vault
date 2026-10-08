# AI Assistant Prompts

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
Close out today's daily note using the AI Daily Workflow. Review completed work and every open item, then propose or record the correct disposition for each item and leave a useful starting point for tomorrow.
```
**Result**: Records outcomes, identifies unresolved work, and prepares deliberate carry-forwards

### Planning and Prioritization
```
Help me plan my day. Review my priorities and suggest optimal sequencing based on my energy patterns and calendar.
```
**Result**: Analyzes tasks and suggests optimal ordering based on difficulty and energy levels

### Task Analysis
```
Analyze my incomplete tasks and help me understand what's causing the persistence. What should I prioritize?
```
**Result**: Reviews carry-forward patterns and suggests priority adjustments

## Meeting and Communication

### Meeting Summarization
```
Could you summarize our [meeting type] from today's notes in a manner suitable for sharing with the wider [audience] team?
```
**Result**: Professional summary with executive overview, key points, and action items

### Email/Message Drafting
```
Based on today's meeting notes about [topic], help me draft a [type of communication] for [audience] focusing on [key points].
```
**Result**: Professional communication draft with key information

### Stakeholder Updates
```
Create a brief stakeholder update for [project/initiative] based on this week's progress notes.
```
**Result**: Concise status update highlighting progress, challenges, and next steps

## Analysis and Review

### Weekly Review
```
Please analyze this week's daily notes and create a weekly summary focusing on:
- Key accomplishments and strategic progress
- Patterns in productivity and energy
- Persistent tasks that need escalation
- Opportunities for process improvement
```
**Result**: Comprehensive weekly analysis with insights and recommendations

### Pattern Analysis
```
Analyze my [time period] notes for patterns in [specific area: productivity, energy, decision-making, etc.].
```
**Result**: Data-driven insights about trends and optimization opportunities

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
```
**Result**: Strategic planning support with data-driven recommendations

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
Based on my recent performance patterns and strategic objectives, help me set realistic [weekly/monthly/quarterly] goals.
```
**Result**: SMART goals aligned with capacity and strategic direction

## Agent-Specific Prompts

### Historian Agent
```
Historian: What patterns do you see in my task completion over the last [time period]? What factors correlate with my highest productivity?
```

```
Historian: Generate a summary of my key achievements this [week/month] for my performance review.
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
Scheduler: Based on my energy patterns, what's the optimal schedule for tomorrow's tasks?
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
CFO: What activities this month had the highest ROI in terms of business impact? What should I do more/less of?
```

```
CFO: Based on my time allocation, what strategic adjustments would maximize value creation?
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
Analyze my energy patterns and task completion rates. How can I better align challenging work with my peak energy periods?
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
Mark [task/project] as complete and process any follow-up actions.
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
