# Personal Context Portfolio

This repo is Samson Schirmer's Codex-maintained second brain.

It has two jobs:

1. Give AI agents enough context to work with Samson without a long re-introduction.
2. Accumulate knowledge over time as a living, Git-backed wiki.

The setup combines the original Personal Context Portfolio template with Andrej Karpathy's LLM Wiki pattern: raw sources stay immutable, the wiki is maintained by the LLM, and `AGENTS.md` defines the operating rules.

## Start Here

- `AGENTS.md` — instructions for Codex and other agents maintaining this repo
- `Personal_Context/index` — human-readable index of Samson's current context files
- `Personal_Context/wiki/index.md` — maintained wiki index
- `Personal_Context/log.md` — append-only operating log
- `Personal_Context/raw/` — source material waiting to be processed or preserved
- `GETTING-STARTED.md` — original setup guide for the broader portfolio template

## What's In The Core Profile

Ten files cover the major dimensions of Samson's working context:

| File | What It Captures |
|------|-----------------|
| `Personal_Context/identity` | Who Samson is in one page |
| `Personal_Context/role-and-responsibilities` | What his weeks actually look like |
| `Personal_Context/current-projects` | Active workstreams, status, priority, and success signals |
| `Personal_Context/team-and-relationships` | Key people, interaction style, and stakeholder dynamics |
| `Personal_Context/tools-and-systems` | Work stack, personal stack, and integration principles |
| `Personal_Context/communication-style` | How Samson writes and how he wants writing to sound |
| `Personal_Context/goals-and-priorities` | What he is optimizing for and deliberately ignoring |
| `Personal_Context/preferences-and-constraints` | Hard rules, strong preferences, and energy patterns |
| `Personal_Context/domain-knowledge` | Expertise, beginner areas, and mental models |
| `Personal_Context/decision-log` | Decision style and durable strategic choices |

## Second Brain Workflow

Drop new material into `Personal_Context/raw/inbox/`, then ask Codex:

> Ingest the new second-brain sources and update my personal context portfolio.

Codex should summarize the source, update affected pages, cross-link related ideas, append the log, and commit/push the changes when asked or when running the scheduled maintenance job.

## Repo Structure

```text
personal-context-portfolio/
├── AGENTS.md                    ← Codex operating manual
├── README.md                    ← this file
├── GETTING-STARTED.md           ← original portfolio guide
├── Personal_Context/            ← Samson's live context and second brain
│   ├── raw/                     ← immutable source layer
│   ├── wiki/                    ← LLM-maintained synthesis layer
│   ├── log.md                   ← append-only operating log
│   └── index                    ← navigation map for agents
├── templates/                   ← original templates plus second-brain templates
├── examples/                    ← original example profiles
├── wiring/                      ← guides for connecting the portfolio to AI tools
└── interview-protocol/          ← original interview prompt
```

## Design Principles

- Markdown-first, because every AI system can read it.
- Modular, so agents can load the relevant slice instead of the whole life story.
- Living, not static, with Codex doing the maintenance work.
- Git-backed, so changes are reviewable, portable, and recoverable.

