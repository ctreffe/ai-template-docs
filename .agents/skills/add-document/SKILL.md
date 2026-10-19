---
name: add-document
description: Add one maintained document or language-linked document set to an initialized documentation project with explicit document-local scope, catalog metadata and navigation decisions. Use only when explicitly invoked; do not use for project initialization or ordinary edits to an existing document.
---

# Add Document

Confirm that this is an initialized derived documentation project, not a
source-template maintenance checkout or an uninitialized repository. Inspect
Git read-only and preserve existing work and staging.

1. Read `PROJECT_CONTEXT.md`, `DOCUMENTS.md` and only the project, audience,
   profile, Quarto, source-access and validation guidance needed for the new
   document. Treat project-level decisions as defaults, not facts to duplicate.
2. Offer one concise, unnumbered choice between normal lean document setup and
   an optional `grill-me` interview. Reuse an explicit choice already supplied
   for this addition. Keep lean setup as the default; invoke `grill-me` only
   after explicit opt-in. Limit its decision tree and question frontier to
   unanswered document-local choices or deliberate departures from reviewed
   project defaults; do not reopen settled project intent. End the interview
   when those choices are settled and the maintainer confirms shared
   understanding. The maintainer may stop and return to lean setup. Neither
   route selection nor interview answers grant source-access, rendering, Git,
   publication or other action authority. Both routes continue through the
   existing confirmation and collision checks before any edits.
3. Confirm the maintainer-owned title, stable document ID, document folder,
   context path and source paths (normally `docs/<document-slug>/` with one
   `DOCUMENT_CONTEXT.md` shared across chapters and linked language versions);
   purpose, scope and non-goals; dominant type profile; primary audience and
   reader task; language relationship and authoritative language; required and
   permitted output formats; source, access and sensitivity constraints;
   navigation placement; validation and review expectations; initial lifecycle
   status; and next action. Capture known assembly/refresh requirements and
   assigned source/material/report IDs with intended use. Populate the context
   from these confirmed decisions and carry forward unresolved document
   questions, dependencies and the concrete next action from this setup.
   Fill later details
   as work proceeds; do not invent past methods or add a full questionnaire.
   Reuse settled answers and mark an inherited project
   default explicitly. Ask only for unresolved document choices. Stop for any
   missing choice that would change the document's meaning or exposure.
4. Refuse an ID, folder or context/source-path collision. Do not overwrite an existing source,
   reinitialize the project or silently contradict project-wide authority.
   Resolve conflicts with the maintainer before editing.
5. After the decisions are confirmed, create the shared context from
   [the scaffold](../../../templates/DOCUMENT_CONTEXT.md) and add its compact
   index entry to `DOCUMENTS.md`. Keep the detailed contract, next action,
   source assignments and assembly/update method in the context; the catalog
   owns lifecycle status. Reference reviewed project defaults. Create the
   agreed source skeleton or language-linked source set and update
   `_quarto.yml` navigation only when those changes are part of the request.
   Keep the internal context out of rendered pages, includes and publication
   resources. Reuse existing catalog IDs without copying shared sources.
   Update `PROJECT_CONTEXT.md` only when its catalog pointer, documentation
   structure or current-work summary would otherwise be stale.
6. Check index/context agreement, required context completeness for the next
   operation, ID/path uniqueness, language relationships,
   navigation references, links and YAML syntax in the narrowest useful scope.
   Report required render, review and Decision Record follow-up separately.

Do not render, publish, commit, push, inspect unapproved sources or grant
versioning or publication approval. Those actions retain their separate local
workflows and authorization requirements.
