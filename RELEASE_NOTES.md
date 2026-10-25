# Release Notes

## v1.1.30
GH#1100 consumer wave (batch 3) — declare the data flow this workflow was resolving positionally.

Each stage below now receives its input through a declared `bindings:` entry instead of `default_from_previous`, which K-073 revoked. **The value is unchanged**: every binding names the step that immediately precedes it, which is exactly what the positional default resolved to. What changes is that the dependency is stated rather than inferred from position, so a reorder can no longer silently feed a stage the wrong artefact.

Bindings added:
  `polish-language` ← `from_step: "Status Email Composition"` (step 4)
  `generate-visual-spec` ← `from_step: "Language Polish"` (step 5)
  `check-consistency` ← `from_step: "Visual Spec Generation"` (step 6)

Dependency pins moved to the published versions that declare these slots:
  `check-consistency` 1.0.5 → 1.0.6
  `generate-visual-spec` 1.0.3 → 1.0.4
  `polish-language` 1.0.1 → 1.0.7
  `track-progress` 1.0.3 → 1.0.4
  `visual-spec-generation` 1.0.1 → 1.0.2

## v1.1.29
GH#1045 — the email generation stage now runs. This skrpt is named for producing a status update email, the stage was documented as Stage 4, and nothing invoked it — so the pipeline produced a status update and stopped short of the email it promises.

The stage's prompt shipped with the package from the start and is unchanged. It now runs on the stakeholder update, turning it into a formatted email: a subject line that states what changed, decisions needed placed near the top with their owners and dates, then progress, risks and detail. The email then flows through the existing polish step as before.

## v1.1.28
GH#1044 — document the inputs this workflow's prompts REQUIRE but its Inputs table never listed. A user supplying exactly what the table asked for was running with required parameters unsatisfied — a silent wrong run, not a documentation nicety. documented 2 input(s): project_status, reporting_period. Every row is generated from the requiring prompt's own declared description, example and required flag — none invented. No behaviour change; documentation only.

## v1.1.27
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.26
GH#745 — declare per-step `output: {name, type}` on every execution step (status_data/text, stakeholder_update/text, polished_report/text, visual_spec/text, consistency_verdict/decision). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.25
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 9 inline shared-content files and declare 9 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.24
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.23
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.22
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.21
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.20
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
