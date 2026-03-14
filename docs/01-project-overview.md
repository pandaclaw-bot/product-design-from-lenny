# Project Overview

## Project goal

Turn `product-design-from-lenny` into a public, shareable project instead of leaving it buried inside a private working repository.

The public version should let other people understand three things:

1. what the skill does
2. how to install and use it
3. how the skill itself was constructed over time

## Public-project principle

This repo should not be only a final artifact drop.
It should preserve the construction logic behind the skill:

- design boundaries
- method choices
- iteration path
- tradeoffs
- practical installation and adaptation guidance

## Included layers

### 1. Skill layer

The reusable skill itself:
- `SKILL.md`
- `references/`

### 2. Build-process layer

The design and iteration story:
- why the skill exists
- how it was shaped
- what changed over time
- why certain directions were abandoned

### 3. Usage layer

Practical docs for:
- OpenClaw
- Claude Code
- Codex and similar IDE agents

## Non-goals

This public project should not expose:

- private workspace memory files
- personal assistant system files
- unrelated projects from the same monorepo
- private business materials or customer data

## Intended audience

- people who want to reuse the skill
- people learning how to build agent skills
- teams wanting a portable product-design prompt/module
