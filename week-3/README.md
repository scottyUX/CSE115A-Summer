# Week 3: Architecture & Agent Systems

## Overview
This week zooms out from individual agents to full systems. We study software architecture principles, then map them onto AI agent systems — understanding how orchestration patterns, memory, and guardrails shape agent architecture the same way coupling and cohesion shape traditional systems.

---

## Lecture 03 – System Architecture & AI Agent Systems

### Software Architecture Fundamentals
- **Decomposition** — breaking a system into smaller, independently understandable pieces.
- **Abstraction** — hiding implementation detail behind clean interfaces.
- **Coupling vs. cohesion** — low coupling and high cohesion remain the goal in agentic systems.

### Architecture Patterns
| Pattern | Characteristics |
|---|---|
| Monolithic | Single deployable unit; simple but hard to scale |
| Microservices | Independent services; scalable but operationally complex |
| Layered | Clear separation of concerns across horizontal tiers |
| Event-driven | Decoupled producers and consumers; reactive and async |

### Quality Trade-offs
Every architecture decision involves trade-offs across: **scalability**, **performance**, **availability**, and **cost**. There is no free lunch.

### Conway's Law
> *"Any organization that designs a system will produce a design whose structure is a copy of the organization's communication structure."*

Your agent architecture will mirror your team structure whether you intend it to or not.

### AI Agent Architecture
A complete agent system is composed of five elements:

```
Agent = Model + Tools + Instructions + Memory + Guardrails
```

### Orchestration Patterns
| Pattern | When to use |
|---|---|
| Sequential | Steps depend on each other; order matters |
| Parallel | Independent subtasks that can run concurrently |
| ReAct | Reason → Act → Observe loop for dynamic decisions |
| Coordinator | Central agent delegates to specialist subagents |
| Hierarchical | Nested layers of coordination for complex workflows |

---

## Lab 03 – Cursor Guardrails

### What You'll Do
Configure a project-level guardrail in Cursor and verify it blocks an action that a rule alone cannot enforce.

### Colab
- [`lab-03-guardrails.ipynb`](./lab-03-guardrails.ipynb) — [Open in Colab](https://colab.research.google.com/github/scottyUX/CSE115A-Summer/blob/main/week-3/lab-03-guardrails.ipynb)

### Lab Goals
- [ ] Explain why guardrails differ from rules.
- [ ] Name the three guardrail types and map each to a Cursor mechanism.
- [ ] Create a `beforeShellExecution` hook that blocks destructive shell commands.
- [ ] Verify the guardrail fires when you test a blocked command.
- [ ] Commit the hook files to git.

---

## Lab 03 — Cursor Rules Sprint

**File:** [`lab-03-cursor-rules.ipynb`](./lab-03-cursor-rules.ipynb)

**Practice repo:** [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint) (public)

Individual exercise: write one Cursor project rule (`.mdc`) and open a pull request. Completes in **~10 minutes**.

### What You'll Do
- Read a self-contained rules intro (basic–medium concepts from the [Cursor Rules docs](https://cursor.com/docs/rules))
- Clone [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint)
- Choose one rule type to practice (Always Apply, Specific Files, Apply Intelligently, or rule with examples)
- Verify the rule in **Cursor Settings → Rules**
- Open a PR to `scottyUX/repo-analysis-sprint`

### Rule type options
| Option | Rule type | Reference issue |
|---|---|---|
| A | Always Apply | [#20](https://github.com/scottyUX/repo-analysis-sprint/issues/20) |
| B | Apply to Specific Files | [#21](https://github.com/scottyUX/repo-analysis-sprint/issues/21) |
| C | Apply Intelligently | [#22](https://github.com/scottyUX/repo-analysis-sprint/issues/22) |
| D | Rule with examples | [#23](https://github.com/scottyUX/repo-analysis-sprint/issues/23) |

### Lab Goals
- [ ] Cloned repo-analysis-sprint and opened in Cursor
- [ ] Created your `.mdc` rule in `.cursor/rules/`
- [ ] Rule visible in Cursor Settings → Rules
- [ ] PR opened to scottyUX/repo-analysis-sprint

---

## Lab 03 — Spec-Driven Development

**File:** [`lab-03-spec-driven-development.ipynb`](./lab-03-spec-driven-development.ipynb)

**Practice repo:** [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint) (public)

Optional **30–45 minute** extension after the rules sprint. Use [GitHub Spec Kit](https://github.com/github/spec-kit) to run a lean specify → plan → tasks → implement workflow with the Cursor `cursor-agent` integration.

### What You'll Do
- Install Spec Kit CLI and initialize `repo-analysis-sprint` with `--integration cursor-agent`
- Run `/speckit.constitution`, `/speckit.specify`, `/speckit.plan`, `/speckit.tasks`, `/speckit.implement`
- Build a **risk level badge** feature from a provided user story
- Verify with `npm run lint` and `npm test`
- Open a PR linking to `specs/<feature>/` artifacts

### Lab Goals
- [ ] Installed `specify-cli` and ran `specify init` with `cursor-agent`
- [ ] Ran `/speckit.specify` on the risk badge user story
- [ ] Ran `/speckit.plan` and `/speckit.tasks`
- [ ] Ran `/speckit.implement`; lint and tests pass
- [ ] Opened PR referencing `specs/...` artifacts

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
- [Cursor Rules docs](https://cursor.com/docs/rules)
- [GitHub Spec Kit](https://github.com/github/spec-kit)
- [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint)
