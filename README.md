# Personal Knowledge Management Vault

A git-based, scalable knowledge base organized into four independent sections.

## Structure

```
pkm/
├── Knowledge/   # Notes by topic; each topic is its own workspace
├── Research/    # Research workspaces with data, logs, citations
├── Projects/    # Active/done project workspaces with tasks & milestones
├── Ideas/       # Idea workspaces, from seed to evergreen
├── Data/        # Data workspaces: data files (csv/json/...) + explanatory notes
├── Templates/   # Markdown scaffolds for each section
└── README.md
```

Each entry (a piece of knowledge, research line, project, or idea) is a
**workspace**: a directory holding a main Markdown note plus any supporting
files (diagrams, data, assets, sub-notes). Workspaces are independent and
scale naturally without being limited to a single file.

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

## Templates

- `knowledge.md` — status: `fleeting | literature | permanent`
- `research.md` — status: `active | on-hold | completed`
- `projects.md` — status: `planning | active | done | archived`
- `ideas.md` — status: `seed | sprouting | evergreen`
