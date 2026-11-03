# Source inventory (Stage 1.1, approved — exactly 10 sources)

No source, URL, author, or date in this file was invented. All URLs were opened and checked during Stage 1 / Stage 1.1 on 3 November 2026. Where a page states no date, that limitation is stated explicitly. No copyrighted full text is reproduced here — only titles, bibliographic details, and original summaries, with links to the originals.

## S1 — Official documentation: Google ADK

- **Title:** ADK | Gemini Enterprise Agent Platform | Google Cloud Documentation
- **Author / organisation:** Google Cloud / Google
- **URL:** https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/adk
- **Type:** Official technical documentation
- **Date:** Last updated 2026-10-30 UTC on the page checked 3 Nov 2026. The page points to https://adk.dev/ as the "Get started" home.
- **Modules:** 2, 3, 4, 5, 6
- **Educational value:** The primary, vendor-authoritative definition of ADK: an open-source framework to build, debug, and deploy agents at enterprise scale, with workflow agents, agent-coordinated dynamic routing, native multi-agent composition, a tool ecosystem, built-in/partner evaluation tools, and deployment via Runtime, Cloud Run, or GKE, in Python, TypeScript, Go, and Java.
- **Version note:** Teach ADK 2.0 first — Workflow Runtime, graph-based execution, GA Python 19 May 2026, Go 30 June 2026, TypeScript 21 August 2026. ADK 1.x is legacy/migration context, with breaking changes to the Event schema, `BaseAgent extends BaseNode`, callbacks, yielded events, and automatic retries / human-in-the-loop pauses. ADK 1.x remains installable (for example, Python: `pip install "google-adk~=1.0"`).

## S2 — Official documentation: LangGraph (LangChain)

- **Title:** LangGraph overview — Docs by LangChain
- **Author / organisation:** LangChain
- **URL:** https://docs.langchain.com/oss/python/langgraph/overview
- **Type:** Official technical documentation
- **Date:** Updated 2026-11-03 on the page checked 3 Nov 2026
- **Modules:** 2, 3, 4, 5 (supporting)
- **Educational value:** LangGraph as a low-level orchestration framework and runtime for long-running, stateful agents, defined as graphs of shared state, nodes, and edges, mixing deterministic and LLM-driven steps, with durable execution, persistence/checkpointing, streaming, human-in-the-loop, and memory. It also clarifies the stack: Deep Agents > LangChain agents > LangGraph > LangSmith.
- **Credibility note:** Primary source, very current. Do not substitute old `langchain-ai.github.io/langgraph` links for this overview.

## S3 — Official documentation: Model Context Protocol, 2026-07-28 specification

- **Title:** Specification — Model Context Protocol (2026-07-28)
- **Author / organisation:** Model Context Protocol (open standard)
- **URL:** https://modelcontextprotocol.io/specification/2026-07-28
- **Type:** Official technical documentation / protocol specification
- **Date:** Specification dated 2026-07-28; specification page updated 2026-10-30 on the site checked 3 Nov 2026. This replaces the 2025-06-18 specification page checked in Stage 1, which must no longer be cited as current.
- **Modules:** 2, 4, 5
- **Educational value:** The authoritative protocol requirements. MCP provides a standardised way to share context with language models, expose tools and capabilities, and build composable integrations, using JSON-RPC 2.0 messages between Hosts (LLM applications), Clients (connectors inside the host), and Servers (services providing context/capabilities). Server features: Resources, Prompts, Tools. Client features include Elicitation. Extensions, always opt-in, include Tasks, Skills over MCP, and MCP Apps.
- **Version note:** The 2026-07-28 base protocol is stateless, self-contained requests with per-request capability negotiation — in contrast to the session-based model in the earlier specification. Its security section stresses user consent and control, data privacy, and tool safety: tool descriptions/annotations must be treated as untrusted unless from a trusted server, and hosts must obtain explicit user consent before invoking a tool.

## S4 — Research paper: ReAct

- **Title:** ReAct: Synergizing Reasoning and Acting in Language Models
- **Authors:** Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik Narasimhan, Yuan Cao
- **URL:** https://arxiv.org/abs/2210.03629
- **Type:** Original research paper (arXiv; ICLR camera-ready v3)
- **Date:** Submitted 6 Oct 2022 (v1); last revised 10 Mar 2023 (v3)
- **Modules:** 1, 2, 3, 5 (supporting)
- **Educational value:** Interleave verbal reasoning traces with task-specific actions, so reasoning helps induce, track, and revise plans and handle exceptions, while actions gather grounding information from external sources. Tested on HotpotQA, FEVER, ALFWorld, and WebShop.
- **Credibility note:** High for the concept, not for 2026 performance claims. Use for the loop, not for absolute scores.

## S5 — Research paper: AutoGen (multi-agent conversation)

- **Title:** AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation
- **Authors:** Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, Beibin Li, Erkang Zhu, Li Jiang, Xiaoyun Zhang, Shaokun Zhang, Jiale Liu, Ahmed Hassan Awadallah, Ryen W. White, Doug Burger, Chi Wang (Microsoft Research, Pennsylvania State University, University of Washington, Xidian University)
- **URL:** https://arxiv.org/abs/2308.08155
- **Type:** Original research paper (arXiv)
- **Date:** Submitted 16 Aug 2023 (v1); last revised 3 Oct 2023 (v2)
- **Modules:** 3, 2, 6
- **Educational value:** Build LLM applications as conversations between customisable, conversable agents (LLM, human, tool, or a combination), programmed by "conversation programming" in natural language and code. Examples span mathematics, coding, question answering, operations research, online decision-making, and entertainment.
- **Credibility note:** High for multi-agent design. Cite it for conversation programming, not as proof that the 2023 AutoGen API is current in 2026.

## S6 — Credible technical article: Anthropic, Building Effective Agents

- **Title:** Building effective AI agents
- **Authors:** Erik Schluntz and Barry Zhang, Anthropic Engineering
- **URL:** https://www.anthropic.com/engineering/building-effective-agents
- **Type:** Credible technical article / engineering guide
- **Date:** 19 December 2024. The page itself now carries a note that much of its tooling landscape has changed since December 2024.
- **Modules:** 1, 2, 3, 5, 6
- **Educational value:** Workflows (predefined code paths) vs agents (LLMs dynamically directing their own process and tool use); the augmented LLM (retrieval + tools + memory); five composable patterns — prompt chaining, routing, parallelisation, orchestrator-workers, evaluator-optimizer — plus the true agent loop; "start simple, add complexity only when it demonstrably improves outcomes", with sandboxed testing and guardrails. Appendix 1 covers customer-support and coding-agent applications.
- **Credibility note:** High for durable patterns, lower for current tooling. Use for patterns and trade-offs, not for 2026 product limits or model names.

## S7 — Credible technical article: OpenAI, A Practical Guide to Building AI Agents

- **Title:** A Practical Guide to Building AI Agents
- **Author / organisation:** OpenAI
- **URL:** https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/
- **Type:** Credible technical article / vendor practical guide (with Agents SDK code examples)
- **Date:** 2025. The page checked 3 Nov 2026 does not state an exact day in its visible text; do not cite a specific day.
- **Modules:** 1, 2, 3, 5, 6
- **Educational value:** Agents as systems that independently accomplish tasks on your behalf; the three-part anatomy — model, tools, instructions; model selection by baseline-then-optimise (evals first, then smaller/cheaper models); data / action / orchestration tool types; single-agent vs multi-agent orchestration (manager pattern: agents as tools; decentralised pattern: agents handing off to agents); guardrails layered with authentication, authorisation, and access controls.
- **Credibility note:** High as vendor deployment guidance, vendor-framed: it naturally centres OpenAI models/APIs. Pair with S1/S2 when comparing frameworks, and re-check model names in the guide before quoting them.

## S8 — Educational YouTube lecture: IBM Technology, What are AI Agents?

- **Title:** What are AI Agents?
- **Author / organisation:** Maya Murad, IBM Technology (YouTube channel: IBM Technology)
- **URL:** https://www.youtube.com/watch?v=F8NKVhkZZWI
- **Type:** Educational YouTube lecture / explainer video
- **Date:** 15 July 2024
- **Modules:** 1, 2, 6
- **Educational value:** A short, non-code entry point: the shift from monolithic models to compound AI systems, how agents integrate with databases and external tools, and why agents suit complex, varied tasks while programmatic systems suit narrow, well-defined ones. Best as the Module 1 primer before denser docs and papers.
- **Credibility note:** Medium-high for foundations, low for implementation detail. Vendor explainer, predates ADK 2.0, the 2026-07-28 MCP revision, and 2025–2026 frameworks. Use for concepts and vocabulary only.

## S9 — Official documentation: OpenAI Agents SDK

- **Title:** OpenAI Agents SDK
- **Author / organisation:** OpenAI
- **URL:** https://openai.github.io/openai-agents-python/
- **Type:** Official technical documentation
- **Date:** No publication date is stated on the landing page checked 3 Nov 2026. Treat it as current documentation to be version-pinned at build time, not as a dated paper.
- **Modules:** 2, 3, 4, 5, 6
- **Educational value:** A lightweight, production-ready package with few abstractions, described as a production-ready upgrade of Swarm. Agents are LLMs equipped with instructions and tools, with a built-in loop. Tools include function tools (any Python function, automatic schema generation, Pydantic validation), hosted tools, and MCP server tool calling. Handoffs let agents delegate to other agents for specific tasks. Guardrails validate inputs and outputs, run in parallel with execution, and fail fast. Sessions are a persistent memory layer for working context within an agent loop. Tracing visualises, debugs, and monitors workflows, with support for evaluation, fine-tuning, and distillation. Also in the docs: sandbox agents, realtime agents, voice pipelines, and human-in-the-loop mechanisms. The SDK uses the Responses API by default for OpenAI models, wrapped in a higher-level runtime.
- **Credibility note:** High. Primary, vendor-authoritative SDK documentation. This URL is the Python SDK docs; the JS SDK is a separate docs site and is not this source. Pair with S7: S7 gives the production reasoning, S9 gives the exact primitives.

## S10 — Research paper: Agent-SafetyBench

- **Title:** Agent-SafetyBench: Evaluating the Safety of LLM Agents
- **Authors:** Zhexin Zhang, Shiyao Cui, Yida Lu, Jingzhuo Zhou, Junxiao Yang, Hongning Wang, Minlie Huang — Conversational AI (CoAI) group, DCST, Tsinghua University
- **URL:** https://arxiv.org/abs/2412.14470
- **Type:** Original research paper (arXiv preprint)
- **Date:** Submitted 19 Dec 2024 (v1); last revised 20 May 2025 (v2). No peer-reviewed venue is claimed on the arXiv page checked — cite it as an arXiv preprint, not as a journal/conference paper, unless a venue is verified later.
- **Modules:** 5 (primary); 1, 2, 6 (supporting)
- **Educational value:** As LLMs are deployed as agents, integration into interactive environments and tool use introduces safety challenges beyond those of the models themselves. Agent-SafetyBench: 349 interaction environments, 2,000 test cases, 8 categories of safety risks, 10 common failure modes. Evaluation of 16 popular LLM agents found none achieved a safety score above 60%. Two fundamental safety defects: lack of robustness and lack of risk awareness. Reliance on defense prompts alone may be insufficient.
- **Relevance to Module 5:** The notebook's first source that defines an agent-safety evaluation method (not just a guardrail principle), gives a failure taxonomy students can use to classify failures, and gives a quantitative baseline to test claims like "guardrails solve agent safety" against. It pairs with S6/S7/S9: S6/S7 say what guardrails to add, S9 says how to implement guardrails/tracing in code, S10 says how to measure whether those guardrails actually work in interactive, tool-using settings.
- **Why AgentBench was not chosen instead:** AgentBench (Liu et al., arXiv:2308.03688, ICLR 2024) is a strong capability benchmark, but it primarily measures capability, not safety. Since the gap was specifically a dedicated safety/evaluation source, Agent-SafetyBench is the better fit for S10.

## Classification summary

| Count | Type | Sources |
|---|---|---|
| 4 | Official documentation | S1, S2, S3, S9 |
| 3 | Research papers | S4, S5, S10 |
| 2 | Technical articles | S6, S7 |
| 1 | YouTube lecture | S8 |
| **10** | **Total** | **S1–S10** |

No duplicates: S7 and S9 overlap on OpenAI agent concepts by design — S7 is the production guide, S9 is the SDK reference — but they have different URLs, purposes, and levels of detail, so both are retained. S6 and S7 overlap on workflow/agent definitions for the same convergence reason.
