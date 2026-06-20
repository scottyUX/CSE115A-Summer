# Week 2: Software Requirements to Agents

## Overview
This week bridges classical software requirements engineering with modern agentic development. We learn how to translate user needs into precise specifications that a coding agent can act on reliably.

---

## Lecture 02 – From Requirements to Agentic Development

### Key Concepts
- **User stories → requirements → specifications** — the pipeline from fuzzy need to actionable, testable spec.
- **Functional vs. non-functional requirements** — what the system does vs. how well it does it.
- **LLMs, reasoning models, and agents** — understanding the tool hierarchy and when to use each.
- **Coding harness** — the environment, rules, and scaffolding that shape agent behavior.
- **Spec-driven development** — writing the spec first so the agent has clear success criteria.

### The Agentic Development Workflow
```
Understand codebase → Plan → TDD → Verify → Commit
```
Each step is explicit. Agents don't guess — they follow a spec and you verify the result.

---

## Lab 02 – Agent Skills, Rules, Guardrails & Tools

### Skills
Reusable agent capabilities defined by **name**, **scope**, and **success criteria**. Think of skills as composable building blocks — write once, invoke anywhere.

### Rules
Four types of rules govern how an agent behaves:

| Type | Location | Scope |
|---|---|---|
| Project Rules | `.cursor/rules` | Per-repository |
| User Rules | User settings | Per-developer |
| Team Rules | Shared config | Per-team |
| `AGENTS.md` | Repo root | Per-project, portable |

### Guardrails
Safety mechanisms that prevent agents from taking unintended actions:
- **Approval gates** — require human sign-off before certain operations.
- **File locks** — restrict which files an agent can modify.
- **Execution restrictions** — limit which commands or tools are available.

### Tools
The primitive capabilities agents use to act on the world:
- **File operations** — read, write, create, delete.
- **Code search** — semantic and lexical search across a codebase.
- **Terminal execution** — run shell commands, scripts, and tests.
- **Version control** — stage, commit, branch, and diff via git.

### Lab Goals
- [ ] Define a skill with a clear name, scope, and success criteria.
- [ ] Write a project rule and verify the agent respects it.
- [ ] Configure at least one guardrail (approval gate or file lock).
- [ ] Use two or more tools in a single agent workflow.
- [ ] Document your rules in `AGENTS.md`.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
