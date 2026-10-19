---
name: handoff-task
description: Close or pause a repository task by writing a compact versioned handoff for later continuation, including cross-device continuation.
---

# Handoff Task

1. Classify the task as `completed`, `paused` or `blocked`.
2. Review changed hunks, staged state and proportionate evidence. Repeat Git
   inspection only after relevant changes or at a new boundary. Record unneeded
   ordinary-commit and milestone checks as deferred. Do not run a whitespace,
   targeted or full check merely because the handoff changed; rerun only for a
   changed governed input or stated risk.
3. Update authoritative project or decision documents only when authorized
   work made them stale. For maintained-document work, update each affected
   DOCUMENT_CONTEXT.md before replacing the task checkpoint: current open
   questions/dependencies, resolved or superseded items, concrete next
   action and changed assembly/evidence rules. Preserve unrelated document
   state. A completed task may still leave document follow-up work. Missing
   context is a reported gap, not permission for an unrequested migration.
4. Replace `TASK_HANDOFF.md` with the compact task delta: status, outcome,
   decisions, change scope, checks and deferred evidence, preserved unrelated
   state, substantive open points, the smallest useful continuation and the
   versioning boundary. Reference authoritative facts rather than copying them;
   exclude chat history and full tool output. Name affected document IDs and
   link their context paths; keep detailed document follow-ups in those
   contexts rather than competing copies in TASK_HANDOFF.md.
5. Keep a completed handoff commit-stable for its intended scoped commit. Do
   not assert that tracked changes remain uncommitted or unstaged or make
   review, commit or push the next task. State when no task work remains;
   later versioning decisions use live Git state.
6. Record exact working-tree or staging state only when a `paused` or `blocked`
   task depends on preserving it. Label it as observed at handoff creation and
   reconcile with live state on resume.

This skill authorizes no commit, push or broader cleanup. Record separately
authorized, completed Git actions only as historical facts.
