# Second Brain

Samson Schirmer's personal knowledge base — a git-tracked, LLM-maintained wiki that serves as the single source of truth for work context across multiple AI platforms.

**Agents: read [`schema/WIKI_SCHEMA.md`](schema/WIKI_SCHEMA.md) before doing anything.**

---

## Three-Layer Model

| Layer | Path | Purpose |
|-------|------|---------|
| **Raw** | `raw/`, `Personal_Context/raw/` | Immutable source material. Never edited. |
| **Wiki** | `wiki/` | LLM-maintained interlinked markdown (people, initiatives, concepts). |
| **Schema** | `schema/`, root agent files | Behavioral contracts for agent operations. |

## Platform Read Paths

| Platform | File | Status |
|----------|------|--------|
| Codex | `AGENTS.md` | Active |
| Replit | `projections/.replit-context.md` | Active |
| Writer | `projections/writer-knowledge.md` | Active |
| VS Code | Repo files directly | Active |
| Claude | `CLAUDE.md` | Parked (~Aug 2026) |

## Start Here

- [`index.md`](index.md) — catalog of all wiki pages
- [`wiki/overview.md`](wiki/overview.md) — running synthesis
- [`MEMORY_CONTEXT.json`](MEMORY_CONTEXT.json) — structured state (workstreams, team, decisions)
- [`log.md`](log.md) — chronological record of all operations
- [`schema/WIKI_SCHEMA.md`](schema/WIKI_SCHEMA.md) — full operating contract

## Original Context Layer

The `Personal_Context/` directory contains the original ten profile pages (identity, role, projects, team, tools, communication style, goals, preferences, domain knowledge, decision log). These remain authoritative source material and are referenced by wiki pages.

## Ingest Workflow

Drop trusted material into `Personal_Context/raw/inbox/`, then ask the librarian agent to ingest. Untrusted/external material goes to `pending/` for human review before it touches the wiki.

## Repo Structure

```
├── README.md                      # this file
├── AGENTS.md                      # Codex schema (active)
├── CLAUDE.md                      # Claude schema (parked)
├── MEMORY_CONTEXT.json            # structured state
├── index.md                       # wiki page catalog
├── log.md                         # append-only operation log
├── .gitignore
├── raw/                           # immutable sources (new structure)
│   └── .gitkeep
├── wiki/                          # LLM-maintained knowledge
│   ├── overview.md
│   ├── people/
│   ├── initiatives/
│   └── concepts/
├── pending/                       # untrusted material awaiting review
├── schema/
│   └── WIKI_SCHEMA.md             # canonical librarian contract
├── projections/                   # read-only platform views
│   ├── .replit-context.md
│   └── writer-knowledge.md
├── skills/librarian/              # portable librarian skill
│   ├── SKILL.md
│   └── META.json
├── Personal_Context/              # original profile pages + local wiki
├── templates/                     # portfolio templates
├── examples/                      # example profiles
├── wiring/                        # integration guides
└── interview-protocol/            # interview agent prompt
```

## Design Principles

- Markdown-first — every AI system can read it.
- No RAG, no vector DB — plain markdown + `index.md` is the retrieval layer.
- Single-writer discipline — one librarian agent maintains the wiki.
- Git-backed — changes are reviewable, portable, recoverable.
- Never fabricate — unknowns get `TODO:` placeholders.
