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

## Lab 03 – Spec-Driven Development Exercise

### What You'll Do
Take a real user story through the full spec-driven workflow — from fuzzy requirement to committed, tested code.

### Steps
1. **Write a technical specification** from a provided user story.
2. **Define functional requirements**, edge cases, and acceptance criteria.
3. **Feed the spec to a coding agent** and review its implementation plan.
4. **Write tests first** — outcome-based tests before any feature code **(TDD)**.
5. **Run the agent** and let it implement against your tests.
6. **Review, verify, and commit.**

### Testing Frameworks (via MCP)
| Framework | Language / Use case |
|---|---|
| **Vitest** | JavaScript / TypeScript unit tests |
| **Pytest** | Python unit and integration tests |
| **Playwright** | End-to-end and browser-based tests |

### Lab Goals
- [ ] Produce a written technical spec from a user story.
- [ ] Define at least three acceptance criteria.
- [ ] Write failing tests before running the agent.
- [ ] Verify all tests pass after agent implementation.
- [ ] Commit with a meaningful message.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
