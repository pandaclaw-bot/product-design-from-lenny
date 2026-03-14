# How the Skill Was Built

## Starting point

The skill did not begin as a clean public project.
It started inside a larger working repository where Lenny-derived product and strategy skills were being explored.

The initial instinct was straightforward:

- collect high-signal product ideas from strong operators
- turn them into reusable agent behavior
- help an agent produce structured product outputs instead of generic brainstorming

## Key build choices

### 1. Do not treat raw transcripts as the skill

A transcript archive is useful, but it is not a usable skill by itself.
The useful part is the distilled method:

- what to look at
- how to structure product thinking
- how to produce a usable output

### 2. Keep the skill narrow enough to be reused

The skill focuses on product planning and feature design.
That is much more reusable than trying to absorb every adjacent task.

### 3. Separate artifact from rationale

A public skill repo should let people use the final skill quickly, but it should also explain:

- why the skill is shaped this way
- what tradeoffs were made
- how it can be adapted to other agent environments

### 4. Make it portable across tools

The final repo is designed so that `SKILL.md` can act as:

- a native skill file in environments like OpenClaw
- a reusable prompt standard in Claude Code
- a repo-local agent workflow file in Codex and other IDE agents

## Build philosophy

This project follows a simple principle:

> A good public skill repo should teach both usage and construction.

That is why this repo contains:
- the final skill
- source references
- usage examples
- process and evolution docs
