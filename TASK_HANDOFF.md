# Task handoff

Status: completed (IDEA-0027 document and subproject folders)
Date: 2026-11-08

## Outcome

TVDR-0085 replaces mandatory format folders with shallow document/subproject
folders in REPOSITORY.md and the existing setup, context, feedback, output and
Quarto guides. Companion formats stay together. Both README languages agree.
SYNCHRONIZED_STORAGE.md routes to the local rule. _quarto.yml now uses
output/website for the coherent site tree. Shared renders use --no-clean or
isolated staging, with collision and preservation checks. No source work remains.

## Evidence and limits

Quarto 1.9.38 rendered both public template entry pages in an isolated temp
fixture at output/website. An invented default project rendered HTML, DOCX,
then HTML again with --no-clean in output/handbook. The other format's hash,
same-folder notes and unrelated output remained unchanged. No legacy site path
was produced. Current guidance, bilingual meaning, links and ignore rules pass
focused checks; historical idea/changelog narratives remain unchanged.

The unchanged Cosmo theme could not fetch its Google Fonts resource; this does
not fail destination checks but leaves full offline presentation unqualified.
No PDF render, visual inspection, full-family, whitespace or milestone gate was
needed or run. No skill changed; skill validation is not applicable.

## Continuation and versioning

Existing projects/files were not migrated or cleaned. Prior work and staging
selections remain intact. No Git mutation or publication was performed. Later
versioning uses live state and repository/action-specific authority.
