<!-- reviews/ — the home for your Review Agent's dated reviews of your execution work. -->

# reviews/

This folder holds your **Review Agent's** dated review files. Every time your execution work is
reviewed — at each execution stage, before the work runs and again after — the Review Agent's
findings are **saved here as a dated `.md` file**, so nothing is lost and every review is
memorialized. Over the year this becomes the record of how carefully your data and analysis were
checked.

There are **two kinds of review per execution stage** (your data stages and your analysis stages),
and each one lands here:

- **Plan reviews** — an expert methodological read of your research agent's plan *before* anything
  runs, e.g. `2026-05-14-core-analysis-plan-review.md`.
- **Quality Control (QC) audits** — a check of the report and the executed output *after* the work
  runs, flagging anything unexpected and suggesting spot-checks, e.g.
  `2026-05-21-core-analysis-qc-audit.md`.

## How a review gets here

1. Your **research agent** hands you a **full prompt** to paste to your **Review Agent** — it writes
   the whole thing for you; you just carry it across.
2. Your **Review Agent** does the review and **saves its findings here** as a dated file.
3. Your **research agent** then **retrieves that file** and works its findings back into your plan or
   your log — revising and re-teaching (for a plan review) or resolving what the audit flagged (for a
   QC audit).

## Your part in a QC audit

A QC audit doesn't just come back and get filed. It hands you **3–5 spot-checks you run yourself** —
small, concrete checks that verify the agent's work came out right. **You run them, and you report
back what you found** so your research agent can log it. That's the step that catches a mistake the
agent might have made, and it's yours to do.

If your project is in **ROW-RULE** mode (Add Health, HRS, anything through ICPSR, the UK Data Service),
this split is not optional — it's how the audit works. **Your Review Agent audits the *pipeline*** — the
cleaning code, the exclusion rules, the distributions — and catches the systematic errors that look fine
one row at a time (a reversed scale, a missing-value code read as a real number, a filter that quietly
dropped a third of your sample). **You audit the *rows*** — the Review Agent tells you exactly which ones
and what to look for, and you're the one who opens the file. Neither of you can do the other's half.

## Why these are worth keeping

These reviews, and the spot-checks you ran, aren't just process — they become part of the story you
tell in your **Analysis and Execution Paragraph** and your **Dataset Creation Paragraph**: how the
plan was reviewed, what the QC audit turned up, and what your own checks confirmed. That record of
rigor is exactly what competitions want to see, so keeping every review here — dated and complete —
pays off when you write it up.
