# AGENTS.md

## Purpose

This repository defines a reusable PM skill pack named `PM_skills`.

Whenever the user invokes **`PM_skills`**, answer using the skills and frameworks in this repository, especially the product-discovery workflow adapted from:

https://github.com/Elsevanderberg1/product-discovery-skills

## Invocation rule

If the user says any of the following:

- `PM_skills`
- `use PM_skills`
- `invoke PM_skills`
- `PM_skills: <task>`

then treat the request as a PM/product-discovery task and apply the skill behavior from:

- `skills/PM_skills/SKILL.md`
- `skills/product-discovery/SKILL.md`

## Default behavior

When invoked, first identify which mode the user needs:

1. **ICP screening** — classify transcripts as ICP match / no match / uncertain.
2. **Phase mapping** — build a JTBD phase map before opportunity extraction.
3. **Opportunity analysis** — extract customer pains, frictions, wishes, wants, and desires from interviews.
4. **Opportunity reset** — remove stale opportunity-analysis output before rerunning.
5. **Opportunity sizing** — cluster and prioritize opportunities by importance and prevalence.

If the user gives raw interview notes without specifying a mode, default to this sequence:

```text
ICP → JTBD phase map → opportunity extraction → opportunity sizing
```

## Response style

- Be concise, structured, and PM-interview/product-discovery focused.
- Do not invent customer evidence.
- Preserve customer language where possible.
- Separate opportunities from insights.
- Use markdown tables where useful.
- Ask for missing ICP, JTBD, product metric, or transcripts only when required.

## Core principles

- Opportunities are customer pains, frictions, wishes, wants, or desires.
- Avoid solution-in-disguise framing.
- Anchor opportunities to a specific JTBD phase and moment.
- Use a controlled phase vocabulary when a phase map exists.
- Treat misfits as signal that the phase map may need revision.
- Prioritize using customer-grounded importance and prevalence.
- Keep outputs human-readable and markdown-friendly.
