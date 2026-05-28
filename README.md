# Agentic AI Design Patterns

A personal, completed deep-dive into software design patterns for building intelligent, autonomous AI agents. Each pattern is implemented as a self-contained Jupyter notebook with code, explanations, and runnable examples.

> **Built for learning.** I completed this repository for my own educational growth — to go beyond simple prompt-response loops and understand how to architect agentic AI systems from the ground up. It serves as a reference I can revisit for future projects and architectural decisions.

---

## Patterns Overview

| # | Pattern | What It Is | Best For |
|---|---------|------------|----------|
| 1 | **Reflection** | The agent generates output, critiques itself, and revises before delivering a final answer. | Tasks where output quality matters more than speed — code generation, writing, reasoning. |
| 2 | **Tool Use** | The agent calls external tools (APIs, search, calculators) to gather information or act. | Any task requiring real-time data or actions the model cannot do from memory alone. |
| 3 | **ReAct (Reason + Act)** | The agent interleaves reasoning with action in a think → act → observe loop. | Multi-step research, web QA, or any task where the path to an answer is unknown upfront. |
| 4 | **Planning** | A dedicated planner decomposes a goal into ordered sub-tasks before execution. | Predictable workflows like data pipelines, report generation, or structured project execution. |
| 5 | **Multi-Agent Systems** | Multiple specialized agents collaborate, each with a distinct role, overseen by a coordinator. | Problems spanning multiple domains — e.g., a team of researcher, writer, and reviewer agents. |
| 6 | **PEV (Planner-Executor-Verifier)** | A three-stage pipeline: plan, execute step-by-step, verify each output and re-plan on failure. | High-precision, safety-critical applications like finance or healthcare. |
| 7 | **Blackboard Systems** | Specialist agents contribute to a shared data store; a controller dynamically decides who acts next based on the evolving state. | Ill-structured problems with no fixed solution path — diagnostics, multi-modal reasoning. |
| 8 | **Episodic + Semantic Memory** | Dual memory: a vector store for past conversations (episodic) and a graph store for extracted facts (semantic). | Long-running personal assistants, tutors, or apps that must remember users over weeks. |
| 9 | **Tree-of-Thoughts** | The agent explores multiple reasoning branches in parallel, evaluating and pruning to find the best path. | Logic puzzles, constraint-satisfaction problems, creative generation with backtracking. |
| 10 | **Mental Loop (Simulator)** | The agent simulates actions in a sandboxed model before executing in the real world. | High-stakes domains where mistakes are costly — trading, robotics, medical decisions. |
| 11 | **Meta-Controller (Router)** | A supervisory agent inspects each request and routes it to the best-suited sub-agent. | Platforms handling diverse request types — customer support ticketing, multi-service AI. |
| 12 | **Graph / World-Model Memory** | Facts are parsed into entities and relationships stored in a graph database for multi-hop querying. | Enterprise knowledge management, research assistants reasoning over interconnected data. |
| 13 | **Ensemble Decision** | Multiple agents with different perspectives solve the same problem; an aggregator synthesizes results. | Ambiguous, high-stakes questions where a single viewpoint may be biased. |
| 14 | **Dry-Run Harness** | Proposed actions are logged in a sandbox; a human must approve before live execution. | Production systems performing irreversible actions — sending emails, posting content, spending money. |
| 15 | **Self-Improvement Loop** | An agent generates output, a critic evaluates it against a rubric, and the agent revises iteratively. | High-quality content generation, personalized assistants that learn preferences over time. |
| 16 | **Cellular Automata** | Simple cell-agents on a grid follow local rules to produce emergent global intelligence. | Spatial reasoning, logistics, pathfinding, simulation of emergent phenomena. |
| 17 | **Reflexive Metacognitive** | The agent maintains a self-model of its own knowledge and limitations, deciding when to answer, use a tool, or escalate. | High-stakes advisory (medical, legal, financial) where guessing would be dangerous. |

---

## Quick Start

```bash
pip install -r requirements.txt
jupyter notebook
```

Open any notebook and run the cells. Each notebook is self-contained — no dependencies between them.

---

## Notes

This is a personal educational repository completed for self-study. While it's public and freely available for anyone to learn from, I'm not actively seeking contributions — I built it to solidify my own understanding and to have a reusable architectural reference for future work.

---

## License

MIT
