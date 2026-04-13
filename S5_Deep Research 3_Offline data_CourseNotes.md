# Claude for Excel — Working with Spreadsheet Data

*Session 5 | AI Onramps*

---

## The Recommended Workflow

For clients working with messy data that needs to be cleaned, anonymised, and turned into useful findings, the recommended workflow combines two tools in sequence.

### Stage 1 — Claude for Excel (/clean-data-xls)

Load the raw file into Claude for Excel and run `/clean-data-xls`. This handles the mechanical work: casing standardisation across all columns, date format normalisation, duplicate detection, missing value flagging, and structured output on a new sheet — with the original preserved untouched. The output is polished, formula-based, and ready for the next stage.

Before you start: duplicate your file and rename the copy. If Autosave is on, changes apply immediately to whatever file is open.

### Stage 2 — Claude Project

Bring the cleaned file into a Claude Project for everything that requires judgment. The Project path catches what `/clean-data-xls` misses — ambiguous duplicates, ID errors, logical inconsistencies — and adds an audit trail. It can also produce descriptive statistics, summary graphics, and narrative findings in the same workspace.

Critically, the Project connects your data to your other work. The cleaned and anonymised dataset can sit alongside your online research, literature review, and report draft in the same Project. The two workstreams — online research from Session 4, offline data from Session 5 — converge here at the reporting stage. This is what a full AI-assisted research workflow looks like in practice.

### Why Two Stages

Claude for Excel thinks in Excel terms — cell formatting, highlights, structured tables. Claude Project thinks in data terms — annotated columns, audit trails, downstream processing. They are not competing tools. Each is optimised for a different part of the job.

### A Note on Anonymisation

Anonymisation belongs in Stage 2. Neither `/audit-xls` nor `/clean-data-xls` raises data privacy unprompted, and anonymisation falls outside the named Skills. The safer path is to handle it explicitly in the Project, where you control the instructions and can review the logic. When done, save the mapping table separately and securely before sharing any output. A non-technical client will not think of this automatically — it needs to be explicitly taught.

---

## Additional Notes

*Practical points for instructors and early adopters.*

- **Claude for Excel is a beta product — expect friction.** Installation can produce misleading error messages before completing successfully. Stick to the suggested setup route and don't let early friction put you off.

- **Claude for Excel: Autosave risk.** If Autosave is enabled in Excel, any changes Claude for Excel applies go immediately back to the original file with no undo trail. Duplicate the file and rename the copy before starting any session.

- **Claude for Excel: Named Skills vs ad hoc requests.** The four named Skills (`/audit-xls`, `/clean-data-xls`, `/dcf-model`, `/comps-analysis`) are tested, constrained workflows — predictable and reliable. Anything outside them, such as asking Claude for Excel to anonymise data, draws on the base model improvising. Capable, but outside the tested envelope and needs checking. This maps onto the three-layer model: Skills are B1; ad hoc requests are B2.

- **Claude for Excel: Audit vs Clean.** `/audit-xls` is diagnostic first — useful when you don't know what you're dealing with. `/clean-data-xls` is purpose-built for fixing — non-destructive, formula-based, superior for raw data cleaning. For a straightforward messy dataset, go straight to Clean.

- **Claude Project: chat with your data.** Unlike Claude for Excel, a Project allows open dialogue with the data — questions, summaries, anomaly investigation, iteration. The analytical depth the named Skills cannot match.

---

*Part of the AI Onramps programme · Building AI literacy for working professionals*
