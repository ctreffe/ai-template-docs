# Document Catalog

This catalog is the compact index of maintained documents in a derived
documentation project. Project-wide defaults remain in `PROJECT_CONTEXT.md`.
Each document or language-linked set has one `DOCUMENT_CONTEXT.md` containing
its confirmed local contract, source assignments and assembly/update procedure.
Use [the context scaffold](templates/DOCUMENT_CONTEXT.md).

`$start-project` creates the initial entry and context. Invoke `$add-document` explicitly
for each later document or language-linked document set. A catalog entry does
not by itself authorize access to source material, Git versioning, rendering or
publication.

The workflow offers lean setup or an explicitly selected `grill-me` interview.
Either path confirms only unresolved document-local choices and identifies
reviewed inherited defaults; route selection does not authorize catalog edits.

## Lifecycle

Use the maintainer-approved project lifecycle, normally `planned`, `draft`,
`review`, `stable` or `archived`. Record the current state here; history belongs
in the changelog or an applicable Decision Record.

## Document folders and entry contract

Normally keep each document's sources, chapters and shared context in
`docs/<document-slug>/`. Linked language versions share the folder, ID and
context. Root `docs/index*.qmd` may remain project navigation pages; a maintained
document at another agreed path still needs its own context pointer. Internal
contexts must not be rendered or included as publication resources.

Copy this entry once per maintained document or language-linked set. Replace
required `TBD`s and verify ID/path uniqueness. Put detailed decisions and next
actions in the context, not a second copy here. Mark inherited project defaults
as reviewed references there; catalog status is authoritative here.

### DOC-0001: TBD title

- Document ID: `DOC-0001`
- Context path: `docs/<document-slug>/DOCUMENT_CONTEXT.md`
- Maintained source path or language-linked paths: TBD
- Lifecycle status: TBD
