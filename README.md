# Personal Knowledge Management Vault

A Git-based, long-term knowledge repository where ideas, knowledge, research,
planning, documentation, and project preparation are created, organized, and
maintained *before* work moves into separate implementation repositories.

This repository preserves the complete thinking process behind future work:
knowledge, decisions, evidence, and reusable assets. Implementation code lives
in separate repositories.

## Structure

```
pkm/
├── Ideas/       # Opportunities and concepts; earliest-stage thinking
├── Knowledge/   # Evergreen knowledge; concepts, principles, trade-offs
├── Research/    # Investigations, evaluations, experiments, findings
├── Projects/    # Planned or active initiatives; milestones, tasks, docs
├── ADRs/        # Architectural Decision Records; decisions & their reasoning
├── Proposals/   # Formal recommendations, solutions, and strategic plans
├── Data/        # Data assets + their documentation/dictionaries/schemas
├── Templates/   # Markdown scaffolds for each workspace
└── README.md
```

Each entry (a piece of knowledge, research line, project, decision, proposal,
or data asset) is a **workspace**: a directory holding a main Markdown note
plus any supporting files (diagrams, data, assets, sub-notes). Workspaces are
independent and scale naturally without being limited to a single file.

## Frontmatter

All templates share a canonical frontmatter set:

| Field | Type | Notes |
|---|---|---|
| `title` | string | empty default |
| `date` | string | `{{date}}` placeholder |
| `author` | string | empty default |
| `last_audited` | string | `{{date}}` placeholder |
| `tags` | array | `[]` |
| `status` | string | section-specific enum (see Templates) |
| `sources` | array | external links/DOIs |
| `references` | array | internal `[[wikilinks]]` / path mentions |

`references` is the connection mechanism between workspaces: point to related
workspaces instead of duplicating their content. Workspaces remain physically
independent but logically connected.

## Lifecycle (optional)

Information may mature through a conceptual pipeline, with **Data** acting as a
supporting asset repository connected to any stage (not a sequential one):

```
            Data
          ↗  ↑  ↖
Idea → Knowledge → Research → Project → ADR → Proposal
```

The pipeline is **optional**, never mandatory. A topic progresses only through
the workspaces meaningful to it; some topics may exist solely as knowledge.

## Workflow

1. Copy the matching template from `Templates/` into its section folder and
   rename it to describe the entry (e.g. `Projects/launch-website.md`).
2. Fill in the YAML frontmatter and body sections.
3. Commit at logical checkpoints: `git add <workspace> && git commit`.

## Git Usage

- Each section is tracked independently, so commits are scoped per workspace.
- Use a branch per long-running workspace if desired: `git switch -c
  research/<topic>`.
- Tag stable snapshots: `git tag v1-kb-YYYY-MM-DD`.

## Templates & Status Legends

- `ideas.md` — status: `seed | sprouting | evergreen`
- `knowledge.md` — status: `fleeting | literature | permanent`
- `research.md` — status: `active | on-hold | completed`
- `projects.md` — status: `planning | active | done | archived`
- `adr.md` — status: `proposed | accepted | deprecated | superseded`
- `proposals.md` — status: `draft | submitted | approved | rejected`
- `data.md` — status: `seed | curated | deprecated`