<!-- analysis/ — the home for your analysis and the reasoned record of running it. -->

# analysis/

This folder holds your project's **analysis** — the code that turns your prepared dataset into
findings, the tables/figures/estimates it produces, and the **Data Analysis Log** where the whole
reasoned record is kept. Your **research agent** does the coding here as a tool; **you direct it,
you understand it, and you run the Quality Control (QC) checks yourself.** The analytic decisions,
the plan approval, and the interpretation are yours.

Nothing about your methodology is "locked" at this stage — **only your Hypotheses and/or Expected
Findings are frozen** (at your proposal seal). Your analytic approach is *meant* to evolve as the
data requires; your job is to keep your write-up current with what you actually did.

It is used across two stages of your project, after each stream's data is prepared.

## The seven-step loop
Your analysis runs as the same **seven-step loop** your data stage used — once for your **core**
project (Stage 19) and once for your **extension** (Stage 23):

1. **Plan.** Your research agent writes a plan whose whole purpose is to **teach you** — the analytic
   strategy behind what it's about to do (baseline model, assumption/diagnostic checks, the primary
   specification, robustness checks…), the ordered steps, and the **specific scripts it intends to write
   and run** (named in the plan). It notes anything **you** have to do that it can't.
2. **Teach.** It teaches you the plan and answers your questions until you can say, in your own words,
   what it's about to run and why it fits your methodology.
3. **Review-Agent plan review.** It hands you a full prompt to paste to your **Review Agent**, which reviews
   the *plan* like an expert methodologist and **saves its findings as a dated review file in `reviews/`**.
   You retrieve that file, bring the review back, and your research agent revises and re-teaches as needed.
4. **Approve — together.** You and your **teacher** approve the plan before anything runs: you sign off
   that you understand it, and your teacher signs off on the process.
5. **Execute.** Your research agent **writes and runs the analysis code itself** — that's allowed; using
   AI as a research tool for analysis is permitted, disclosed, and cited. It fits the models and runs the
   checks directly, rather than gating you through every line.
6. **Report.** It writes back what it actually did: the estimates and diagnostics, and **any change to the
   plan** (a specification that changed, a check it added, a step the data required you to amend) — recorded
   honestly. Your analysis is *meant* to evolve; keeping the record current with what you actually did is
   rigorous practice, not deviation from something frozen (only your Hypotheses and/or Expected Findings are
   frozen).
7. **Review-Agent QC audit + your spot-checks.** It hands you a second full prompt for your **Review Agent**,
   which produces a **QC audit** — flagging any unexpected finding and giving you **3–5 spot-checks you run
   yourself** to catch any mistake the agent might have made — and **saves it as a dated audit file in
   `reviews/`**. You retrieve it, run the spot-checks yourself, and tell your research agent what you found
   so it can log it. If a spot-check turns up something that compromises the whole analysis, the loop goes
   all the way back; a smaller fix just gets corrected and re-reported.

## The Data Analysis Log (what you keep here)
Everything from all seven steps — the plan, the teaching, the plan review, the approval, the execution
report, the audit, and your spot-check results — is kept in your **Data Analysis Log**, one per stream:

- `core-data-analysis-log.md` — your **core** project (Stage 19), done first.
- `extension-data-analysis-log.md` — your **extension** (Stage 23), after the core is carried through.

The log is an **ungraded workbench record**, and it **is not your paper.** The messy iterative record stays
here in the log, out of the paper body.

## The Analysis and Execution Paragraph (what you write for the paper)
From the log you write one graded paper paragraph — the **Analysis and Execution Paragraph** (Core at
Stage 19, Extension at Stage 23) — the analysis-stage counterpart to the data stage's Dataset Creation
Paragraph. In it you narrate, in your own words while the work is fresh: the **analytic approach as you
planned it**; **what was actually executed** (the models/estimators actually run); **how the analysis was
amended as the data required**; and the **Quality Control you ran — including the spot-checks you did
yourself to verify the agent's work**. Your research agent hands it off for scaffolding via the same R10
handoff the Dataset Creation Paragraph uses, and it's **teacher-approved like any other paper output**.
(The log's distilled content also feeds the analytic-strategy line in your **Methods Section** and the
robustness/sensitivity lines of your **Results Section**.)

## The analysis artifact (code + outputs)
Alongside the log, this folder holds the **analysis code** (Python / SPSS / Wolfram) your research agent
writes and runs, and its **outputs** — the tables, figures, and estimates it produces. The log is *the
reasoned story of running it*; the code and outputs are *what ran*.

## What's synced vs. local
This README, your **Data Analysis Log**, and your **analysis code** stay in your workspace and sync to Google
Drive — they are the reproducible record your teacher can see (your workspace folder is shared with them) and
your later paper sections draw on. **Large or regenerable outputs** (bulky figure sets, model dumps,
intermediate files) can stay **on your computer only** — the analysis re-runs from the code + the prepared
dataset on each machine. What syncs is the record, not the heavy artifacts. (Keeping bulky outputs out of Drive
sync is a setup detail your teacher configures.)
