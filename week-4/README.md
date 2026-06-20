# Week 4: Security in the Age of AI

## Overview
Security is not an afterthought — it is an architectural constraint. This week we study foundational security principles, examine a real-world breach, and map classic and emerging attack vectors onto agentic systems. Lab introduces the Agent Development Kit (ADK) for building production-grade agents.

---

## Lecture 04 – Security in the Age of AI

### Security Foundations
| Principle | What it means |
|---|---|
| Defense in depth | Multiple overlapping layers of control — no single point of failure |
| Least privilege | Agents and users get only the permissions they need, nothing more |
| Separation of duties | No single agent or actor can complete a sensitive operation alone |
| Secure by design | Security is baked in from the start, not bolted on at the end |

### Case Study: Canvas Breach
A real-world incident illustrating what goes wrong when security is treated as optional:
- **Broken access control** — users could access resources they shouldn't.
- **Monitoring gaps** — the breach went undetected because observability was missing.
- **Missing kill switches** — no mechanism to halt or roll back compromised behavior.

### OWASP 2025 — Top Web Risks
- Broken access control
- Security misconfiguration
- Supply chain vulnerabilities
- Injection attacks
- Logging and monitoring failures

### OWASP ASI 2026 — Agentic Security Initiative
Ten agentic attack vectors organized across four tiers:

| Tier | Attack surface |
|---|---|
| Goal | Prompt injection, goal hijacking |
| Resource | Unauthorized tool use, data exfiltration |
| State | Session poisoning, memory manipulation |
| Multi-agent | Trust escalation, rogue subagent coordination |

### Defense in Depth for Agents
- **Input sanitization** — validate and constrain all inputs before they reach the model.
- **Instruction hierarchy** — system instructions take precedence over user instructions.
- **Programmable privilege** — grant and revoke tool access dynamically based on context.
- **Observability** — log every tool call, decision, and output for audit and anomaly detection.

---

## Lab 04 – Introduction to ADK

### What You'll Do
Install and configure the Agent Development Kit, build a multi-tool agent, and iterate on its behavior live.

### Topics Covered
- **ADK installation and project structure** — setting up a clean, reproducible environment.
- **Agents, tools, instructions, and model configuration** — the four knobs you control.
- **Custom tool functions and tool bindings** — writing Python functions the agent can call.
- **Running agents via CLI and web playground** — two ways to interact and debug.
- **Multi-tool agents and tool selection reasoning** — how agents decide which tool to use.
- **Live iteration** — changing instructions mid-session and observing behavior shift.

### Lab Goals
- [ ] Install ADK and verify the environment is working.
- [ ] Define an agent with at least two custom tools.
- [ ] Run the agent via CLI and confirm tool calls appear in the trace.
- [ ] Open the web playground and run the same agent interactively.
- [ ] Modify the agent's instructions and document the behavior change.
- [ ] Identify one security concern in your agent and apply a mitigation.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
- OWASP Top 10: https://owasp.org/www-project-top-ten/
- OWASP ASI 2026: https://owasp.org/www-project-agentic-security-initiative/
