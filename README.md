# Product Design from Lenny

A reusable product-design skill distilled from Lenny’s Podcast product conversations and rebuilt for agent workflows.

This project is not only the final skill. It also documents how the skill was designed, narrowed, revised, and made usable in real-world agent setups.

## What this project includes

- `SKILL.md`: the public skill itself
- `references/`: source references and reusable method notes
- `docs/`: design rationale, evolution, and build process
- `examples/`: example prompts and usage patterns

## What this skill does

Use this skill when you want an agent to help with product planning and feature design using a structured lens inspired by top product leaders.

Typical use cases:
- turn a rough idea into a clearer product concept
- design an MVP or a feature scope
- structure a product proposal for discussion
- borrow product-design heuristics from high-signal interviews and operator thinking

## What this skill does not try to do

This project is intentionally narrow.

It does not aim to be:
- a full product operating system
- a complete PRD generator for every situation
- a replacement for direct user research
- a source-of-truth transcript archive

## Download and install

### Option A: Clone the repo

```bash
git clone <your-public-repo-url>
cd product-design-from-lenny
```

### Option B: Copy only the skill files

At minimum, copy these into your own workspace:

- `SKILL.md`
- `references/`

If your environment supports skill packages, keep the folder structure intact.

## Install in OpenClaw

Recommended layout:

```text
skills/
└── product-design-from-lenny/
    ├── SKILL.md
    └── references/
```

Then place this project folder under your OpenClaw skill workspace or copy it into your existing `skills/` directory.

If you keep it as a standalone repo, the easiest pattern is:

1. clone this repo locally
2. copy or symlink `product-design-from-lenny/` into your OpenClaw skills directory
3. restart or reload your agent environment if needed

Suggested usage prompt in OpenClaw:

```text
Use the product-design-from-lenny skill to turn this idea into a structured product proposal. Focus on users, pain points, MVP scope, workflow, risks, and success metrics.
```

## Adapt for Claude Code

Claude Code does not use OpenClaw-native skill packaging, so the practical approach is to use this project as a reusable prompt-and-reference module.

Recommended patterns:

### Pattern 1: Keep as a local reference folder

- put this repo next to your product project
- ask Claude Code to read `SKILL.md` and the relevant docs before drafting

Example:

```text
Read ./product-design-from-lenny/SKILL.md and use it as the working framework for this task. Then design an MVP for the following product idea...
```

### Pattern 2: Convert into a team prompt asset

- keep `SKILL.md` as the core instruction file
- keep `references/` as optional reading
- keep `examples/` as onboarding examples

This works well when your team wants a repeatable product-design prompt standard.

## Adapt for Codex and other IDE agents

For Codex-style coding agents, this repo works best as a checked-in workflow module.

Recommended patterns:

### Pattern 1: Repo-local skill folder

Place the folder in your repo:

```text
.ai/
  skills/
    product-design-from-lenny/
```

Then prompt the agent:

```text
Read ./.ai/skills/product-design-from-lenny/SKILL.md and use that framework to design the product plan before writing implementation tasks.
```

### Pattern 2: Prompt + references split

- `SKILL.md` = operating instruction
- `docs/` = design rationale and build philosophy
- `references/` = deeper reusable notes
- `examples/` = few-shot guidance

This split works well in Codex, Claude Code, Cursor, Windsurf, and similar IDE agents.

## Compatibility guidance

This project is designed to be portable across agent environments because it separates:

- the reusable instruction layer
- the method/rationale layer
- the examples layer

That means you can:
- use it natively as a skill in environments that support skill folders
- use it as a prompt framework in environments that do not
- embed it into internal team workflows as a reusable product-design module

## Suggested repo structure for sharing

```text
product-design-from-lenny/
├── README.md
├── SKILL.md
├── docs/
├── references/
└── examples/
```

## How this skill was built

If you want the construction process instead of just the artifact, start here:

- `docs/01-project-overview.md`
- `docs/02-how-the-skill-was-built.md`
- `docs/03-design-evolution.md`
- `docs/04-public-repo-boundary.md`

## Publishing checklist

Before pushing this as a public repo, verify:

- no private client material is included
- no personal workspace files are included
- no large data files are included
- examples are safe to share
- the README matches the final folder structure

## Status

Prepared as a public-project version from a larger working repository.
Further cleanup, examples, and license selection can be added before final publication.
