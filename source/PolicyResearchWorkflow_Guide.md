# The Policy Research Workflow — An AI Onramps Guide

## A guide for course participants tackling a major policy research project

---

## Overview

This guide describes a structured workflow for producing a major policy research report using AI tools. It is organised into a Setup Phase and three working phases, with dedicated evaluation checkpoints at the end of Phase 2 and Phase 3.

The workflow is designed for a two-person human team — a subject lead and an AI engineer — supported by a set of AI agents, each driven by its own agent instructions file. The subject lead owns all judgment calls. The AI engineer owns the agentic tooling. The agents handle bounded, repeatable tasks under clear instructions.

A companion reference table maps every step to its human roles and AI tools. Read the table first to orient yourself; use these descriptions when you need the reasoning behind a step.

---

## Setup Phase — Framing the Project

These two steps happen before any research begins. Their outputs — the question map and the report specification — are the project's constitution. They travel with the project, get embedded in agent instructions throughout, and provide the rubric against which every subsequent output is evaluated. Time spent here pays back at every later stage.

### S1: Conceptual planning — the question

Research briefs are written to commission work, not to guide it. Your first task is to translate the brief into a precise account of what a genuinely good answer would look like: the sub-questions that need answering, the domains that need covering, the evidence that would count as strong support for each. The output is a question map — not long, but precise. An agent given a clear question map can evaluate its own output against explicit criteria. One given a vague brief cannot.

### S2: Conceptual planning — the report

The question map defines the intellectual requirements of a good answer. The report specification defines the practical requirements of a good deliverable: audience, purpose, structure, register, and what defensible looks like for this particular client. These are not the same thing, and conflating them produces reports that answer the question well but serve the client poorly — or vice versa. Settle both before any research begins.

---

## Phase 1 — Data Gathering

*Steps S3 and S4 run in parallel where the project allows.*

### S3a: Web search — landscape pass

Submit your research brief to Claude Research with minimal direction. You are not trusting its output at this stage. You are using it to discover sources you might not have found independently, to see how the tool frames the problem, and to produce a first source list as raw material for curation. When the run completes, set the report aside and focus on the sources.

### S3b: Web search — source ranking

A source ranking agent works through the landscape pass output and scores each source against explicit criteria: recency, authority, geographic and sectoral specificity, and relevance to the research question. The output is a ranked list, not a curated one — ranking is a mechanical task that an agent handles consistently; curation is a judgment call that requires domain knowledge.

### S3c: Web search — source curation

The subject lead reviews the ranked list and makes the curation decisions: which sources to prioritise, which to set aside, and which gaps need filling from their own knowledge of the domain. This step has no agent component. It is the most important quality gate in the entire workflow — gaps in the source base cannot be fixed at the report writing stage — and it belongs entirely to the human with domain expertise.

### S3d: Web search — directed extraction

A search agent works through the curated source list systematically, extracts relevant material against the research questions in the question map, and produces structured findings. The quality of this step depends directly on the quality of the agent instructions: a well-crafted brief produces consistent, usable output; a vague one produces summaries that require extensive reworking. This is where investment in the agent instructions pays off most visibly.

### S4: Offline data processing

Offline material — confidential documents, internal reports, messy spreadsheets — often contains the most valuable evidence and requires the most careful handling. The governing principle is simple: material containing sensitive or confidential data should never enter a web-connected tool. A separate, isolated Project handles raw offline material only. Clean and anonymise before uploading; review all outputs before they leave the offline environment. Nothing passes directly from this Project to the main research Project without human review.

---

## Phase 2 — Processing

### S5: Preliminary summaries

The web search and offline workstreams produce findings in different formats, at different levels of detail, organised around different principles. Preliminary summaries bring them to a common structure — organised around the question map — so they can be worked across in thematic synthesis. The human role here is review, not production: does each summary accurately represent what the source material contains, without adding interpretation the sources don't support?

### S6: Thematic synthesis

This is the intellectual centre of the project. The preliminary summaries contain findings organised by source. Thematic synthesis reorganises them by argument — across sources, across workstreams, in response to the research question. The output is not a summary of what the sources say. It is a structured account of what the evidence shows. The synthesis agent should be instructed to return to the question map, organise the evidence around it, and flag where coverage is thin or contradictory. The human review at this step is substantive — the last analytical quality gate before evaluation.

---

## Evaluation 1

### E1: Grounding check

An evaluation agent works through the thematic synthesis and verifies that every substantive claim can be traced to a source in the preliminary summaries. Where a claim cannot be traced, the agent flags it explicitly. The critical instruction: flag, do not fix. An agent that silently patches gaps is more dangerous than one that surfaces them. The subject lead then resolves every flagged claim — grounding it in the source material, revising it to reflect what the sources actually support, or removing it.

### E2: Coverage and coherence

Once the grounding check is complete, the subject lead reads the thematic synthesis against the question map and the report specification. Is every sub-question addressed? Does the structure serve the intended audience? Are the limitations of the evidence honestly represented? This is a judgment call that no agent can make reliably. The project does not move to Phase 3 until both evaluation steps are complete.

---

## Phase 3 — Report Writing

### S7: Final report

The thematic synthesis is organised around the research question. The final report is organised around the reader. The move from one to the other — adjusting structure, register, and emphasis for the intended audience — is the first task of this step. The writing agent works from the verified thematic synthesis and the report specification; its instructions should include an explicit directive to flag any point where the evidence feels thin or a claim feels stronger than the source material supports. The human role is editorial in the fullest sense: not just checking for errors but making the judgments about emphasis, framing, and tone that determine whether the report is genuinely useful to its audience.

---

## Evaluation 2

### E3: Final evaluation pass

One complete read of the finished report against all three rubric levels — process quality, content quality, output quality — before it leaves the team. Not to find new problems; the earlier checkpoints should have caught those. The purpose is to verify that the report as a whole is coherent, that the claims in the executive summary are supported by the body, and that the limitations are honestly stated. The question that drives this pass is the same one from Session 3: *could you hand this report to a senior client and defend every claim in it?* If the answer is yes, the report is ready.

---

## Closing — Assembling the Team

The workflow described in this guide requires two human roles and one that is increasingly a specialism in its own right.

The **subject lead** owns the Setup Phase, the curation decisions, all evaluation checkpoints, and the final report. Domain expertise is the qualification — this is the person who knows which sources are authoritative, which claims are well-grounded, and what the client actually needs to hear.

The **AI engineer** builds and maintains the agent instructions files, runs the agentic steps, and adapts the playbooks to new client contexts. This is not a software engineering role — it does not require coding expertise — but it does require fluency with Claude Code, careful attention to instruction design, and the judgment to know when a process needs a full orchestrating agent and when a well-crafted Claude Chat instruction will do.

The agent instructions files developed across a project — search, ranking, summarisation, synthesis, evaluation, writing — are reusable assets. A team that refines them across multiple projects builds something genuinely valuable: a policy research capability that gets better with use, and that can be adapted to new domains and new clients without starting from scratch.

The minimum viable team for a serious policy research project is one subject lead and one AI engineer. On larger projects a coordination role may be needed; on smaller ones, a single person may cover both roles if they have both domain expertise and AI fluency. What the workflow cannot accommodate is the absence of either — domain expertise without AI fluency produces research that doesn't use the tools well; AI fluency without domain expertise produces polished output that can't be defended.

---

*Part of the AI Onramps programme · Building AI literacy for working professionals*
