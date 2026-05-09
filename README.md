# PM_skills

A reusable Product Management skill pack.

## Invocation

When I say **`PM_skills`**, respond using the instructions in this repo.

Primary skill currently installed:

- **Product Discovery Skills** — based on https://github.com/Elsevanderberg1/product-discovery-skills

This skill pack is designed for customer interview discovery workflows: ICP screening, JTBD phase mapping, opportunity extraction, opportunity reset, and opportunity sizing.

## Product Discovery Pipeline

```text
PM_skills
  └── product-discovery
        ├── icp-screener
        ├── phase-map-analyst
        ├── opportunity-analyst
        ├── opportunity-analyst-reset
        └── opportunity-sizer
```

Source repo pipeline:

```text
icp-screener → phase-map-analyst → opportunity-analyst → opportunity-mapper → opportunity-sizer
                       ↑                    │
                       └───── feedback ─────┘
                       via opportunity-analyst-reset
```

## How to use in ChatGPT / Codex

Use prompts like:

```text
PM_skills: screen these customer interviews against this ICP: ...
PM_skills: create a JTBD phase map from these transcripts
PM_skills: extract opportunities from this interview transcript
PM_skills: size and prioritize these opportunities
```

The detailed behavior is defined in:

- `AGENTS.md` — global instruction for agents working in this repo
- `skills/PM_skills/SKILL.md` — wrapper skill invoked by `PM_skills`
- `skills/product-discovery/SKILL.md` — product-discovery pipeline behavior

## Source attribution

This repo adapts the workflow from Else van der Berg's public `product-discovery-skills` repo:

https://github.com/Elsevanderberg1/product-discovery-skills

Original concepts include ICP screening, JTBD phase maps, Teresa Torres-style customer opportunities, Opportunity Solution Trees, importance × prevalence sizing, and misfit-driven phase-map revision.
