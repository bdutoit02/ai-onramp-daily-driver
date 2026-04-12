# The Policy Research Workflow — Reference Table

## AI Onramps Guide

---

| Step | Description | Human (Subject Lead) | AI Engineer | AI Tools |
|------|-------------|---------------------|-------------|----------|
| **Setup Phase** | | | | |
| S1 | Conceptual planning: the question | Leads discussion, owns question map | — | Claude Chat as thinking partner |
| S2 | Conceptual planning: the report | Leads discussion, owns report spec | — | Claude Chat as thinking partner |
| **Phase 1 — Data Gathering** | | | | |
| S3a | Web search: landscape pass | — | Runs canned tool | Claude Research |
| S3b | Web search: source ranking | Reviews ranked list | Builds and runs ranking agent | Claude Chat / Claude Code: source ranking agent* |
| S3c | Web search: source curation | Owns curation decisions | — | — |
| S3d | Web search: directed extraction | — | Builds and runs search agent | Claude Chat / Claude Code: search agent* |
| S4 | Offline data processing | Owns anonymisation decisions | Builds and runs processing agent | Claude Chat / Claude Code: processing agent* |
| **Phase 2 — Processing** | | | | |
| S5 | Preliminary summaries | Reviews and approves | Builds and runs summarisation agent | Claude Chat / Claude Code: summarisation agent* |
| S6 | Thematic synthesis | Editorial review | Builds and runs synthesis agent | Claude Chat / Claude Code: synthesis agent* |
| **Evaluation 1** | | | | |
| E1 | Grounding check | Resolves all flagged claims | Builds and runs evaluation agent | Claude Chat / Claude Code: evaluation agent* |
| E2 | Coverage and coherence | Owns judgment against question map and report spec | Supports | Claude Chat as thinking partner |
| **Phase 3 — Report Writing** | | | | |
| S7 | Final report | Editorial direction, emphasis, framing | Builds and runs writing agent | Claude Chat / Claude Code: writing agent* |
| **Evaluation 2** | | | | |
| E3 | Final evaluation pass | Owns entirely | Supports | Claude Chat as thinking partner |
| **Closing** | | | | |
| S8 | Team composition | Owns | — | — |

---

*\* All steps marked \* can be run in either Claude Chat or Claude Code. Use Claude Code where the process requires an orchestrating agent managing multiple subagents or complex sequential tasks. For most steps, a well-crafted instruction in Claude Chat or a Claude Project is sufficient and simpler to implement.*

---

*Part of the AI Onramps programme · Building AI literacy for working professionals*
