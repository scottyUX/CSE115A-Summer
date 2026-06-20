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

**File:** [`lab-01-intro-to-cursor.ipynb`](./lab-01-intro-to-cursor.ipynb)

### What You'll Do
Install Cursor, learn the agent interface, and build a working grade calculator using the full agentic workflow — from planning through testing to commit.

### Topics Covered
- **Install and configure Cursor** — student Pro discount, sign in, verify setup.
- **Meet the Cursor Agent** — four modes (Agent/Plan/Ask/Debug), tools, checkpoints, queued messages, Agents Window, Agent Review.
- **Planning** — Grill Me → Plan Mode → incremental execution workflow.
- **Prompting** — anatomy of a strong prompt, @ mentions, visual context, model selection.
- **Rules** — `.mdc` format, application modes, AGENTS.md, best practices.
- **Skills** — SKILL.md format, project vs. user scope, TDD skill exercise.
- **Subagents** — built-in agents, when to delegate, four role-based agents (Planner, Engineer, QA, Reviewer).
- **MCP integration** — connect Vercel, Supabase, and Figma.

### Lab Goals
- [ ] Cursor installed, signed in with `.edu` email, and Pro plan confirmed.
- [ ] Course repo cloned and indexed in Cursor.
- [ ] Agent chat opened and three practice prompts sent.
- [ ] `BUGBOT.md` created with at least three review rules.
- [ ] Planning workflow completed — Grill Me → Plan Mode → incremental execution.
- [ ] `grade_calculator.py` created using a strong structured prompt.
- [ ] `python-style.mdc` and `commit-format.mdc` rules created and verified.
- [ ] `tdd` skill created in `.cursor/skills/` and verified in Cursor Settings.
- [ ] Four role subagents created in `.cursor/agents/` (Planner, Engineer, QA, Reviewer).
- [ ] Vercel, Supabase, and Figma MCP servers connected and reachable.
- [ ] Work committed and pushed.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
- [Cursor Docs — Agent](https://cursor.com/docs/agent)
- [Cursor Docs — Rules](https://cursor.com/docs/rules)
- [Cursor Docs — Skills](https://cursor.com/docs/skills)
- [Cursor Docs — MCP](https://cursor.com/docs/mcp)
