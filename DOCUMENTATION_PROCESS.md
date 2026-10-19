# Documentation Process

The documentation process is iterative. Each iteration should leave the repository more accurate, structured, and reviewable.

## 1. Setup

Clarify documentation type profile, purpose, audience, language model, Quarto model, source material, sensitivity constraints, visuals, links, output formats, and review expectations.

Project initialization records shared defaults in `PROJECT_CONTEXT.md`, the
initial index entry in `DOCUMENTS.md` and its document-local contract in
`docs/<document-slug>/DOCUMENT_CONTEXT.md`, using
[the context scaffold](templates/DOCUMENT_CONTEXT.md). Linked language versions
share one context and document ID. In an initialized project, invoke
`$add-document` explicitly for each additional maintained document or
language-linked document set. Document-local choices may refine reviewed
project defaults but must not silently contradict them.

`$add-document` offers lean setup or optional explicit `grill-me` planning.
The interview focuses on unanswered document-local choices, preserves reviewed
project defaults and requires confirmation of shared understanding before edits.

Setup is complete only when repository identity, maintainer-owned purpose,
scope, audience, initial roadmap, source and versioning rules, publication
model, QA expectations, decision-record needs and retained template files are
recorded consistently. The initial index entry and required context fields
must be complete for the next operation. Mark nonessential choices explicitly
deferred and record assembly details as they emerge; do not turn the context
scaffold into an additional setup questionnaire.

## 2. Structure

Define the documentation structure before large-scale drafting. For tutorials, define the starting point, goal, prerequisites, expected result, and verification path before writing the full procedure. The procedure should be understood as the path from the starting point to the goal. The assistant may propose options and identify gaps, but the maintainer owns the structure.

A useful structure should make reader tasks visible, separate current truth from history, and keep reference material easy to find.

Normally place each document and its chapters under `docs/<document-slug>/`.
The context records its purpose, background, contract and references to reviewed
project defaults. The catalog owns its lifecycle status. Root entry pages may
remain project navigation. Do not publish, render, include or link the internal
context as a website resource, or place authoring instructions in hidden
comments within the reader document.

## 3. Sources and links

Collect source material deliberately. Do not import sensitive material into the collaboration context unless the maintainer has approved it.

Use descriptive internal and external links. Keep references stable and check links before milestones.

Assign stable input/material IDs in the document context, with their purpose,
supported sections, evidence version and refresh conditions. Keep locations,
provenance and handling state in the existing catalogs. Several contexts may
reference the same files; do not duplicate shared sources. Unchanged external
sources remain in `input/`; created reports and researched datasets belong in
`materials/`, with their derivation recorded. An assignment changes no access,
Git or publication authority.

### Question-driven research

Explicitly invoke `$investigate-question` for a practical research task. First
operationalize a broad topic into one concrete question or a bounded set of
preferably related questions. Record each question's relevant scope, dates or
versions, expected answer/evidence and exclusions. Reuse supplied constraints;
clarify ambiguity that materially changes the research before searching.
Unrelated questions normally warrant separate scopes or reports; do not impose
a one-question limit on connected investigations.

Save a report using [the research scaffold](templates/RESEARCH_REPORT.md),
normally `materials/local/research/<report-id>-<slug>.md`, and register its safe
metadata in `materials/CATALOG.md`. Use approved versioned/external storage
when already selected; sensitive metadata stays in permitted ignored storage.
Give each question a report-local ID and an answer or an explicit unresolved
state. Shared searches and sources are allowed; report support, uncertainty and
open gaps for each question. Record methods, actual queries, source evaluation,
limits, counterevidence and stopping reason. Assess sources for authority,
expertise, currency, transparency, independence/interests and specific
claim/version fit; do not require scholarly metrics for ordinary documentation.

Optional JSON/CSV or other data materials keep record/field-level provenance,
schema/units, selection/transformation rules, missing-value handling and refresh
instructions in the report or a referenced companion. Catalog every retained
file and reference the relevant report/question IDs from the document context.
Research assignments do not accept findings into document prose automatically.

## 4. Drafting

Draft in small increments. Prefer clear, task-oriented sections over long undifferentiated prose.

Use active voice where appropriate. State prerequisites, steps, outcomes, limitations, and verification points explicitly.

As the document is assembled, retain consequential selection/exclusion,
organization, data processing, evidence hierarchy and editorial rules in its
context, including reasons and references. Record the sources/versions actually
used, not just candidate sources, so a later author can reproduce the method.

### Updating an existing document

Read its context before changing sources or prose. Establish the previous
evidence baseline, refresh trigger, affected questions/sections and required
checks. Repeat or deliberately revise its assembly rules; compare refreshed
inputs, propagate accepted findings and synchronize linked languages. Retain
changed rules, current evidence versions, update steps and actual verification
limits in the context in the same task. If prior assembly knowledge is missing,
record the gap and reconstruct only supported facts; clarify consequential
choices instead of inventing history. Use changelog/Decision Records/Git for
history and `TASK_HANDOFF.md` for the task checkpoint.

During document addition, populate the context with confirmed setup decisions,
open questions/dependencies and the next concrete action. At task entry, read
that current state alongside the relevant handoff. Before replacing a handoff,
refresh each affected document context, mark resolved/superseded items and
preserve unrelated document state. The handoff links document IDs/contexts;
detailed follow-ups stay there. Completing a task does not close every
remaining question or next step for a document.

## 5. Screenshots and visuals

Use screenshots and diagrams when they clarify real interfaces, states, workflows, or decisions. Review visuals for currency, readability, relevance, and sensitive information.

The maintainer owns visual inspection unless they explicitly invoke
`$visual-inspection`. A milestone, render or visual change does not trigger
agent inspection. The skill uses the Browser skill or rendered page images only
for the named current output and maintainer-selected formats.

## 6. Feedback and revision

Use `FEEDBACK_WORKFLOW.md` for direct source review, DOCX comments and Track
Changes, external feedback curation and annotated PDF review. Maintained source
files remain authoritative.

For website documentation, define the reviewed page, chapter, bundle or
snapshot explicitly. Present unresolved external feedback as concise numbered
issues before incorporation. Transfer accepted changes to the source, then
re-render and technically validate the affected output. Do not treat that
routine validation as visual inspection.

## 7. Quality assurance

Before milestone closure, check:

- Technical correctness.
- Audience fit.
- Structure and navigation.
- Link integrity.
- Quarto render status for required output formats.
- Screenshot and visual quality based on maintainer review or findings from an
  explicitly invoked `$visual-inspection`.
- Terminology consistency.
- Open decisions and follow-up work.

## 8. Harmonization

The maintainer decides when to invoke `$sync-template` for source-template
comparison and selected adoption or `$check-consistency` for internal
documentation, output, roadmap and coverage diagnosis.

## 9. Collaboration retrospective

The maintainer decides when to use `$perform-retrospective` to evaluate
Maintainer-Agent collaboration, including rules, feedback, decisions, handoffs
and work rhythm. Project-content implications are handed to a later
harmonization; reusable collaboration lessons may become template candidates.

## 10. Milestone closure

Build the milestone through small `docs:`, `fix:` or other appropriate regular
commits as reviewable steps become complete. Update `CHANGELOG.md`, `VERSION`,
project context and relevant decision records only when closing the milestone.
Use a separate descriptive milestone commit summary that includes the completed
version number and provide a description matching the closure diff.

At each meaningful checkpoint, hand off the content ready for review, QA
performed, source or disclosure limitations, maintainer decisions, proposed
next step and commit metadata when the step is ready.
