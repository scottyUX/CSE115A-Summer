# Week 2: Software Requirements to Agents

## Overview
This week bridges classical software requirements engineering with modern agentic development. We learn how to translate user needs into precise specifications that a coding agent can act on reliably. Labs cover the Cursor CLI, Skills, and the Rules/Guardrails/Tools system.

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

## Lab 02 — Cursor CLI

**File:** [`lab-02-cursor-cli.ipynb`](./lab-02-cursor-cli.ipynb)

The Cursor CLI (`agent`) gives you the full power of Cursor Agent from the terminal — no GUI required. Use it for automation, CI pipelines, and long-running background tasks.

### What You'll Do
- Install the CLI and authenticate with your `.edu` account.
- Start an interactive agent session and switch between Agent, Plan, and Ask modes.
- Use shell mode to run commands from inside a conversation.
- Run the agent non-interactively with `-p` for scripts and pipelines.
- Use slash commands to manage context, sessions, and models.
- Push long-running tasks to Cloud Agent.

### Lab Goals
- [ ] CLI installed and `agent --version` returns a version.
- [ ] `agent status` shows Pro plan and `.edu` email.
- [ ] Interactive session started — agent described the project files.
- [ ] Switched between Agent, Plan, and Ask modes in a live session.
- [ ] Used shell mode to run a command and used the output as context.
- [ ] Ran a non-interactive review with `-p`.
- [ ] Used `/summarize`, `/rename`, `/clear`, and `/resume`.

---

## Lab 02b — Cursor Skills

**File:** [`lab-02b-cursor-skills.ipynb`](./lab-02b-cursor-skills.ipynb)

Skills implement progressive disclosure — the agent loads only what it needs, when it needs it. This lab builds four skills from scratch, one per skill pattern.

### What You'll Do
- Understand why skills exist and how they differ from rules and MCP servers.
- Build an instruction-only skill (`git-commit-formatter`).
- Use asset reference files to avoid hallucinating exact text (`license-header-adder`).
- Teach the agent a transformation pattern through examples (`json-to-pydantic`).
- Delegate deterministic validation to a Python script (`grade-validator`).

### Lab Goals
- [ ] `git-commit-formatter` skill created and verified in Cursor Settings.
- [ ] Agent produced a Conventional Commit message without being told the format.
- [ ] `license-header-adder` skill created with a reference file.
- [ ] New Python file created with the license header copied verbatim.
- [ ] `json-to-pydantic` skill created with a `references/` folder.
- [ ] `week-2/models.py` generated matching the example pattern.
- [ ] `grade-validator` skill created with a validation script.
- [ ] `grade_calculator.py` passes all script checks.
- [ ] All four skills committed to `.cursor/skills/`.

---

## Lab 02c — Rules, Guardrails & Tools

**File:** `lab-02c-rules-guardrails-tools.ipynb` *(coming soon)*

Rules, guardrails, and tools are the control layer of an agentic system. Rules define how the agent behaves, guardrails prevent unintended actions, and tools are the primitive capabilities the agent uses to act on the world.

### What You'll Do
- Write project and user rules in `.mdc` format.
- Configure guardrails including approval gates and file locks.
- Understand the built-in tool set and when each tool is invoked.
- Document your configuration in `AGENTS.md`.

### Lab Goals
- [ ] Write a project rule and verify the agent respects it.
- [ ] Configure at least one guardrail.
- [ ] Use two or more tools in a single agent workflow.
- [ ] Document rules in `AGENTS.md`.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
- [Cursor CLI Docs](https://cursor.com/docs/cli/overview)
- [Cursor Skills Docs](https://cursor.com/docs/skills)
- [Agent Skills Standard](https://agentskills.io)
