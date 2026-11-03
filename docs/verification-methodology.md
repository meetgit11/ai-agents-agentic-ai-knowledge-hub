# Verification methodology

## Principle

A notebook answer is not verified because it sounds plausible. It is verified only when (1) it cites a source actually in the notebook, (2) the cited source is the right source for that claim, and (3) the cited passage actually supports the claim. This methodology was used for the NotebookLM notebook behind this repository, and it should be reused for any future source change.

## Step 1 — Import check

For each of S1–S10, confirm in NotebookLM: listed, title correct, preview readable, no error.

Risks watched in this project:

- **ArXiv papers (S4, S5, S10):** if NotebookLM imports only the abstract, grounding is weak. Fix, without adding a new source: use **View PDF** on the same arXiv page and replace the abstract import with the PDF of the same paper.
- **YouTube (S8):** import depends on transcript availability. If it fails, report the exact error; do not substitute a different video without approval.
- **SDK docs (S9):** the approved URL is the landing overview, not the full Tools / Guardrails / Sessions sub-pages. If detail questions fail, ask before adding sub-pages, because NotebookLM counts each URL as a source and the set is already at 10.
- **MCP (S3):** the URL must be the 2026-07-28 specification, not the 2025-06-18 page. A session/handshake answer is a sign the wrong version was imported.

## Step 2 — Question test

Ask questions in NotebookLM chat, one at a time, covering all six modules plus cross-module synthesis. The full question set used in Stage 2 includes, per module:

- **Module 1:** What is an agent vs a workflow? What is the ReAct loop? Why compound systems?
- **Module 2:** What are an agent's components? How do LangGraph and the Agents SDK structure an agent differently? What is MCP (Hosts, Clients, Servers)?
- **Module 3:** What are the five Anthropic patterns? Manager vs decentralised? When not to use multi-agent?
- **Module 4:** Compare ADK, LangGraph, MCP, and the Agents SDK. What changed in ADK 2.0? What changed in MCP 2026-07-28? What are guardrails, sessions, and tracing in the Agents SDK?
- **Module 5:** How does Agent-SafetyBench measure safety, and what did it find? Safe vs reliable vs capable? Why are guardrails alone not enough?
- **Module 6:** Two real-world applications from the sources, with limits. When do agents help most, and when do programmatic systems win?
- **Cross-module:** Design a support agent from multiple sources, with reasons. What does this notebook *not* prove?

## Step 3 — Blocker questions

Three questions must pass before sharing. A failure on any blocker is a fix-first result, regardless of how well the other questions scored:

1. **ADK 2.0 vs 1.x:** architecture changed from hierarchical executor to graph-based Workflow Runtime; Event gains `node_info` and `output`; `BaseAgent` subclasses `BaseNode`; legacy overrides are bypassed; events must be yielded; automatic retries and human-in-the-loop pauses can be broken by broad exception handling.
2. **MCP 2026-07-28 vs earlier:** stateless, self-contained requests with per-request capability negotiation; opt-in extensions (Tasks, Skills over MCP, MCP Apps); security principles of user consent, data privacy, and tool safety.
3. **Agent-SafetyBench:** 349 environments, 2,000 cases, 8 risk categories, 10 failure modes, 16 agents, none above 60%; defects of robustness and risk awareness; defense prompts alone may be insufficient.

## Step 4 — Scoring

- **Pass:** at least 16 of 18 verification questions answered with a correct, supporting citation, including all 3 blockers.
- **Partial:** 12–15 of 18, with all 3 blockers passing — fix the failed non-blocker questions, then re-run only those questions.
- **Fail / fix first:** any blocker fails, or more than 3 answers cite the wrong source. Fix by re-importing (PDF swap), re-checking the S3 URL, or correcting a mis-titled source, then re-run only the failed questions.

## Step 5 — Studio check

Generate Studio outputs one at a time (audio/video overview, mind map, flashcards, quiz, infographic, slide deck, report) and check each against the same rule: does it cite the right source, and does the cited passage support the claim? A polished output with a wrong citation is a failure, not a pass. Retain the limitations section in any report or deck — do not delete it for polish.

## Status for this project

On 3 November 2026, the author reported that all 10 sources imported cleanly and that the blocker questions passed. That result was reported from inside NotebookLM and cannot be independently verified from GitHub; it is recorded here as author-reported, not as a tool-verified result.

## Reuse rule

If any source is added, removed, or replaced in the future, re-run Steps 1–4 for the affected modules and update `source-inventory.md` and `module-map.md` in the same change. Do not update a version claim silently — record the version, date, and source URL.
