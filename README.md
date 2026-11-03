# AI Agents & Agentic AI — Complete Knowledge Hub

> A source-grounded learning hub exploring AI Agents and Agentic AI, covering architectures, workflows, frameworks, multi-agent systems, evaluation, safety, and real-world applications.

**Project:** BSERC GenAI Internship — Project 1 (Week 1, AI notebook)
**Author:** Meet Patil — 3rd-year B.Tech, Computer Science and Engineering, Pimpri Chinchwad University (PCU), Pune, Maharashtra, India
**Notebook title:** AI Agents & Agentic AI – Complete Knowledge Hub
**Status:** Learning and documentation hub. This repository is **not** a deployed AI agent system, and it does not claim that any agent described in the sources has been deployed by this project.

## What this repository is — and is not

This repository is the public, citable companion to a Google NotebookLM notebook built from exactly 10 approved sources (S1–S10, see [Source references](#source-references)). It contains original summaries, a module structure, a source inventory, and a verification methodology — all written for learning.

It is **not**:

- a deployed agent, product, or service;
- a reproduction of copyrighted papers, articles, or videos — those works are linked, not uploaded, and remain the property of their respective owners;
- a claim that NotebookLM outputs are custom-built software — NotebookLM is a separate learning tool used to test questions and generate study materials from the sources.

## Objectives

1. Explain, fundamentals first, what an AI agent is and how it differs from a workflow, a framework, a protocol, and a benchmark.
2. Organise the topic into six coherent learning modules, each traceable to specific sources.
3. Compare the major implementation routes in the sources — Google ADK, LangGraph, Model Context Protocol (MCP), and the OpenAI Agents SDK — as different jobs, not as a single ranking.
4. Teach evaluation and safety as part of building, not as an afterthought, using a dedicated agent-safety benchmark.
5. Give learners a verifiable way to test understanding: questions whose answers must cite a source in the notebook, with version-sensitive claims (ADK 2.0, MCP 2026-07-28) checked explicitly.

## Six learning modules

| Module | Focus | Primary sources |
|---|---|---|
| 1. Foundations of AI Agents | What an agent is; the ReAct loop; workflow vs agent; compound systems | S4, S6, S7, S8 |
| 2. Architecture and Components | Model, tools, instructions, memory/sessions, execution loop | S1, S2, S3, S4, S6, S7, S8, S9 |
| 3. Agent Workflows and Multi-Agent Systems | Five workflow patterns; manager vs decentralised orchestration; handoffs; conversation programming | S1, S2, S4, S5, S6, S7, S9 |
| 4. Frameworks and Technologies | ADK 2.0, LangGraph, MCP 2026-07-28, OpenAI Agents SDK | S1, S2, S3, S9 |
| 5. Evaluation, Reliability and Safety | Guardrails, tracing, consent, human-in-the-loop; Agent-SafetyBench | S1, S3, S6, S7, S9, S10 |
| 6. Real-world Applications | Customer support and coding agents, with limits; when agents help and when programmatic systems win | S1, S5, S6, S7, S8, S9 |

See [docs/module-map.md](docs/module-map.md) for the full coverage matrix.

## Methodology

1. **Source-first, in stages.** Stage 1 selected 8 verified sources. Stage 1.1 retained all 8, added the OpenAI Agents SDK documentation (S9) and a dedicated safety paper (S10), updated MCP to the 2026-07-28 specification, and clarified ADK 2.0 vs 1.x. No source, URL, author, or date was invented.
2. **NotebookLM as the test bed.** The 10 sources were imported into a NotebookLM notebook under the title above. Questions were then asked in NotebookLM chat and checked for correct source citation — see [docs/verification-methodology.md](docs/verification-methodology.md).
3. **Fundamentals before advanced claims.** Definitions and the ReAct loop are taught before framework comparisons; guardrail principles are taught before benchmark numbers; and every version-sensitive claim is labelled with its version and date.
4. **Honesty about gaps.** Reliability beyond safety, multi-agent safety specifically, dedicated memory/context-engineering, and India-specific applications are gaps in this 10-source set, not findings. They are listed in [docs/project-overview.md](docs/project-overview.md), not filled by inference.

## Project architecture

This is a documentation and learning architecture, not a software deployment architecture:

```text
Sources (S1–S10, external, linked only)
        │
        ▼
NotebookLM notebook (learning + Q&A + Studio study materials)
        │
        ▼
This repository (public documentation)
  ├── README.md — objectives, modules, methodology, sources
  └── docs/
      ├── project-overview.md
      ├── module-map.md
      ├── source-inventory.md
      ├── verification-methodology.md
      └── learning-outcomes.md
```

There is no application code, no API server, and no agent runtime in this repository, because none is claimed. If a future stage adds code, it will be added as a separate, explicitly described component — not retroactively claimed for this stage.

## Expected outcomes

After working through the six modules, a learner should be able to:

- Define an AI agent, explain the ReAct loop, and distinguish a workflow from an agent.
- Describe an agent's components (model, tools, instructions, memory/sessions) and how LangGraph and the Agents SDK structure them differently.
- Choose among the five Anthropic workflow patterns and between manager and decentralised multi-agent orchestration, with reasons.
- Explain what ADK 2.0, LangGraph, MCP, and the Agents SDK each do, and what changed in ADK 2.0 and in MCP 2026-07-28.
- Explain how Agent-SafetyBench measures safety, what it found, and why guardrails alone are not enough.
- Apply the selection rule for applications: agents for open-ended, varied tasks; programmatic systems for narrow, well-defined, repeatable tasks.

Full outcomes are in [docs/learning-outcomes.md](docs/learning-outcomes.md).

## NotebookLM verification — status

On 3 November 2026, the author reported that all 10 sources imported cleanly into NotebookLM and that the blocker verification questions passed — ADK 2.0 vs 1.x, MCP 2026-07-28 vs earlier versions, and Agent-SafetyBench. This is an author-reported result from inside NotebookLM; it cannot be independently verified from GitHub, and this repository does not present NotebookLM's internal outputs as its own files.

## Source references

All 10 approved sources. URLs are the original, verified URLs from Stage 1.1. No copyrighted full text is included in this repository.

| ID | Source | Type | URL |
|---|---|---|---|
| S1 | Google ADK — ADK \| Gemini Enterprise Agent Platform \| Google Cloud Documentation | Official documentation | https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/adk |
| S2 | LangGraph overview — Docs by LangChain | Official documentation | https://docs.langchain.com/oss/python/langgraph/overview |
| S3 | Model Context Protocol — Specification 2026-07-28 | Official documentation | https://modelcontextprotocol.io/specification/2026-07-28 |
| S4 | ReAct: Synergizing Reasoning and Acting in Language Models — Yao et al. | Research paper | https://arxiv.org/abs/2210.03629 |
| S5 | AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation — Wu et al. | Research paper | https://arxiv.org/abs/2308.08155 |
| S6 | Building effective AI agents — Schluntz & Zhang, Anthropic Engineering | Technical article | https://www.anthropic.com/engineering/building-effective-agents |
| S7 | A Practical Guide to Building AI Agents — OpenAI | Technical article | https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/ |
| S8 | What are AI Agents? — Maya Murad, IBM Technology | YouTube lecture | https://www.youtube.com/watch?v=F8NKVhkZZWI |
| S9 | OpenAI Agents SDK | Official documentation | https://openai.github.io/openai-agents-python/ |
| S10 | Agent-SafetyBench: Evaluating the Safety of LLM Agents — Zhang et al., Tsinghua CoAI | Research paper | https://arxiv.org/abs/2412.14470 |

Full details — authors, dates, modules, educational value, and credibility notes — are in [docs/source-inventory.md](docs/source-inventory.md).

**Count:** 4 official documentation (S1, S2, S3, S9) + 3 research papers (S4, S5, S10) + 2 technical articles (S6, S7) + 1 YouTube lecture (S8) = 10, at the top of the BSERC 5–10 source range for Project 1. Do not add an 11th source without removing one or obtaining approval to expand the set.

## Version warnings — read before reusing any claim

- **ADK:** Teach ADK 2.0 first (Workflow Runtime, graph nodes; GA: Python 19 May 2026, Go 30 June 2026, TypeScript 21 August 2026). ADK 1.x hierarchical examples are legacy/migration context.
- **MCP:** Teach the 2026-07-28 specification first (stateless, self-contained requests, per-request capability negotiation). Do not teach the old session/handshake flow as current.
- **Dates matter:** S4 (2022–2023), S5 (2023), S6 (Dec 2024, with a tooling-change note), S8 (Jul 2024), and S10 (Dec 2024 / May 2025 preprint) are foundational, pattern, or benchmark sources. S1–S3 and S9 are current implementation sources. Never mix their dates into a single timeless claim.

## Repository structure

```text
ai-agents-agentic-ai-knowledge-hub/
├── README.md
├── LICENSE
└── docs/
    ├── project-overview.md
    ├── module-map.md
    ├── source-inventory.md
    ├── verification-methodology.md
    └── learning-outcomes.md
```

## License and third-party material

The MIT License in [LICENSE](LICENSE) applies only to the original text in this repository (this README, the docs folder, and any future original material added by the author). It does not claim ownership of, and does not license, any third-party source material. Papers, articles, documentation, and videos referenced here remain the property of their respective authors and publishers, are linked rather than reproduced, and are subject to their own terms.

## Contributing

Corrections are welcome, especially version corrections: if ADK, LangGraph, MCP, or the Agents SDK releases a new major version, open an issue noting the version, date, and source URL, rather than editing a version claim silently. Do not add new sources in a pull request without updating the source inventory and the module map in the same change.
