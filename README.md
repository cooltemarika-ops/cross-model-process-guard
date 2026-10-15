# Process Guard 2.0 — cross-model workflow skill

A portable process skill for GPT, Claude, Grok, and other assistants working with project files, decision logs, versioned documents, and connected storage.

## Files
- `SKILL.md` — primary reusable skill instructions.
- `templates/state-snapshot.md` — baseline before work.
- `templates/decisions-register.md` — explicit decisions and revision history.
- `templates/change-log.md` — ordinary edits that are not author decisions.
- `templates/completion-report.md` — completion report and independent statuses.
- `tests/evaluation-scenarios.md` — manual evaluation cases.
- `LICENSE` — MIT.

## Quick start
1. Add `SKILL.md` to the assistant's skill/project knowledge area or paste it into project instructions.
2. Provide the real project sources and the relevant decision register.
3. State which actions are authorized: read, audit, propose, edit, save, or publish.
4. Keep source files, decisions, change history, and delivery status traceable.

## Design principles
- Generic task permission is distinct from explicit author approval of content changes.
- Authors may revise prior decisions; preserve history and mark previous decisions as superseded.
- The source hierarchy belongs to the project; timestamps alone do not determine authority.
- Work status, author approval, storage status, and sync/delivery status are independent.
- Claim a save, push, publication, or test only when there is observable confirmation.

## Access note
The repository is public, but a link to a private project file still requires authorization. This skill does not grant permissions or repository access.

## Testing status
The scenarios are a manual evaluation set; they are not evidence of automated testing. Model behavior must be checked in practice.
