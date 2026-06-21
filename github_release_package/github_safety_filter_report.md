# GitHub Safety Filter Report

## Result

- confirmed credential files (`.env`, credential-named files): none found by the file-name scan.
- potential unredacted credential-value files: `2`; values are intentionally not printed.
- potential-value review path: `scripts/fetch_api_football_match_odds.py`
- potential-value review path: `scripts/fetch_the_odds_api_match_odds.py`
- sensitive-field reference files: `72`; these are excluded or require manual review.
- cache directories: `scripts/__pycache__`.

## Mandatory Exclusions

- `.env*`, credentials, tokens, cookies, secrets, and API-key material.
- `data/manual_inputs/`, `data/backups/`, raw fetched API payloads, temporary dry runs, and caches.
- prediction logs containing a realized-score field, legacy pending-only evaluations, and non-final review artifacts.
- records whose score source is operator-attested only until independently public source URLs are added.

## Manual Review Queue

- `data/backups/bosnia_formal_merge_20260612/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/backups/czechia_formal_merge_20260611/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/backups/dr_congo_formal_merge_20260612/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/backups/fifa_schedule_reconciliation_formal_merge_20260613/match_market_v03_the_odds_api_filled.csv.bak`
- `data/backups/fifa_schedule_reconciliation_formal_merge_20260613/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/backups/iraq_formal_merge_20260613/match_market_v03_the_odds_api_filled.csv.bak`
- `data/backups/iraq_formal_merge_20260613/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/backups/team_metadata_patch_tunisia_coach_20260614/wc-2026-team-master-enriched-v0.2.before.json`
- `data/backups/uefa_path_b_c_formal_merge_20260613/match_market_v03_the_odds_api_filled.csv.bak`
- `data/backups/uefa_path_b_c_formal_merge_20260613/wc-2026-team-master-enriched-v0.2.json.bak`
- `data/manual_inputs/candidates/match_market_v03_the_odds_api_candidates_20260609.csv`
- `data/manual_inputs/candidates/match_market_v03_the_odds_api_incremental_candidates_20260609.csv`
- `data/manual_inputs/candidates/match_market_v03_the_odds_api_incremental_candidates_20260611.csv`
- `data/manual_inputs/match_market_v03_api_football_odds_filled.csv`
- `data/manual_inputs/match_market_v03_group_stage_skeleton.csv`
- `data/manual_inputs/match_market_v03_group_stage_skeleton_filled.csv`
- `data/manual_inputs/match_market_v03_polymarket_filled.csv`
- `data/manual_inputs/match_market_v03_sample_fill_template.csv`
- `data/manual_inputs/match_market_v03_sample_polymarket_test_filled.csv`
- `data/manual_inputs/match_market_v03_template.csv`
- `data/manual_inputs/match_market_v03_the_odds_api_filled.csv`
- `data/manual_inputs/team_enrichment_v03_batch5_market.csv`
- `data/manual_inputs/team_enrichment_v03_batch8_market.csv`
- `data/manual_inputs/team_enrichment_v03_batch8_market_filled.csv`
- `data/manual_inputs/team_enrichment_v03_market_all.csv`
- `data/manual_inputs/team_enrichment_v03_template.csv`
- `data/manual_inputs/team_resolution/iraq_team_profile_candidate_20260613.json`
- `data/manual_inputs/team_resolution/sweden_team_profile_candidate_20260613.json`
- `data/manual_inputs/team_resolution/turkiye_team_profile_candidate_20260613.json`
- `data/manual_inputs/team_resolution/wc-2026-team-master-iraq-candidate-20260613.json`
- `data/manual_inputs/team_resolution/wc-2026-team-master-uefa-path-b-c-candidate-20260613.json`
- `data/processed/wc-2026-predictions-with-market-the-odds-api-v0.3.json`
- `data/processed/wc-2026-predictions-with-market-v0.3-sample.json`
- `data/processed/wc-2026-predictions-with-market-v0.3.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-bosnia-full-patched.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-czechia-enriched.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-czechia-full-patched.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-czechia-minimal.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-czechia-patched.json`
- `data/processed/wc-2026-team-master-enriched-v0.2-dr-congo-full-patched.json`
- `data/processed/wc-2026-team-master-enriched-v0.2.json`
- `data/reports/api_football_capability_check_20260612.md`
- `data/reports/match-market-v0.3-sample-polymarket-test-fill-report.md`
- `data/reports/match_previews/june14_matchday_package_summary_20260612.md`
- `data/reports/match_previews/june15_matchday_package_summary_20260612.md`
- `data/reports/match_previews/urgent_match_package_summary_canada_bosnia_usa_paraguay_20260612.md`
- `data/reports/polymarket-match-market-fetch-report.md`
- `data/reports/scoreline_model/scoreline_v0.2_readiness_summary_20260613.md`
- `data/reports/scoreline_model/total_goals_odds_check_20260613.md`
- `data/reports/team-enrichment-v0.3-batch5-market-skeleton-report.md`
- `data/reports/team-enrichment-v0.3-batch8-market-filled-report.md`
- `data/reports/team_resolution/czechia_formal_merge_20260611.md`
- `data/reports/team_resolution/czechia_full_formal_candidate_audit_20260611.md`
- `docs/api_football_match_odds_workflow.md`
- `docs/polymarket_match_market_fetch_design.md`
- `docs/prediction_model_v03_market_signal.md`
- `docs/recent_form_workflow.md`
- `docs/the_odds_api_match_odds_workflow.md`
- `docs/wc2026_market_pipeline_runbook.md`
- `scripts/build_bosnia_full_candidate.py`
- `scripts/build_dr_congo_full_candidate.py`
- `scripts/build_github_release_package.py`
- `scripts/build_iraq_full_candidate.py`
- `scripts/build_uefa_path_b_c_candidate.py`
- `scripts/check_api_keys.py`
- `scripts/fetch_api_football_match_odds.py`
- `scripts/fetch_polymarket_match_markets.py`
- `scripts/fetch_recent_form_api_to_csv.py`
- `scripts/fetch_the_odds_api_match_odds.py`
- `scripts/import_match_market_v03.py`
- `scripts/import_team_enrichment_v02.py`
- `scripts/run_market_incremental_update.py`

## Local Path Exposure

Files marked `SANITIZE_THEN_PUBLISH` in the manifest contain local absolute path metadata. Keep probability values and hashes unchanged; remove or replace only those machine-local metadata values in an exported public copy.
