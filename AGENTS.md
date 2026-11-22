# AGENTS.md

## Continuity Across Sessions

- Start by reading this file and SESSION_HANDOFF.md, if present. Check the handoff against actual files and execution state; distinguish verified facts from assumptions.
- Reuse or create a handoff only when future work needs context not clear elsewhere. Do not create one just to record a finished edit.
- Maintain a current snapshot, not a session log. At milestones, update sections in place and remove obsolete, resolved, duplicate, or completed items unless their outcome still affects next steps.
- Retain the objective, active constraints, key decisions and rationale, unfinished work, blockers, open questions, next steps, and essential artifact references and verification results.
- Aim for at most 80 concise lines; consolidate before saving without losing active work, unresolved blockers, or essential constraints.
- Keep durable rules in AGENTS.md and progress in the handoff. Link to existing evidence and history instead of duplicating them or listing every file. Archive only for audit or reproducibility, not automatically per session or merely to relocate old text.
- During concurrent work, re-read before saving, distinguish work-item scopes and status, and preserve others' updates and unresolved context.

## File Organization

For analysis and document work, use these defaults. Honor explicit save locations and existing project structure; do not relocate existing files without authorization.

| Location | Contents |
| --- | --- |
| `deliverables/` | Final artifacts intended for the user or recipients to read or use, plus only their required runtime/display dependencies. |
| `data/` | Inputs and reference materials; never overwrite originals. |
| `scripts/` | Entry-point scripts for data acquisition, reproducible analysis, output generation, and maintenance. |
| `src/` | Reusable implementation code called by scripts or applications, such as aggregation, transformation, and decision logic. |
| `tests/` | Automated tests that verify implementation behavior and expected results; keep test outputs in work/. |
| `docs/` | Lasting specifications, decision rationale, and instructions. |
| `work/` | Drafts, intermediate data, verification images, and temporary logs. |

- Classify by purpose, not extension, and write directly to the chosen location. Create directories only when needed; avoid equivalent aliases. Keep the root for project instructions, handoff, configuration, and entry documents rather than working files.
- Small, one-off tasks may keep implementation in scripts/; splitting into src/ and tests/ is not mandatory. Move shared or maintained implementation into src/ as needed. Use tests/ for new projects, while preserving existing project naming conventions.
- Treat deliverables/ as ready to hand over: include a file only if it is an intended final artifact or recipients need it to open, use, or display one. Being useful for generation, verification, or traceability alone does not qualify it as a deliverable.
- Keep intermediate exports, scratch calculations, execution logs, QA reports, and verification screenshots in work/, even after completion. Include these in deliverables/ only when explicitly requested as final outputs. Keep reproducibility scripts in scripts/ and source data in data/.
- For multiple independent work items, use matching work-item subdirectories across relevant locations, never per-session folders.
- Revise deliverables under stable filenames; distinguish recurring outputs by reporting period rather than accumulating revision copies.
- Before completion, open and inspect deliverables and verify supporting references. Check every included file against the handover rule above. Include required runtime/display dependencies with them; usage and display must not depend on work/. Link to deliverables in the final response.
- Retain working files in work/ when needed; placement there does not authorize deletion. Do not bulk-delete files to enforce organization.

## Routine Upkeep

- Before creating files, check for existing scripts, implementation, tests, and documents serving the same purpose. Prefer updating or extending them over creating parallel versions.
- When changing behavior or paths, update affected callers, configuration, and maintained documentation together. Consolidate superseded implementation and instructions within the task's scope, preserving still-needed behavior and references.
- Before completion, review files created or changed for the task and remove only temporary files confirmed to be disposable. Preserve original inputs, user work, and evidence needed for reproduction, verification, or unresolved issues; retain uncertain items.
- Keep routine upkeep limited to the affected work. Do a broader cleanup review of the project at major milestones or when clutter accumulates, rather than auditing the entire project on every task. Do not create extra logs or documents merely to record routine upkeep.
