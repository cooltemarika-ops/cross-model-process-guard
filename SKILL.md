---
name: process-guard
description: Use before editing or auditing multi-file projects with an author, multiple sources, decisions, versioned files, external storage, or AI collaborators. Prevents source confusion, silent canon changes, scope creep, and false claims about saving or publishing.
---

# Process Guard — Cross-model workflow discipline

## Purpose
Follow this skill when a task depends on project files, approved decisions, continuity, version control, multiple AI agents, or a save/publish workflow. It governs process; it does not invent project facts or override the user's instructions.

## 1. Establish the actual source of truth
1. Read the task, current project instructions, and the relevant files that are actually accessible.
2. Record exact paths, version/commit identifiers, and timestamps when available.
3. Identify the authoritative source for each type of information. Do not assume the newest file is authoritative.
4. Treat chat memory and summaries as navigation hints, not evidence. Confirm important claims against a project source.
5. If copies disagree, show the conflict and pause the affected change. Do not pick silently, merge copies blindly, or move/rename files without authorization.
6. A URL is not proof of access. If a private source cannot be read, say so and request an upload or authorized connector.
7. If no decision register exists, you may propose a template, but do not claim it is an official source until the user approves and stores it.

## 2. Separate authorization from approval
- Permission to inspect, audit, or edit a file does not automatically approve a change to project facts or canon.
- Interpret short replies such as “yes”, “okay”, or “good” in the context of the exact question. Do not log every affirmative reply as a durable decision.
- Record a content decision only when the user's intent to establish or change that fact is explicit enough to identify what was decided.
- The user may revise a prior decision at any time. Do not require a magic phrase or explanation. Preserve the history and mark the earlier decision as superseded; do not erase history.
- If intent is materially ambiguous, mark `REQUIRES AUTHOR DECISION` and ask one precise question.

## 3. Apply source authority carefully
Use the project's declared authority rules. A practical default, only when the project has not defined its own hierarchy, is:
1. The user's current explicit decision, including a clear revision of an earlier decision.
2. A project decision register, including status and supersession history.
3. Designated approved source documents / approved current files.
4. Current audit reports and changelog for evidence about workflow, not as automatic authority for lore or policy.
5. Drafts, notes, old exports, and model memory as non-authoritative leads.

Recency is not authority by itself. If two high-authority sources conflict and the user's intent does not resolve it, stop and expose the conflict.

## 4. Define scope before action
At the start of non-trivial work, state briefly:
- desired deliverable;
- files or sections in scope;
- explicit exclusions;
- allowed actions (read, audit, propose, edit, save, publish);
- completion criteria.

An audit is not a rewrite. A targeted edit is not permission for a full rewrite. Building a package is not the same as installing it or publishing it.

## 5. Snapshot before editing
Capture the working baseline: authoritative files, version/commit identifiers, current decisions relevant to the task, known conflicts, and intended file targets. Do not overwrite the sole original. Before consolidation, moving, or merging, identify all candidates by path/version/content and ask if storage structure or original files would change.

## 6. Make the smallest justified change
- Preserve all out-of-scope content and the user's voice.
- Make only changes supported by the task and the established sources.
- Do not invent facts to fill gaps. Label them `REQUIRES AUTHOR DECISION` or `REQUIRES SOURCE`.
- For material edits, record `before → after → reason → source/decision → verification`.
- Keep the decision register for explicit decisions about project content/rules. Keep ordinary edits, formatting, and typo corrections in the changelog; do not pollute the decision register with every edit.

## 7. Track four independent statuses
Never compress these into one 'done' flag.

1. **Work status:** not started / in progress / blocked / waiting for author / under audit / complete.
2. **User approval:** not reviewed / proposed / approved / rejected / superseded.
3. **File/storage status:** not located / source identified / working copy created / edited / diff checked / saved and read back.
4. **Delivery/sync status:** not required / not attempted / pending / confirmed successful / failed / access unavailable.

'Editorially ready' does not mean approved. 'Saved locally' does not mean synced. A Git commit does not prove that another AI can read the repository.

## 8. Verify observable outcomes
After editing:
1. Inspect the actual diff and verify only in-scope files changed.
2. Run relevant checks/tests that are available; state those not run.
3. Read the saved target back, or inspect the resulting commit/file through the destination tool.
4. Confirm publication/synchronization separately from local save.
5. Never report 'saved', 'uploaded', 'pushed', 'shared', 'tested', or 'verified' without a returned/observed confirmation. A command being issued is not proof of success.

## 9. Stop conditions
Pause and ask the user if the authoritative version cannot be established; sources conflict; the change would establish an unstated fact/rule; the task would exceed scope; an action could destroy/replace original data; or a required external system is inaccessible. Continue with unaffected read-only analysis when useful.

## 10. Completion report
Report concisely:
- sources actually read;
- files changed and deliberately left unchanged;
- checks performed and not performed;
- the four independent statuses;
- unresolved decisions/blockers;
- the next action needed from the user, if any.

Do not claim a tool, agent, or external service has completed work unless its result confirms it.

## Minimal decision record
Use `templates/decisions-register.md`. Include: ID, decision text, evidence of author intent, date, status (active/superseded/open), supersedes/superseded-by, and affected source/path. If the author changes a decision, append the revision instead of silently rewriting history.