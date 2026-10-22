# Quarto Documentation Format

documentation projects use Quarto Markdown (`.qmd`) as the preferred internal documentation format unless a project-specific reason argues against it.

Quarto is useful for technical documentation because it combines readable Markdown sources with structured metadata, cross-references, executable code support when needed, and multiple output formats such as HTML, PDF, DOCX, RevealJS slides, websites, and books.

## Installation

Install the Quarto CLI before rendering Quarto projects. Use the official Quarto download and setup page:

- <https://quarto.org/docs/get-started/>

After installation, open a new terminal and verify that Quarto is available:

```powershell
quarto --version
```

On Windows, if Quarto is installed but not yet visible in the current terminal session, close and reopen the terminal. If needed, verify the default installation path:

```powershell
& 'C:\Program Files\Quarto\bin\quarto.exe' --version
```

PDF rendering requires a TeX toolchain in addition to the Quarto CLI. HTML rendering works without TeX, but `quarto render --to pdf` will fail until TeX is available. Quarto can install TinyTeX when needed:

```powershell
quarto install tinytex
```

## Standard structure

This template uses a dedicated `docs/` directory for maintained Quarto source files.

```text
_quarto.yml
docs/
  index.qmd
  index.de.qmd
  <document-slug>/
    DOCUMENT_CONTEXT.md
    index.qmd
    index.de.qmd
templates/
  DOCUMENT_CONTEXT.md
  RESEARCH_REPORT.md
materials/
  local/
    research/
  versioned/
styles/
output/
  html/
```

`_quarto.yml` defines project-level rendering and navigation. `docs/` contains
maintained documentation sources. `materials/versioned/` contains maintained
binary documentation material approved for Git, while `styles/` contains
presentation source when needed. Generated formats remain below ignored
`output/` in separate format directories.

`DOCUMENTS.md` indexes each maintained document or language-linked document
set and its shared context. Normally group its chapters and language versions
under `docs/<document-slug>/`; root entry pages can remain project navigation.
`DOCUMENT_CONTEXT.md` records authoring/assembly/update guidance, not reader
content. Add later documents through the explicit `$add-document` workflow so
source paths, language relationships, navigation and required formats remain
consistent with the project configuration.

The default render scope is limited to Quarto source files in `docs/`:

```yaml
project:
  render:
    - /docs/**/*.qmd
    - "!/docs/**/DOCUMENT_CONTEXT.md"
```

This prevents repository governance files such as `README.md`, `COLLABORATION.md`, or `PROJECT_CONTEXT.md` from being rendered as website pages by default.

The leading slash anchors Quarto's pattern to the project root. Without it,
smart glob expansion can also select nested copies such as `temp/example/docs/`.
Retain this anchor when adding document subdirectories; verify the actual render
input list after changing project scope.

Do not add internal contexts, report scaffolds, saved research reports or
unapproved data to navigation, includes, listings or resource bundles. A render
exclusion is not a resource-copying boundary: Quarto can copy files referenced
by published pages ([site resources](https://quarto.org/docs/websites/website-tools.html#site-resources)).
Keep internal references in the context/report rather than linking those files
from reader pages. When adapting render/resource scope, verify actual outputs
for unintended working files. Publish a deliberately prepared reader-facing
summary or approved data export only through the separate publication workflow.

## Executable source readability

When a documentation project uses executable Quarto chunks, write the QMD for
a human source reader. Give every substantive chunk a unique descriptive label,
keep one coherent reviewable purpose per chunk and place explanatory prose
immediately above it. The prose should state why the chunk exists, what it uses
and what result the reader should expect. Split overloaded chunks, but do not
fragment a short coherent operation into trivial pieces.

## Default outputs

HTML is the default practical output for most technical documentation projects and is the default format in this template.

The HTML format uses `embed-resources: true` by default:

```yaml
format:
  html:
    embed-resources: true
```

This embeds images, styles and scripts for static page delivery. It does not
combine a website's pages, search index, downloads or ordinary links into one
file. Deliver the selected page alone only when those site functions are not
required; deliver the complete site when they are. Keep existing output paths.
Larger HTML files and dynamic services or runtime requirements may justify a
deliberate override. Record its reason, required companion files/services and
checks in the document context or project guidance. Embedding grants no new
source access, remote fetching or publication authority.

After changing HTML resource settings, inspect the selected output's image,
script, stylesheet and CSS loading references, including remaining local and
remote dependencies. Check a copy of the HTML away from adjacent asset folders
before describing static delivery as self-contained. For offline claims,
also verify without network access and document any site/runtime exceptions.
Unused generated asset folders alone do not prove a dependency; do not delete
unrelated output. See [Quarto's embedding guidance](https://quarto.org/docs/output-formats/html-basics.html#self-contained).

PDF is supported when a printable or archival output is needed, but it requires a local TeX toolchain such as TinyTeX. Derived projects should enable PDF output in `_quarto.yml` only when PDF rendering is required and the toolchain is available. If PDF is part of milestone QA, verify TinyTeX or another TeX distribution during project setup.

Other Quarto outputs may be used if the project requires them, but they should be documented in `DOCS_SETUP.md` and tested before milestone closure.

Every generated format should use its own ignored directory below `output/`,
for example `output/html/`, `output/pdf/` or `output/docx/`. A format directory
must contain only that output family and may be cleaned independently before a
new render. The template website baseline writes HTML to `output/html/`.

## DOCX and PDF review outputs

DOCX may be generated as a bounded review format for wording, structure,
terminology, comments and Track Changes. It is not the default website output
and must not silently broaden the reviewed scope. A derived project should
define and validate a project-specific render command or profile for the named
page, chapter, selected bundle or snapshot before relying on DOCX review.

PDF is preferred when review depends on layout, pagination, tables, figures,
captions or print behavior. PDF annotations are less reliably mapped back to
editable source structure, so uncertain findings require explicit source
mapping and maintainer confirmation.

In both cases, Quarto files and other maintained repository sources remain
authoritative. Follow `FEEDBACK_WORKFLOW.md` when rendering, receiving,
interpreting and closing feedback files. Store newly generated review outputs
under `output/<format>/`; store returned annotated copies directly under
ignored `review/`.

## Bilingual documentation

The template starts with parallel English and German entry points:

- `docs/index.qmd`
- `docs/index.de.qmd`

The default convention is to maintain German and English as parallel files. The English file uses the base name, for example `index.qmd`; the German file adds `.de`, for example `index.de.qmd`.

A concrete project must decide whether one language is authoritative and how terminology, screenshots, links, and structure are kept aligned. If the project uses a different bilingual structure, document that decision in `PROJECT_CONTEXT.md` and consider recording a DDR.

## Screenshots and binary material

Maintained screenshots, figures and other binary documentation material
approved for Git belong below `materials/versioned/`, using descriptive
subdirectories such as `screenshots/` and `figures/` when useful. Publication
remains a separate decision.

Raw, unreviewed or sensitive captures belong in the classified `input/`
workflow. Retained derivatives remain registered `materials/` in local,
external or versioned storage according to their approved state.

## Rendering

Before a documentation milestone, run Quarto rendering when the toolchain is available:

```powershell
quarto render
```

Verify that each generated format is written below its documented
`output/<format>/` directory and that no files from another output family are
mixed into it.

To render a specific format:

```powershell
quarto render --to html
quarto render --to pdf
```

If PDF output is required, confirm that the local PDF toolchain is available. If rendering cannot be performed, document the reason in the final work summary or milestone notes.

## QA expectations

Quarto output should be checked for:

- Successful render.
- Correct navigation.
- Working internal links and cross-references.
- Correct external links, where feasible.
- Correct rendering of callouts, tables, code blocks, figures, and screenshots.
- No sensitive information in rendered output.
- No unintended disclosure through hover text, embedded resources or file
  metadata.
- Consistency between English and German outputs when both are maintained.

## Project exceptions

A project may choose a different internal format, but that decision should be explicit in `PROJECT_CONTEXT.md` and, if consequential, recorded as a DDR.
