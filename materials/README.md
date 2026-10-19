# Project Materials

Synchronized external materials use provider-neutral `sync:` roots and storage
`external`; see [SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md).

`materials/` contains retained, assistant-readable working files created by the
documentation project or derived by changing content from external files under
`input/`. Git versioning and publication remain separate decisions.

Files under `input/` remain content-unchanged. Cropping, annotation, redaction,
OCR, conversion, optimization, combination or any other content change creates
a new material. Preserve the original input and record its ID under `Based on`
in `CATALOG.md`.

The catalog records three storage states:

- `local`: stored under `materials/local/` and ignored by Git;
- `versioned`: stored under `materials/versioned/` and approved for Git;
- `external`: stored outside the repository and represented by a stable
  logical location in the catalog.

Copy `PATHS.local.example.md` to the ignored `PATHS.local.md` for
device-specific paths. Never version credentials, private share tokens or
absolute local paths.

Examples include cropped screenshots, OCR extracts, converted reference
documents, retained review preparations, research reports and researched
JSON/CSV data. Research follows the storage and reuse rule below. Use
[the report scaffold](../templates/RESEARCH_REPORT.md) to preserve question-level
findings, provenance and refresh rules. Document contexts assign catalog IDs to
one or more documents without copying shared files. Retained research remains
working evidence rather than automatically accepted document text.

Move accepted textual content to
`docs/`; keep reviewed binary documentation material in `materials/versioned/`
after Git approval and preserve its provenance. Presentation source belongs in
`styles/`. Generated review copies and finished publication outputs belong in
the applicable format directory below `output/`; returned annotated review
files remain separate under `review/`.

## Question research

Retain question research reports and optional datasets as separately cataloged
materials, under the storage rule below. Use the
[report scaffold](../templates/RESEARCH_REPORT.md) for concrete questions,
individual source assessments with evidence/reasons/dates, methods and limits.
Keep prior report/source references when later assessments change. New data
retain schema and record/field provenance; publication remains separate.

## Research storage and reuse

New research reports and generated data sources stay outside Git by default.
Prefer `sync:<project-id>/materials/research/` only when that project's mapping,
identity and approved write/provider scope already cover these materials and
the destination is locally available. Use the selected project's existing
catalog and ignored mapping; do not discover cloud folders or set up storage
implicitly. This use of an approved mapping does not invoke a setup skill.

Otherwise save under ignored `materials/local/research/` and catalog the actual
local location and any availability limitation. A missing, mismatched,
placeholder or unsupported external destination is not permission to hydrate,
move or transmit. If an externally stored artifact is required for the task,
report the gap rather than silently claiming successful external delivery.
Do not move earlier artifacts automatically. Separate file-specific approval
is needed to version research content; a cloud location is not Git or publication
approval. Keep reports and generated datasets separately cataloged with stable
IDs, provenance and references to prior assessments.

Before later reuse, resolve the required artifact's ID and location, verify the
relevant availability and access, and reuse still-current evidence from this
task. Record a missing report as an evidence gap; never invent its contents or
assessment. Check only needed artifacts, not every catalog or project. Use
[SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md) when setup or a mapping
problem actually needs attention.
