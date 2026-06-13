<!-- This file is your project's live position tracker. The YAML block below is authoritative;
     your project mentor reads and updates it automatically. Do NOT hand-edit it — if it ever
     looks wrong or your mentor says it's inconsistent, show this file to your teacher, who can
     set it right. (Dispatch contract §2.1.) -->

```yaml
# --- Position (project-mentor-owned) ---
program_phase: year1-first-time      # year1-first-time | year2-execution | year2-restart | year3-refinement
current_project_id: null             # set when your project begins
current_cycle: null                  # 1, 2, or 3 — null until your first cycle opens
current_regime: planning             # planning | execution | between-cycles | closed
cycle_template_stage: null           # 1–18 within the active cycle — null in the project initiation sequence
spine_complete: false                # the project initiation sequence (discipline → topic → research problem) is done?
seal_status:
  cycle_1: unsealed                  # a cycle seals when its proposal is approved

# --- Reference articles (project-mentor-owned) ---
reference_articles_status:
  research_problem_articles: needed
  method_exemplars_per_cycle: {}
  project_reference_articles_per_cycle: {}
  paper_structure_articles_per_cycle: {}

# --- Paper position (paper-walkthrough-owned) ---
section_state: {}                    # per-cycle, per-section: unwritten | written | stale | sealed
stale_verdict: []                    # sections that must be rewritten before you proceed (shared: mentor populates, paper side clears)

# --- Coordination ---
pending_scaffold: []                 # sections whose thinking is done and that are ready to scaffold-and-write (shared)
last_skill_dispatched: null          # the in-flight-dispatch / resumption signal
last_updated: null                   # ISO 8601 timestamp of the last write
```
