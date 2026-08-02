<!-- data/ — the home for your project's dataset and the reasoned record of building it. -->

# data/

This folder holds your project's **data** — the real dataset your analysis runs on, and the
work that builds it. Your **research agent** does the coding here as a tool; **you direct it,
you understand it, and you run the Quality Control (QC) checks yourself.** The agent writes and runs
the scripts; the decisions, the plan approval, and the quality checks are yours.

Nothing about your methodology is "locked" at this stage — **only your Hypotheses and/or Expected
Findings are frozen** (at your proposal seal). How you source and prepare the data is *meant* to
evolve as the work requires; your job is to keep your write-up current with what you actually did.

It is used across two stages of your project.

## Planning (Stage 5)

**First (Stage 5.3 — `check-data-policy`): how may the agents work with this data?**
Before any agent touches a candidate dataset, you and your research agent read the source's terms and set the
**data-interaction mode** — recorded in your Data Validity Log and in `project_paper_status.md`:

- **CLEAR** — the agent may work with the data directly, rows and all. *This is the normal case.*
- **ROW-RULE** — the agent reads the codebook, writes your analysis code, and runs it on your machine, but
  **never receives an individual person's record.** Four sources need this: Add Health, HRS, anything through
  ICPSR, and the UK Data Service.
- **NO-AGENT** — data you collected yourself from people under IRB; it stays on your machine.

**Then (`operationalize-construct`):** your research agent helps you **operationalize your constructs** — decide
exactly how each idea in your research question gets measured — and **validate a candidate dataset** against that
plan by reading its codebook. To let you explore what's possible, it may stage here:

- `codebook/` — the data dictionary / codebook for a candidate dataset. *(Always allowed — reading the codebook
  is permitted in every mode.)*
- `sample/` — a small real extract, where one is openly available. *(Under **ROW-RULE**, a real sample is rows,
  so it is not staged; a toy/synthetic set is used instead.)*
- `toy/` — a **clearly-labeled toy or synthetic dataset**, shaped like the real one, for trying out
  candidate operationalizations.

> **Integrity rule:** a toy/synthetic dataset is for *exploring operationalizations only*. It is always
> labeled as synthetic, is **never analyzed for findings**, and is **never** a stand-in for the real
> data. Findings only ever come from the real dataset acquired in execution.

Once your operationalization is validated, your research agent writes your **Data Validity Log**
(`data-validity-log.md`) here — the record of how each construct is measured and why the dataset you chose is a
valid way to measure it. It also carries the **data-policy determination**: which source, which door you came
through, what its terms say (quoted), and the mode that follows. Like your other logs, it is an ungraded working
record — but this part becomes a sentence in your Methods, and you write it up in your weekly journal in your own
words.

## Execution (Stages 18 & 22 — `source-and-prepare-data`)
After your proposal is approved, your research agent acquires, cleans, and quality-checks the real
dataset. This runs **twice** — once for your **core** project (Stage 18) and again for your
**extension** (Stage 22), since you carry the core all the way through first and then the extension.

Each time, the work runs as a **seven-step loop** you drive:

1. **Plan.** Your research agent writes a plan whose whole purpose is to **teach you** — the ideas
   behind sourcing and cleaning this dataset, the ordered steps it will take, and the **specific
   scripts it intends to write and run** (named in the plan). It also spells out anything **you** have
   to do that it can't — for example, requesting **ICPSR or other credentialed access**, or signing a
   data-use agreement — written as clear steps for you.
2. **Teach.** It teaches you the plan and answers your questions until you can say, in your own words,
   what it's about to do and why.
3. **Review-Agent plan review.** It hands you a full prompt to paste to your **Review Agent**, which reviews
   the *plan* like an expert methodologist and **saves its findings as a dated review file in `reviews/`**.
   You retrieve that file, bring the review back, and your research agent revises and re-teaches as needed.
4. **Approve — together.** You and your **teacher** approve the plan before anything runs: you sign off
   that you understand it, and your teacher signs off on the process. This is a checkpoint on the *plan*,
   separate from grading your writing later.
5. **Execute.** Your research agent **writes and runs the code itself** to acquire, clean, and derive the
   dataset — that's allowed; using AI as a research tool for data and analysis is permitted, disclosed,
   and cited. You do any steps the plan assigned to you (the access request, for instance). **Under
   ROW-RULE the agent still writes and runs all the code — on your machine, against every row — but the
   code's *output* (counts, distributions, model results) is what comes back to it, never the records
   themselves. When it needs eyes on the raw rows, it tells you exactly what to look for, and you look.**
6. **Report.** It writes back what it actually did: the results and checks, and **any change to the plan**
   (a script that changed, a step it added, a step the work required you to amend) — recorded honestly. How
   you prepare the data is *meant* to evolve; keeping the record current with what you actually did is
   rigorous practice, not deviation from something frozen (only your Hypotheses and/or Expected Findings are
   frozen).
7. **Review-Agent QC audit + your spot-checks.** It hands you a second full prompt for your **Review Agent**,
   which produces a **QC audit** — flagging anything unexpected and giving you **3–5 spot-checks you run
   yourself** to catch any mistake the agent might have made — and **saves it as a dated audit file in
   `reviews/`**. You retrieve it, run the spot-checks yourself, and tell your research agent what you found
   so it can log it. If a spot-check turns up something that breaks the whole dataset, the loop goes all the
   way back; a smaller fix just gets corrected and re-reported.

Everything from all seven steps — the plan, the teaching, the plan review, the approval, the execution
report, the audit, your spot-check results — is kept in your **Dataset Creation Log**, one per stream:

- `core-dataset-creation-log.md` — your **core** project (Stage 18), done first.
- `extension-dataset-creation-log.md` — your **extension** (Stage 22), after the core is carried through.

The log is an **ungraded workbench record** — it's not your paper. From it you write one short **Dataset
Creation Paragraph** for your paper (the graded output), in your own words while the work is fresh: where
the data came from, the sample and how it was drawn, the key cleaning steps, how the plan was **amended as
the work required**, and the **Quality Control you ran — including the spot-checks you did yourself to
verify the agent's work**. (This is the data-stage counterpart to the analysis stage's Analysis and
Execution Paragraph.)

The folder also holds the working files — with one important placement rule:

- `raw/` — the raw source file(s) as downloaded. **These do NOT live inside your synced workspace.** Your
  research agent stages them in a **local-only folder outside the Drive-mirrored workspace** (for example
  `~/research-data-local/<your-workspace>/raw/` on macOS), because (1) raw microdata is often large and would
  churn your Drive sync and quota, and (2) many data-use terms don't allow it to leave your machine. The `raw/`
  entry you see here is a **pointer** (a `.gitkeep` + this note); the actual bytes stay off-cloud.
- the **cleaned, analysis-ready dataset** — also kept in that same **local-only off-mirror folder** by default
  (it's regenerable from `raw/` + your cleaning script, so it doesn't need to travel). If your data-use terms
  explicitly allow sharing a cleaned extract, you *may* keep that one file in the synced `data/` folder — but
  local-only is the default.

## What's synced vs. local — and *how* the split works
Your workspace folder is synced by Google Drive (Mirror mode) and shared with your teacher, so **everything
inside it is visible to them.** That's exactly why the heavy, restricted data is kept *outside* it.

- **Synced (in the workspace):** this README, your **Dataset Creation Log**, and your cleaning script — the
  reproducible **record** your teacher can see and your **Dataset Creation Paragraph** draws on.
- **Local-only (outside the mirrored folder):** the raw microdata and the cleaned analysis-ready file. Your
  research agent re-acquires the raw source and re-runs the cleaning on each machine you use, so the data is
  always reproducible without ever syncing.

**Why "outside the folder" and not "excluded inside it":** Google Drive for Desktop mirrors a folder *whole* —
it can't sync a folder while skipping one subfolder inside it. So the only reliable way to keep raw data
off-cloud is to place it in a **separate local path that isn't inside the mirrored workspace at all.** Your
research agent handles this placement automatically; you don't configure anything.

