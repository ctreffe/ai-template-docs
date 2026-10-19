# Document Context

Copy to `docs/<document-slug>/DOCUMENT_CONTEXT.md` during initialization or
document addition. One context covers the whole document, its chapters and
linked language versions. Replace required placeholders with confirmed facts;
mark nonessential choices `Deferred until <trigger>` or `Not applicable`.
Complete assembly details as they become known, before relying on them.
Do not invent historical decisions or turn this file into a task log.

This is internal authoring and update guidance. Do not render, include or link
it as a publication resource. Store only metadata approved for this repository;
refer to ignored catalog/mapping files for sensitive details.

## Identity and document contract

- Document ID and title: TBD
- Catalog entry: `DOCUMENTS.md` -> TBD document ID
- Maintained source paths, chapters and linked language versions: TBD
- Purpose and intended reader outcome: TBD
- In scope / out of scope: TBD
- Dominant documentation type profile: TBD
- Primary audience, reader task and assumed prior knowledge: TBD
- Language relationship, authoritative language and translation checks: TBD
- Required / permitted output formats and navigation placement: TBD
- Source, assistant-access, sensitivity and publication constraints: TBD
- Validation and review expectations: TBD
- Relevant Decision Records: none or TBD

## Background and inherited requirements

Why this document exists, the use or decision it supports, and constraints that
would otherwise be lost between authoring and a later update: TBD

| Requirement | Authoritative reference | Document-specific application or departure |
| --- | --- | --- |
| `<audience/style/format or other default>` | `PROJECT_CONTEXT.md#<section>` or another reviewed rule | `<reviewed inheritance or confirmed local requirement>` |

Reference project defaults precisely; do not copy the entire project context.
Resolve conflicts explicitly. Mark unconfirmed assumptions and their impact.

## Assembly and maintenance rules

Record how this particular document is compiled, not just what it covers.
Use concrete criteria sufficient for another author to repeat the work.

| Aspect | Applied rule and rationale | Evidence, configuration or example |
| --- | --- | --- |
| Coverage and selection | `<inclusion/exclusion criteria, cutoff date, product/version/geographic scope>` | `<source/report ID and locator>` |
| Evidence hierarchy | `<which sources settle which claims; treatment of contradictions>` | `<references>` |
| Organization | `<grouping, ordering, section mapping and completeness criteria>` | `<source sections or maintained configuration>` |
| Data preparation | `<extraction, normalization, deduplication, joins, units, calculations and rounding>` | `<dataset ID/schema; retained script or reproducible steps>` |
| Missing/uncertain data | `<unknown vs absent, estimates and permitted wording>` | `<examples and limits>` |
| Editorial and language rules | `<terminology, naming, translation, visuals and permitted adaptation>` | `<reviewed references>` |

Delete inapplicable example rows and add rules needed for this document.
Retain consequential choices and reasons; chat transcripts are not required.

## Assigned sources, data and research

Paths in this context are relative to the project root unless stated otherwise.
Assignments here are authoritative for this document. Identify sources by
stable IDs from `input/CATALOG.md` or `materials/CATALOG.md`; the catalogs own
location, provenance and access/storage state. Another document may reference
the same IDs. An assignment is not new access or publication approval.

| Catalog and ID | Role in this document / supported sections or claims | Used version, retrieval date or report question IDs | Refresh condition |
| --- | --- | --- | --- |
| `<input/material catalog + ID>` | `<why this source/data/report is used>` | `<baseline; report-ID/Q1, report-ID/Q2 when relevant>` | `<change or date requiring recheck>` |

Use `None yet` when no sources are assigned. Do not move or copy shared files
into the document folder. Distinguish research candidates from accepted evidence
and record which accepted findings informed the document. Use portable links
where safe; otherwise resolve the ID through the catalog and local mapping.

## Reproducing and updating the document

- Last assembled/reviewed baseline and date: TBD or not yet assembled
- Inputs and research/data versions actually used: TBD or not yet used
- Refresh trigger or cadence and responsibility: TBD
- Repeatable update procedure: TBD

Describe how to retrieve permitted current inputs, repeat the selection and
transformation rules, identify changed facts and affected sections, refresh
research/data where necessary, align language versions and validate the result.
Reference maintained scripts/commands/configuration where available; do not
invent commands or imply that documented operational steps were executed.

- Required content, source/data, link, language and format checks: TBD
- What needs maintainer confirmation or fresh access before an update: TBD
- Latest verification actually performed, date and remaining limits: none yet

When an accepted update changes the rules, source baseline or procedure,
update this context in the same task. Keep current instructions here; use Git,
the changelog and Decision Records for history.

## Open questions and next action

- Unresolved assumptions, evidence gaps and their effect: none or TBD
- Dependencies or blocking decisions: none or TBD
- Next concrete document action: TBD

The catalog owns lifecycle status; this context owns document-specific next
steps and assembly/update knowledge. At task entry, reconcile this state with
the current request and applicable handoff; before handoff, update affected
open/resolved/superseded items and next actions. Preserve unrelated document
state. TASK_HANDOFF.md links this context and remains the task checkpoint,
not a competing document backlog. Task completion can leave document work open.
