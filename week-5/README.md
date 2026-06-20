# Week 5: Agent Quality

## Overview
Building an agent that works once is not enough. This week focuses on making agents reliable, measurable, and improvable over time. We cover observability, evaluation strategies, and debugging non-deterministic systems — then get hands-on with session management, state, and memory in Lab 05.

---

## Lecture 05 – Agent Quality

### Observability
You cannot improve what you cannot see. Three pillars:
- **Logging** — capture inputs, outputs, and tool calls at every step.
- **Tracing** — follow a request through the full agent execution graph.
- **Reasoning traces** — record the model's chain-of-thought for post-hoc analysis.

### Key Metrics
| Metric | What it tells you |
|---|---|
| Latency | How long the agent takes end-to-end |
| Token usage | Cost and context consumption per run |
| Tool call success rate | How often tool invocations succeed vs. fail |
| Task completion rate | How often the agent achieves the stated goal |

### Evaluation Strategies
| Strategy | Description |
|---|---|
| Outcome-based | Did the agent produce the correct final result? |
| Behavioral | Did the agent follow the expected steps and constraints? |
| Regression testing | Does a change break previously passing behaviors? |

### Debugging Non-Deterministic Systems
> *Characterize behavior — don't trace code.*

Classical debuggers are the wrong tool. Instead:
1. Run the agent many times and observe the distribution of outputs.
2. Identify failure modes by category, not by individual trace.
3. Adjust instructions, constraints, or tools — not line-by-line logic.

### Continuous Monitoring
- **Anomaly detection** — flag outputs that fall outside expected distributions.
- **Drift detection** — catch when model behavior shifts over time (model updates, data changes).
- **Alerting** — route anomalies to humans before they compound.

### From Evaluation to Improvement
Evaluation is only useful if it drives change. The feedback loop:
```
Evaluate → Identify failure modes → Adjust spec/instructions/tools → Re-evaluate → Commit
```

---

## Lab 05 – Sessions, State & Memory

### What You'll Do
Build a stateful agent that maintains context across multiple turns — then write tests to verify that state persists correctly and is properly isolated between sessions.

### Session Management
- **Creating sessions** — initialize a new isolated agent context.
- **Resuming sessions** — pick up where you left off without losing state.
- **Isolating sessions** — ensure one session's state cannot leak into another.

### State
- Agents read and write **key-value data** within a session.
- State is scoped to the session — it does not persist by default across restarts.

### Memory Patterns
| Pattern | Scope | Use case |
|---|---|---|
| Short-term memory | Within a session | Multi-turn conversation context |
| Long-term memory | Across sessions | User preferences, project facts |

### Context Window Management
- Context windows are finite — long conversations will hit limits.
- **Compaction strategies:** summarize older turns, evict stale state, prioritize recent context.

### Testing Stateful Behavior
- Verify that state written in turn N is readable in turn N+1.
- Verify that session A's state is not visible in session B.
- Test behavior at context window boundaries.

### Lab Goals
- [ ] Create a new agent session and write a value to state.
- [ ] Resume the session and confirm the value persists.
- [ ] Build an agent that references prior-turn state in its responses.
- [ ] Demonstrate session isolation with two parallel sessions.
- [ ] Implement a basic compaction strategy and verify it doesn't lose critical state.
- [ ] Write at least two tests for stateful behavior.

---

## Resources
- Course outline: [`docs/course-outline.md`](../docs/course-outline.md)
