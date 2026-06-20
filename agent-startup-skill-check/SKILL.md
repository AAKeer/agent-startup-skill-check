---
name: agent-startup-skill-check
description: Use at the start of a new project or project session to ensure the project root has AGENT_STARTUP.md and to make checking available Skills a default first step before any task, without limiting Skill usage to specific task categories.
---

# Agent Startup Skill Check

Use this skill when starting work in a new project or when the user asks to make Skill usage part of the project startup workflow.

## Startup File Rule

Before starting any task in a project, check whether `AGENT_STARTUP.md` exists in the project root.

If `AGENT_STARTUP.md` does not exist, create it before doing anything else.

The file must contain exactly:

```markdown
AI_CONTEXT.md

Before starting any task, first check available Skills.

Read any Skills that may be relevant.

Let existing Skills guide your work whenever appropriate.

Treat Skills as reusable knowledge, not optional references.
```

Do not overwrite or recreate `AGENT_STARTUP.md` if it already exists unless the user explicitly asks.

If `AGENT_STARTUP.md` already exists, read it before starting work and follow its instructions.

## Skill Usage Rule

After the startup file check, inspect available Skills before continuing.

Read any Skill that may be relevant to the current task.

Do not restrict Skill usage to a fixed set of task categories. A Skill may be relevant for coding, writing, planning, research, debugging, review, file work, tool usage, project conventions, or any other task where reusable knowledge can improve the result.

Skip extra Skill loading only when the available Skills are clearly unrelated or would not materially improve the work.

## Operating Principle

Treat Skills as reusable project knowledge, not optional references. Use them when they can improve correctness, consistency, maintainability, or fit with project conventions.
