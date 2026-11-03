# Module map

Six approved learning modules, in learning order: foundations first, applications last. Every module is traceable to specific sources; no module is taught from memory alone.

## Module 1 — Foundations of AI Agents

**Questions this module answers:** What is an AI agent? How does it differ from a workflow, a chatbot, and a single model call? What is the ReAct loop?

**Key ideas:** An agent perceives, reasons, acts with tools, observes results, and learns from feedback. A workflow orchestrates LLMs and tools through predefined code paths; an agent dynamically directs its own process and tool use. ReAct interleaves reasoning traces with actions — Thought → Act → Observation, repeated. Compound systems combine models with databases, tools, retrieval, and memory.

**Primary sources:** S4, S6, S7, S8. Supporting: S1, S2, S3, S5, S9, S10.

## Module 2 — Architecture and Components

**Questions this module answers:** What are an agent's components? How do different frameworks structure them?

**Key ideas:** The durable anatomy is model + tools + instructions, augmented by retrieval and memory, with a persistent session / checkpoint layer for long-running work. LangGraph structures an agent as a graph of shared state, nodes, and edges. The Agents SDK structures an agent as primitives: Agents, tools, handoffs, guardrails, sessions, tracing. There is no single universal component list — the overlap across sources is the reliable core.

**Primary sources:** S1, S2, S3, S4, S6, S7, S8, S9. Supporting: S5, S10.

## Module 3 — Agent Workflows and Multi-Agent Systems

**Questions this module answers:** Which workflow pattern fits which task? When does multi-agent help, and when does it only add cost?

**Key ideas:** Five patterns — prompt chaining, routing, parallelisation, orchestrator-workers, evaluator-optimizer. Manager orchestration (a central agent calls others as tools) vs decentralised orchestration (agents hand off directly). Conversation programming: multi-agent applications built as conversations between customisable, conversable agents. Rule: start simple; add complexity only when it demonstrably improves outcomes.

**Primary sources:** S1, S2, S4, S5, S6, S7, S9. Supporting: S3, S8, S10.

## Module 4 — Frameworks and Technologies

**Questions this module answers:** What does each technology actually do? What changed in its current version?

**Key ideas, as a comparison, not a ranking:**

- **Google ADK (S1):** enterprise framework to build, debug, and deploy agents; in 2.0, a graph-based Workflow Runtime (graph, dynamic, collaborative workflows).
- **LangGraph (S2):** low-level orchestration runtime for stateful, long-running agents (graphs, state, nodes, edges, persistence, human-in-the-loop).
- **MCP (S3):** a protocol, not a framework — it standardises context and tool integration between Hosts, Clients, and Servers; the 2026-07-28 version is stateless with per-request capability negotiation.
- **OpenAI Agents SDK (S9):** a lightweight, production-ready Python package with few abstractions — Agents, function/hosted/MCP tools, handoffs, guardrails, sessions, tracing.

**Primary sources:** S1, S2, S3, S9. Supporting: all others at a supporting level.

## Module 5 — Evaluation, Reliability and Safety

**Questions this module answers:** How is agent safety measured? Why are guardrails alone not enough? What is the difference between safe, reliable, and capable?

**Key ideas:** Layered guardrails — input/output validation, authentication, authorisation and access controls, tool-use consent, sandboxed testing, human-in-the-loop for high-risk actions. Tracing and evaluation as part of safety, not an afterthought. Agent-SafetyBench (S10): 349 interaction environments, 2,000 test cases, 8 categories of safety risks, 10 common failure modes; 16 agents evaluated, none above 60% safety; two fundamental defects — lack of robustness and lack of risk awareness; defense prompts alone may be insufficient. Limits: arXiv preprint, 2024–2025 model snapshots. Reliability (drift, compounding errors, cost/latency) remains a gap — see `project-overview.md`.

**Primary sources:** S1, S3, S6, S7, S9, S10. Supporting: S2, S4.

## Module 6 — Real-world Applications

**Questions this module answers:** Where do agents help most? Where do programmatic systems still win? What are the limits of the best-evidenced applications?

**Key ideas:** Best-evidenced applications in the sources: customer support (routing, retrieval, tools, guardrails, human escalation) and coding (generate, test in sandbox, evaluate, fix, in an evaluator-optimizer loop). Selection rule: agents for complex, varied, open-ended tasks where the path cannot be fully predefined; programmatic systems for narrow, well-defined, repeatable tasks where determinism, cost, and latency matter. No deployment beyond what the sources describe is claimed.

**Primary sources:** S1, S5, S6, S7, S8, S9. Supporting: S2, S3, S4, S10.

## Coverage matrix

● = primary coverage, ○ = supporting coverage, — = no meaningful coverage

| Module | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 | S10 |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 Foundations | ○ | ○ | ○ | ● | ○ | ● | ● | ● | ○ | ○ |
| 2 Architecture | ● | ● | ● | ● | ○ | ● | ● | ● | ● | ○ |
| 3 Workflows / Multi-Agent | ● | ● | ○ | ● | ● | ● | ● | ○ | ● | ○ |
| 4 Frameworks | ● | ● | ● | ○ | ○ | ○ | ○ | ○ | ● | ○ |
| 5 Evaluation / Safety | ● | ○ | ● | ○ | — | ● | ● | — | ● | ● |
| 6 Applications | ● | ○ | ○ | ○ | ● | ● | ● | ● | ● | ○ |

Every module has at least three primary sources. Module 4 has four primary documentation sources; Module 5 has six primary sources, with S10 as the dedicated benchmark anchor.
