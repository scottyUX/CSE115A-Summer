# Week 1: Foundations

## Overview
This week establishes the conceptual foundation for the course. We draw a clear line between programming and engineering, introduce the probabilistic nature of AI systems, and explore what that means for how we build software today.

---

## Lecture 01 – Foundations

### Key Concepts
- **Engineering ≠ programming** — software engineering is about designing reliable systems under constraints, not just writing code.
- **Deterministic vs. probabilistic systems** — classical software behaves predictably; AI systems introduce uncertainty by design.
- **Language models under the hood** — transformers, self-attention mechanisms, and tokenization explained at a practical level.

### Engineering Realities of AI
| Challenge | What it means in practice |
|---|---|
| Hallucination | Models confidently produce incorrect output |
| Bias | Training data shapes model behavior in hidden ways |
| Cost | Token usage, latency, and inference costs are real constraints |

### Behavior Shifts When Using AI
- **Non-determinism** — the same prompt can yield different results.
- **Phrasing sensitivity** — small wording changes produce large output changes.
- **Unreadable logic** — you cannot step through a model's reasoning like code.

### Engineering Demands
- Write precise specifications before prompting.
- Validate outputs — don't assume correctness.
- Define edge cases and handle them explicitly.
- Maintain human oversight at critical decision points.
- Apply **TDD** and continuous testing to AI-integrated workflows.
- Understand the **AI-driven SDLC**: requirements → spec → agent → test → verify → commit.

---

## Lab 01 – Intro to Coding Agents

### What You'll Do
Get hands-on with a coding agent from scratch. By the end of lab you will have run your first agent, written your first prompt, and connected an external tool via MCP.

### Topics Covered
- **Introduction to Coding Agents** — what they are, how they differ from chatbots.
- **Planning** — how agents decompose tasks before executing them.
- **Prompting basics** — structure, clarity, and intent in prompts.
- **Rules** — setting behavioral boundaries for your agent.
- **Agent Skills** — reusable, composable capabilities you define.
- **Subagents** — delegating subtasks to specialized child agents.
- **MCP integration** — connecting agents to external tools and data sources.

### Lab Goals
- [ ] Install and configure your coding agent environment.
- [ ] Write and run your first structured prompt.
- [ ] Define a simple rule and verify it is respected.
- [ ] Invoke a skill and observe the output.
- [ ] Connect one MCP tool and confirm it is reachable.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
