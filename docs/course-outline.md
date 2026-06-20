# CSE 115A Summer 2026
## Software Engineering in the Age of AI — Lectures and Labs

---

## Week 1: Foundations

### Lecture 01 – Foundations

**Topics**
- Engineering ≠ programming.
- Deterministic vs. probabilistic systems.
- Language models, transformers, self-attention, tokens.
- **Engineering realities:** hallucination, bias, cost.
- **Behavior shifts:** non-determinism, phrasing sensitivity, unreadable logic.
- Demand: specification, validation, edge cases, oversight.
- TDD, continuous testing.
- AI-driven SDLC.

### Lab 01 – Intro to Coding Agents

**Topics**
- Introduction to Coding agents
- Planning
- Prompting basics
- Rules
- Agent Skills
- Subagents
- MCP integration

---

## Week 2: Software Requirements to Agents

### Lecture 02 – From Requirements to Agentic Development

**Topics**
- User stories → requirements → specifications.
- Functional vs. non-functional requirements.
- LLMs, reasoning models, and agents.
- Coding harness.
- Spec-driven development.
- Workflow: Understand codebase → plan → TDD → verify → commit.

### Lab 02 – Agent Skills, Rules, Guardrails & Tools

- **Skills:** Reusable agent capabilities defined by name, scope, and success criteria.
- **Four types of Rules:**
  1. Project Rules (`.cursor/rules`)
  2. User Rules
  3. Team Rules
  4. `AGENTS.md`
- **Guardrails:** Safety mechanisms including approval gates, file locks, and execution restrictions.
- **Tools:** File operations, code search, terminal execution, and version control.

---

## Week 3: Architecture & Agent Systems

### Lecture 03 – System Architecture & AI Agent Systems

**Topics**
- System architecture: decomposition, abstraction, coupling vs. cohesion.
- Architecture patterns: monolithic, microservices, layered, event-driven.
- Quality trade-offs: scalability, performance, availability, cost.
- Conway's Law: architecture mirrors organization.
- AI agent architecture: model + tools + instructions + memory + guardrails.
- Orchestration patterns: sequential, parallel, ReAct, coordinator, hierarchical.

### Lab 03 – Spec-Driven Development Exercise

- Take a user story and write a technical specification.
- Define functional requirements, edge cases, and acceptance criteria.
- Feed the spec to coding agents and review the agent's implementation plan.
- Write outcome-based tests **before** any feature code **(TDD basics)**.
- Testing framework MCPs: **Vitest (JS/TS)**, **Pytest (Python)**, **Playwright (E2E/browser)**.
- Review, verify, and commit.

---

## Week 4: Security in the Age of AI

### Lecture 04 – Security in the Age of AI

**Topics**
- **Security foundations:** defense in depth, least privilege, separation of duties, secure by design.
- **Canvas breach case study:** broken access control, monitoring gaps, missing kill switches.
- **OWASP 2025:** broken access control, misconfiguration, supply chain, injection, logging failures.
- **OWASP ASI 2026:** ten agentic attack vectors across goal, resource, state, and multi-agent tiers.
- **Defense in depth:** input sanitization, instruction hierarchy, programmable privilege, observability.

### Lab 04 – Introduction to ADK

- ADK installation and project structure.
- Agents, tools, instructions, and model configuration.
- Custom tool functions and tool bindings.
- Running agents via CLI and web playground.
- Multi-tool agents and tool selection reasoning.
- Live iteration on agent instructions and behavior.

---

## Week 5: Agent Quality

### Lecture 05 – Agent Quality

**Topics**
- **Observability:** logging, tracing, and reasoning traces for agents.
- **Key metrics:** latency, token usage, tool call success rates, task completion.
- **Evaluation strategies:** outcome-based, behavioral, regression testing.
- **Debugging non-deterministic systems:** characterize behavior, don't trace code.
- **Continuous monitoring:** anomaly detection, drift, and alerting.
- **From evaluation to improvement:** feedback loops and iterative refinement.

### Lab 05 – Sessions, State & Memory

- **Session management:** creating, resuming, and isolating agent sessions.
- **State:** reading and writing key-value data within a session.
- Short-term vs. long-term memory patterns.
- Building a stateful agent that remembers across turns.
- Context window management and compaction strategies.
- Testing stateful behavior: verifying persistence and isolation.

---

> Detailed lab assignments will be provided separately.
