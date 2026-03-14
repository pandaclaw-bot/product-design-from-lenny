# English Adapter Guide

This file keeps the English-facing integration notes separate from the main Chinese README.

## For Claude Code

Read the target `SKILL.md` first, then read the related `references/` files when the task is complex.

Example:

```text
Read ./skills/lenny-product-positioning/SKILL.md first. Use it as the working framework for this task.
```

## For Codex / IDE agents

Keep the skill folders inside a repo-local path such as:

```text
.ai/skills/lenny-product-positioning/
.ai/skills/lenny-product-plan/
```

Then tell the agent to read the relevant skill before planning implementation.

## For OpenClaw

Copy the needed skill folders into your `skills/` directory and keep the folder structure unchanged.
