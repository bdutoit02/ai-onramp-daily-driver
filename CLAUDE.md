# CLAUDE.md — AI Onramps Web App

## What this repo is

A single-page web application delivering course materials for the AI Onramps
programme. It runs entirely in the browser with no build step, no framework,
and no external dependencies.

Live site: https://bdutoit02.github.io/ai-onramp-daily-driver/

GitHub Pages serves the app from the `/docs` folder, main branch.

---

## File structure

/docs
  index.html                — page skeleton, nav sidebar, heading area, script tags
  styles.css                — all appearance: colours, fonts, layout, spacing
  content.js                — all content sections and the headings lookup table
  BankingRegulationApp.html — standalone demo app, linked from nav, not part of
                              the main app structure
CLAUDE.md                   — this file (repo root)
/source                     — canonical md files for major content areas (local only,
                              gitignored, not served by GitHub Pages)

The three core app files are strictly separated by responsibility:
- Never put content or behaviour in styles.css
- Never put styles or content in index.html
- Never put styles or structure in content.js

Do not recreate lec_sections.html — this file was removed. Its content
is in content.js.

---

## How the app works

The app shows one content panel at a time. All panels are defined in
content.js as <section class="step"> elements. The nav sidebar controls
which panel is visible by toggling a visible CSS class. The heading area
updates to match the active panel using a headings lookup object in
content.js.

Critical: every section needs two things in content.js:
1. A <section class="step" id="[id]"> block with the content
2. A matching entry in the headings object: '[id]': { title: '...', subtitle: '...' }

If you add a section without the headings entry, the heading area will break.

---

## Nav architecture

The nav has four top-level collapsible groups:

1. Onramp — conceptual guide + toolkit quickstarts
2. Deep Research Deep Dive — S3 through S7, the methodology arc
3. Appendices — public supplementary material
4. Other Resources — working materials, not for public consumption

Each top-level group is a nav-group-btn. Nested sub-groups use the
nav-sub-btn pattern. Nav groups are defined in index.html.

Nav links follow this pattern:
<a href="#[section-id]">[Link label]</a>

---

## Onramp structure (Group 1)

Two parts:

Part 1: Conceptual Guide
- What AI is and how it works
- The three-layer model (A, B1, B2)

Part 2: Toolkit Quickstarts
Opinionated, minimal, low technical risk. One quickstart per tool:
- Claude Chat
- Claude Projects
- Claude Desktop
- Claude Code
- Orchestrated agentic workflows
- Building web apps with Claude Code
- Claude for Excel

Quickstarts are continuously updated as tools evolve.

---

## Adding and updating content

The preferred workflow for content changes:

- Write new or updated content as a markdown or plain text file
- Give CC the file and instruct it to format and insert it using the
  existing style in content.js as the template
- For new sections, CC must add both the section block and the
  headings entry

To add a new section:
1. Add the <section class="step" id="[id]"> block in content.js
2. Add the matching entry to the headings object in content.js
3. Add the nav link in the correct group in index.html

To update content in an existing section:
Edit the relevant <section> block in content.js only.

---

## Making other changes

To change appearance:
Edit styles.css only. CSS variables at the top of the file control
colours and key dimensions — change those first before editing
individual rules.

To change nav structure:
Edit the nav in index.html. Keep group names and order consistent
with the four-group architecture above.

---

## Working instructions

- Work in small steps. One change at a time, confirm it works before
  the next step.
- Never make structural changes (nav reorganisation, file splits,
  folder moves) without explicitly being asked to.
- Never touch the nav without being explicitly instructed to.
- When adding or editing content, touch only content.js unless
  told otherwise.
- After any change that affects the live site, confirm what was
  changed and what was left untouched.
- If a requested change would affect more than one file, flag it
  before proceeding.

---

## What not to do

- Do not add inline styles to content sections
- Do not add <style> or <script> blocks anywhere outside the
  designated files
- Do not add external library imports without flagging it — the app
  is intentionally dependency-free
- Do not edit files in /source
- Do not recreate lec_sections.html

---

## Local-only folders (gitignored, not on GitHub)

- /source — canonical reference documents, not served by GitHub Pages
- FinanceReports — session working materials

---

## GitHub Pages

Served from /docs, main branch.
To deploy: commit and push to main. No build step required.
Repository: https://github.com/bdutoit02/ai-onramp-daily-driver
