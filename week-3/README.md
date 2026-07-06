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

## Lab 03 — Cursor Rules Sprint

**File:** [`lab-03-cursor-rules.ipynb`](./lab-03-cursor-rules.ipynb)

**Practice repo:** [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint) (public)

Four teams each write one Cursor project rule (`.mdc`) and open a pull request. Completes in **~10 minutes**.

### What You'll Do
- Read a self-contained rules intro (basic–medium concepts from the [Cursor Rules docs](https://cursor.com/docs/rules))
- Clone [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint)
- Write one rule matching your team's assigned type (Always Apply, Specific Files, Apply Intelligently, or rule with examples)
- Verify the rule in **Cursor Settings → Rules**
- Open a PR to `scottyUX/repo-analysis-sprint`

### Team assignments
| Team | Rule type | Issue |
|---|---|---|
| 1 | Always Apply | [#20](https://github.com/scottyUX/repo-analysis-sprint/issues/20) |
| 2 | Apply to Specific Files | [#21](https://github.com/scottyUX/repo-analysis-sprint/issues/21) |
| 3 | Apply Intelligently | [#22](https://github.com/scottyUX/repo-analysis-sprint/issues/22) |
| 4 | Rule with examples | [#23](https://github.com/scottyUX/repo-analysis-sprint/issues/23) |

### Lab Goals
- [ ] Cloned repo-analysis-sprint and opened in Cursor
- [ ] Created assigned `team-N-*.mdc` in `.cursor/rules/`
- [ ] Rule visible in Cursor Settings → Rules
- [ ] PR opened to scottyUX/repo-analysis-sprint

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
- [Cursor Rules docs](https://cursor.com/docs/rules)
- [repo-analysis-sprint](https://github.com/scottyUX/repo-analysis-sprint)
