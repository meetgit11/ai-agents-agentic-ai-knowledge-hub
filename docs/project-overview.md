# Project overview

## Context

This project is Week 1, Project 1 of a 15-day online Artificial Intelligence Internship (2026) at Bharat Space Education Research Centre (BSERC). Project 1 asks for an AI notebook on the student's own topic, built from 5–10 sources, with every NotebookLM feature tested (chat, audio/video overview, mind map, flashcards, quiz, infographic, slide deck) and the notebook link shared.

The selected topic is **AI Agents & Agentic AI**, organised as a complete knowledge hub. The notebook itself lives in Google NotebookLM; this repository is its public documentation companion.

## Problem the hub addresses

Learners encounter AI agents through disconnected sources: a framework tutorial here, a paper there, a vendor guide elsewhere. Without a shared vocabulary, four different things get confused:

1. A **workflow** (a predefined path) with an **agent** (a system that dynamically directs its own process and tool use).
2. A **framework** (ADK, LangGraph, Agents SDK) with a **protocol** (MCP).
3. A **guardrail** (a control) with an **evaluation** (a measurement of whether controls work).
4. A **capability** claim ("it can do the task") with a **safety** claim ("it will not cause harm while doing it").

This hub separates those concepts, module by module, and traces every claim back to a named source.

## Scope — and what is out of scope

**In scope:**

- Definitions, architecture, workflows, multi-agent systems, frameworks, evaluation, safety, and applications — as presented in S1–S10.
- A source inventory, a module map, a verification methodology, and learning outcomes.
- NotebookLM study materials generated from those sources and checked against them.

**Out of scope, explicitly:**

- Building or deploying an AI agent system. No agent runtime, API, or product is part of this project.
- Reproducing copyrighted papers, articles, or videos. Those works are linked, not uploaded.
- Presenting NotebookLM outputs as custom-built software.
- Any claim about a real-world deployment that S1–S10 do not describe. In particular, no BSERC, hospital, farm, or other local deployment is claimed in this project.

## Method in brief

Stage 1 selected 8 verified sources. Stage 1.1 retained all 8, added S9 (OpenAI Agents SDK documentation) and S10 (Agent-SafetyBench), updated MCP to the 2026-07-28 specification, and clarified ADK 2.0 vs 1.x. Stage 2 imported all 10 into NotebookLM, organised them by the six modules, and verified answers with citation checks, including three blocker questions on ADK 2.0, MCP 2026-07-28, and Agent-SafetyBench.

## Known gaps (not findings)

These gaps remain in the 10-source set and must not be filled by inference:

1. **Reliability beyond safety is thin.** S10 measures safety, not long-run reliability: drift over long sessions, compounding errors, cost/latency trade-offs, or recovery after tool failures (beyond ADK 2.0 retries and LangGraph checkpointing).
2. **Multi-agent safety specifically.** S10 evaluates LLM agents in interactive environments; it is not a dedicated study of multi-agent coordination failures such as delegation errors, handoff loops, or conflicting subagent goals.
3. **No dedicated memory / context-engineering source.** S2 covers persistence, S6 covers memory as augmentation, and S9 covers sessions, but no single dedicated long-term memory source is in the set.
4. **No India-specific application source.** All 10 sources are global English sources.
5. **No empirical MCP security paper.** S3 gives the specification's security principles (consent, privacy, tool safety); no paper in the set empirically evaluates MCP-specific exploits.

Because the set is at the 10-source maximum, adding a source for any of these gaps would require removing an existing source or an approved expansion — not a silent 11th addition.

## How to use this repository

- **To learn:** start with Module 1 in `module-map.md`, then follow the modules in order.
- **To verify a claim:** find its S-number in `source-inventory.md`, open the original URL, and check the date and version.
- **To test understanding:** use the verification methodology in `verification-methodology.md` — ask a question, check the cited source, and check that the cited passage actually supports the claim.
- **To cite this hub:** cite the repository for its original organisation and summaries, and cite S1–S10 separately for their own content. Do not cite this repository as the source of a paper's finding.
