# Release Notes

## v1.1.24
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.23
GH#745 — declare per-step `output: {name, type}` on every execution step (performance_report/text, audience_insights/text, content_strategy/text, audience_segments/list, visual_spec/text). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.22
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 6 inline shared-content files and declare 6 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.21
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.20
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.19
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.18
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.17
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
