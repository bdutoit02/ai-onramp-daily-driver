# Session 3: Deep Research in the Wild — What Canned Tools Can Do

## Student Notes

---

## 1. The Skilled User Frame

As AI tools become more capable, the gap between casual users and skilled users widens. Skilled users are not necessarily more technical — they are more deliberate. They think clearly about three things:

**Input** — the material you bring to the conversation: documents, data, files, screenshots. The raw substance the model works with.

**Direction** — everything you say to the model: the question, the context, the instructions, the constraints, the format, the iteration. Direction is how you guide the model toward useful work.

**Evaluation** — how you assess what comes back. Not "does this look good?" but structured, criteria-driven judgment applied consistently.

This session focuses on Evaluation. Direction becomes the focus of Session 4. Input becomes the focus of Session 5.

A note on why evaluation matters: AI outputs are increasingly polished and confident in tone. The easier they are to read, the harder it is to spot what is missing, overstated, or wrong. Evaluation is the skill that keeps you in control of the work — and it transfers across every tool you will ever use.

---

## 2. Key Concepts

### Deep Research

Deep Research is a specific product feature — available in Claude, ChatGPT, and Perplexity — not simply a description of researching with AI. It was among the first applications outside of coding to combine three capabilities that had previously operated separately:

- Extended thinking
- Agentic behaviour
- Tool use

When you trigger Deep Research, you are not sending a prompt to a language model and waiting for a response. You are initiating an autonomous research process that can run for several minutes, visit dozens of sources, and make hundreds of decisions before producing its output.

### Extended Thinking / Chain-of-Thought Reasoning

Standard AI responses are generated fluidly, with no visible reasoning step. Extended thinking changes this: the model is given time and compute to plan its approach, break the problem down, and reason through it before producing output. Where visible — as in Claude's thinking indicator or ChatGPT's activity log — you are watching the model work, not just watching it write.

This is inference-time computation: the model doing more work per question rather than simply being a larger model.

### Agentic Behaviour

An agent is a system that pursues a goal by taking a sequence of actions, using tools, and making decisions along the way. Deep Research tools behave agentically: they decide what to search for, choose which sources to read, extract what seems relevant, identify gaps, and search again. They are not following a fixed script — they are planning and replanning in response to what they find.

### Tool Use

Agentic behaviour requires tools. In Deep Research, the primary tool is web search: the model calls the search tool, receives results, decides what to do with them, and calls it again as needed. The search-analyse-replan cycle — visible in ChatGPT's activity log — can repeat dozens of times in a single research run. This is the same architecture that underlies the more powerful agentic systems we will see in Session 6.

---

## 3. The Evaluation Rubric

Evaluation is not a general impression formed after reading. It is a structured assessment applied consistently against explicit criteria. The rubric below organises those criteria into three levels.

You will use this rubric for your homework after this session. You will use it again in Sessions 4 and 5 to evaluate work you have produced yourself.

---

### Process Quality — how did it research?

- *Breadth of sources* — did it draw on a wide range of relevant sources, or rely heavily on a narrow base?
- *Authority of sources* — are the sources credible, current, and appropriate for the question?
- *Geographic and sectoral specificity* — did it find sources directly relevant to the context, or did it generalise from elsewhere?
- *Transparency of reasoning* — can you see what it did, what it chose, and why?

### Content Quality — what did it find?

- *Quality of insight extraction* — did it draw meaningful conclusions from its sources, or summarise superficially?
- *Domain coverage* — did it address the full scope of the question, or leave significant areas thin or absent?
- *Contextual accuracy* — did it handle the specific regulatory, institutional, and market context correctly?
- *Logical coherence* — do the findings hold together as an argument, or sit as disconnected observations?

### Output Quality — what did it produce?

- *Structure and navigability* — is the report organised clearly and easy to use?
- *Specificity of recommendations* — are recommendations actionable, or generic enough to apply to any situation?
- *Caveats and limitations* — does the report acknowledge what it does not know, where data is incomplete, or where claims are uncertain?
- *Fitness for purpose* — could you hand this report to a senior client and defend every claim in it?

---

That last question is the one that matters most for the kind of work this course is built around. A report that looks authoritative but cannot survive scrutiny is not a research output — it is a liability.

---

## 4. The Session Demos

This session demonstrates Deep Research using a single research brief submitted to three tools simultaneously. Watching all three run in parallel — and then evaluating what they produce — is the core of the session.

### The Research Brief

> You are preparing a report for an organisation that provides training resources to banks in South Africa. The report should identify the key skills shortages emerging in the South African banking sector over the next three years, and recommend the training priorities that should shape the organisation's programme development.

Note what this prompt does and does not do. It provides role context and a clear task. It does not specify sources, structure, depth, audience, or format. That absence of Direction is deliberate — we want to see what each tool does with minimal guidance.

---

### The Three Tools

**Claude Research**

Before starting, Claude asks three clarifying questions: scope of the banking sector, target audience for the training, and preferred output format. This is Direction in action — from the model's side. The questions it asks reveal exactly what you should have specified in your prompt.

Claude produces two artefacts: the report itself, and a separate process artefact summarising its research plan and sources. Run time approximately 9 minutes.

**ChatGPT Deep Research**

ChatGPT generates a research plan immediately and begins executing against it. A live progress tracker shows which steps have been completed and which is active. On completion, an activity log is available showing the full reasoning and search cycle across the run — strategic source selection, autonomous workarounds for blocked content, and search-analyse-replan cycles throughout. 353 sources examined, 24 cited. Run time approximately 12 minutes.

The activity log is the richest illustration of extended thinking and agentic behaviour available in this session. Key observations:

- The model plans its approach before searching
- It identifies and pursues primary sources — regulatory instruments, BANKSETA documents, bank job postings
- When pages are blocked or PDFs inaccessible it finds alternatives without stopping
- It monitors its own tool call budget and adjusts strategy accordingly

**Perplexity Deep Research**

Perplexity provides live action descriptions as it runs — searching, extracting insights — but no research plan and no activity log. It is the fastest of the three at approximately 5 minutes. Output includes a report, downloadable artefact, citations, and relevant images located during the search. The most immediately accessible tool and the least process-transparent.

---

### The Evaluation Exercise

Rather than reading three long reports side by side, we use a fourth AI — Claude, in a dedicated Project — to assist with the evaluation. This is itself a demonstration of Direction: Claude is given a specific role, the three reports as documents, and the rubric as its framework.

The evaluation proceeds in sequential steps, each producing an artefact that feeds the next:

1. *Structured summaries* — each report summarised to a common template, making comparison possible
2. *Comparative analysis* — a structured comparison across all five template sections, surfacing similarities, differences, and gaps
3. *Rankings* — the three reports ranked on seven criteria, with one-sentence justifications

**Key findings from the evaluation:**

- All three reports look authoritative on first reading
- One report uses the wrong time horizon without acknowledging it
- The most strategically coherent report makes bold quantitative claims without a single source caveat
- No report adequately acknowledges its own limitations or source bias
- The rankings reveal genuine tensions: the report best suited for senior management presentation ranks last for transparency; the most operationally useful report ranks last for senior management suitability
- No single report is sufficient for the full brief

The critical point: **without systematic evaluation you would not know any of this.** A quick read would not expose these weaknesses. The rubric did.

---

## 5. Homework

Before Session 4, work through the following tasks.

### What You Have

- The comparison document produced in the session — a structured analysis of all three reports across five dimensions
- The rankings document — the three reports ranked on seven criteria with justifications
- Access to the three full reports if you want to refer to them directly

### The Task

Apply the evaluation rubric to one of the three reports in detail. Choose whichever report interests you most.

Work through each of the three rubric levels — process quality, content quality, output quality — and for each criterion make a brief note of your assessment. You do not need to write formally. Bullet points are fine. The goal is to have thought carefully about the report before Session 4, not to produce a polished document.

### The Question to Bring to Session 4

Having completed the evaluation, come prepared to answer this:

*Which of the three reports would you be most comfortable presenting to a senior client — and what would you need to change, add, or verify before you could stand behind it?*

There is no correct answer. The discussion will be more interesting if participants have reached different conclusions.

### A Prompt to Help You

If you want to use AI to assist with your evaluation, here is a starting prompt:

> I am evaluating an AI-generated research report on skills shortages in the South African banking sector. I will paste the report below. Please assess it against the following criteria, working through each one in turn and noting both strengths and weaknesses: breadth and authority of sources, geographic and sectoral specificity, transparency of reasoning, quality of insight extraction, domain coverage, contextual accuracy, logical coherence, specificity of recommendations, caveats and limitations acknowledged, and fitness for purpose. Where you cannot assess a criterion from the report text alone, say so explicitly.

Note the final instruction: *where you cannot assess a criterion from the report text alone, say so explicitly.* That instruction models the intellectual honesty you are looking for in the report itself.

### Looking Ahead

Session 4 opens with a brief discussion of what you found. We will then move directly into building a controlled research process from scratch — one that addresses the weaknesses the evaluation exposed.

The question that will drive Session 4: *what would a research process look like if you were in control of every step?*

---

*Part of the AI Onramps programme · Building AI literacy for working professionals*
