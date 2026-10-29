# Release Notes

## v1.1.27
GH#1100 retrospective repair — two bindings that resolved and served while feeding the wrong artefact.

`generate-visual-spec`'s slot is labelled **"Analysis Results"** and was bound to Audience Segmentation, so the visualisation spec was derived from audience segments rather than from any analysis. Re-bound to Engagement Analysis, whose performance report is the analysis result.

`segment-audience`'s slot is labelled **"Product or Campaign"** and was bound to Content Performance Modeling — a content strategy, not a product. Nothing in this flow produces a product description, so this is `from_step` where `from_input` was needed: a new required `product_or_campaign` input now carries it.

**This flow now requires an input it did not require before.** Previously the user supplied nothing and the segmentation silently ran against a content strategy rather than a product. The new input makes the requirement visible instead of guessing at it.

## v1.1.26
GH#1045 — run the platform comparison and hashtag strategy stages this pipeline documents. `platform-comparison-prompt` (Stage 4) and `hashtag-strategy-prompt` (Stage 5) both shipped declared and uninvoked, so the flow produced neither the cross-platform resource recommendation nor the hashtag strategy its own Outputs table promises.

Added `platform-comparison` and `hashtag-strategy` backing skills — Stage 4's prose names no skill and Stage 5's prompt would otherwise have had to share a slug, and two entries on one skill share a title so one is silently dropped.

Two more labels that read the wrong source, neither flagged by any rule because the references resolved. `platform-comparison-prompt` asked for "Platform Performance Data" via `{{steps.previous.output}}`, which is whatever happens to precede it rather than the performance report; it is now bound to Engagement Analysis, which its label names. `hashtag-strategy-prompt` asked for "Content Pillars: based on the content performance model" while reading `{{steps.Engagement Analysis.output}}` — Stage 1's output, not the content model — and used the same reference again for hashtag performance. Each is now a declared slot bound to the stage its own label names. Skills 3→5, total 12→14.

## v1.1.25
GH#1100 consumer wave (batch 2) — declare the data flow this workflow was resolving positionally.

Each stage below now receives its input through a declared `bindings:` entry instead of `default_from_previous`, which K-073 revoked. **The value is unchanged**: every binding names the step that immediately precedes it, which is exactly what the positional default resolved to. What changes is that the dependency is stated rather than inferred from position, so a reorder can no longer silently feed a stage the wrong artefact.

Bindings added:
  `segment-audience` ← `from_step: "Content Performance Modeling"` (step 4)
  `generate-visual-spec` ← `from_step: "Audience Segmentation"` (step 5)

Dependency pins moved to the published versions that declare these slots:
  `audience-segmentation` 1.0.1 → 1.0.2
  `campaign-performance-benchmarks` 1.0.1 → 1.0.2
  `generate-visual-spec` 1.0.3 → 1.0.4
  `segment-audience` 1.0.5 → 1.0.6
  `visual-spec-generation` 1.0.1 → 1.0.2

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
