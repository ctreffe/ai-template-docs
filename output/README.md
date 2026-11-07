# Generated Documentation Outputs

Prefer shallow folders named for the document or subproject, keeping companion
formats together, for example `output/handbook/handbook.pdf` and
`output/handbook/handbook.docx`. A single deliverable can live directly here.
The template website uses `output/website/` with its necessary page/resource
tree. Generated content is ignored; this README is the only tracked output file.

Freshly generated files prepared for review remain in the document's output
folder. Rendering must preserve companion formats and unrelated files; see
`QUARTO.md` for `--no-clean` and isolated staging. Cleanup needs separate authority.
Returned files with comments, Track Changes or PDF annotations
belong directly in `review/`. Maintained `docs/`, `materials/versioned/` and
`styles/` content remains authoritative according to its documented role.
