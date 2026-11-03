# Learning outcomes

After completing the six modules, a learner should be able to do the following. Each outcome is traceable to the sources listed; no outcome requires a deployment, a code submission, or a source outside S1–S10.

## Module 1 — Foundations of AI Agents

- Define an AI agent in one paragraph, without confusing it with a chatbot, a prompt, or a single model call. [S6, S7, S8]
- Explain the ReAct loop (Thought → Act → Observation) and why reasoning and acting must be interleaved, not done in separate phases. [S4]
- Distinguish a workflow (predefined code paths) from an agent (dynamic direction and tool use), and state when each is appropriate. [S6]
- Explain why compound systems — model plus tools, data, retrieval, and memory — are needed for complex, varied tasks. [S8]

## Module 2 — Architecture and Components

- Describe an agent's components: model, tools, instructions, memory/sessions, and the execution loop with feedback. [S7, S6, S9]
- Explain how LangGraph structures an agent as a graph of shared state, nodes, and edges, with durable execution and persistence. [S2]
- Explain how the Agents SDK structures an agent as primitives — Agents, tools, handoffs, guardrails, sessions, tracing — and what each primitive is for. [S9]
- Explain what MCP adds to an architecture: standardised context and tool integration between Hosts, Clients, and Servers. [S3]

## Module 3 — Agent Workflows and Multi-Agent Systems

- Name and explain the five Anthropic patterns — prompt chaining, routing, parallelisation, orchestrator-workers, evaluator-optimizer — and give a use case for each. [S6]
- Compare manager orchestration (agents as tools) with decentralised orchestration (handoffs), including traceability and failure trade-offs. [S7, S9]
- Explain conversation programming: multi-agent applications as conversations between customisable, conversable agents. [S5]
- Apply the rule "start simple, add complexity only when it demonstrably improves outcomes" to a multi-agent proposal, and identify when *not* to use multi-agent. [S6]

## Module 4 — Frameworks and Technologies

- Explain what ADK, LangGraph, MCP, and the OpenAI Agents SDK each do, in one paragraph each, without calling a protocol a framework or a framework a protocol. [S1, S2, S3, S9]
- Explain what changed in ADK 2.0 vs 1.x: Workflow Runtime, graph nodes, and the breaking changes to events, agent execution, callbacks, and retries. [S1]
- Explain what changed in MCP 2026-07-28 vs earlier versions: stateless requests, per-request negotiation, opt-in extensions, and security principles. [S3]
- Explain the Agents SDK's guardrails (parallel validation, fail fast), sessions (persistent working context), and tracing (visualise, debug, monitor, evaluate). [S9]

## Module 5 — Evaluation, Reliability and Safety

- Explain how Agent-SafetyBench measures agent safety: scale, risk categories, failure modes, and headline finding — and its limits as a 2024–2025 preprint. [S10]
- Distinguish capable (can complete the task), safe (will not cause harm while doing it), and reliable (performs consistently over long sessions and recovers from failures). [S10, S2, S1, S9]
- Design a layered guardrail plan: validation, authentication, authorisation and access controls, tool-use consent, sandboxed testing, and human-in-the-loop for high-risk actions. [S7, S6, S9, S3]
- Explain why guardrails alone are not enough, using the robustness and risk-awareness defects from S10. [S10]
- State, honestly, what this source set does *not* prove about reliability and multi-agent safety. [Project gaps]

## Module 6 — Real-world Applications

- Describe two applications actually in the sources — customer support and coding — with their patterns, tools, and limits. [S6, S7, S5, S9]
- Apply the selection rule: agents for open-ended, varied tasks; programmatic systems for narrow, well-defined, repeatable tasks. [S8, S6]
- For a new application proposal, state which sources support it, which guardrails it needs, and how its safety would be evaluated — or state that the sources do not support it. [S1–S10]

## Assessment note

These outcomes are assessed by the verification methodology in `verification-methodology.md`: a learner demonstrates an outcome by answering a question whose answer cites the correct source and is supported by the cited passage. A polished summary without a supporting citation does not demonstrate an outcome.
