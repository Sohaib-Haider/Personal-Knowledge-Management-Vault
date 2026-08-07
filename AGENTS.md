# Personal Knowledge Management Vault

## Project Overview

A Git-based, long-term knowledge repository (PKM vault) that preserves the
complete thinking process — ideas, knowledge, research, decisions, proposals,
and data — before work moves into separate implementation repositories.
It holds knowledge only; implementation code lives elsewhere.

## Project Structure

```
pkm/
├── ADRs/       # decisions & reasoning
├── Data/       # data assets + schemas
├── Ideas/      # earliest-stage thinking
├── Knowledge/  # evergreen knowledge
├── Projects/   # planned / active initiatives
├── Proposals/  # recommendations & plans
├── Research/   # investigations & experiments
├── Templates/  # canonical scaffolds (source of truth)
├── .opencode/agents/   # custom subagents
├── AGENTS.md           # this file — rules for AI
└── README.md           # human-facing description
```

For human-readable detail (frontmatter fields, status legends), read
`README.md`. This file only states the rules an AI must follow here.

## Source of Truth

- Never invent facts, citations, DOIs, or sources.
- Distinguish stated facts from inference; flag uncertainty explicitly.
- Prefer accuracy over completeness — omit rather than fabricate.
- If you cannot verify something, say so and ask instead of guessing.

## Auto Validation Policy

AI responses must never be treated as correct on the first attempt.

Before presenting any response or performing any modification to the
repository, the AI must execute an internal self-validation and refinement
loop.

For each validation pass, critically review the entire response as if it had
been written by another AI. Attempt to identify:

- factual inaccuracies
- logical errors
- hallucinations
- unsupported claims
- weak reasoning
- missing considerations
- inconsistencies
- ambiguity
- unnecessary complexity
- opportunities to produce a clearer or higher-quality answer

Whenever an issue is found, revise the response and repeat the validation.

Continue this process for up to **10 validation iterations**, or stop earlier
only when an entire validation pass finds no further improvements.

The objective is not merely to check formatting or compliance with repository
rules. The objective is to maximize the correctness, completeness, clarity,
and reliability of the final response before it is presented or any repository
changes are made.

Never assume the first generated answer is the best answer.

## Editing Rules

- Make only the necessary changes; preserve existing content.
- Never modify unrelated notes or workspaces.
- Never delete or reorganize content without explicit instruction.
- Prefer incremental improvements over large rewrites.

## Workspace & Template Rules

- Place content in the correct workspace (Ideas ≠ Research, etc.).
- Before creating or editing a file, open and mirror the matching template in
  `Templates/` — it defines the frontmatter fields, section layout, and
  `status` enum for that workspace.
- Preserve the required frontmatter exactly as the template specifies.

## Knowledge Linking

- Prefer linking over duplication: use `references` / `[[wikilinks]]`.
- Ensure references resolve to existing workspaces.
- Update references when a linked note changes.

## Ask Before You Act

- Ask when information is missing or ambiguous.
- Ask before destructive or large structural changes.
- Never replace uncertainty with assumptions.

## Absolute Guardrails

- **Atomicity** — no Markdown file exceeds **150 lines**; split overflow into
  sub-files inside the workspace and link them.
- **Discoverability & auditability** — keep `date`, `last_audited`,
  `Changelog`, and accurate `references`; commit per workspace.
- **No guessing** — when a decision could change the outcome, ask me.
