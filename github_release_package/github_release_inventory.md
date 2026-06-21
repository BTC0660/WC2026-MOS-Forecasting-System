# GitHub Release Inventory

## Release Boundary

This inventory prepares a public research package. It does not move source files or alter the frozen MOS v3.7 engine. Public publication is restricted to the manifest status for each item.

## Inventory Summary

- `MANUAL_REVIEW_REQUIRED`: `8` files
- `PUBLIC_READY`: `27` files
- `SANITIZE_THEN_PUBLISH`: `10` files
- v3.7 production state: frozen, sole probability writer.
- HARD monitoring state: 8 accepted samples, rolling-10 provisional at 8/10.

## Core Prediction Outputs

| Source | Proposed public path | Status | Reason |
| --- | --- | --- | --- |
| data/processed/model_calibration/mos_v3_7_predictions_20260618.json | data/predictions/20260618.json | SANITIZE_THEN_PUBLISH | Frozen v3.7 probability output; retain probabilities and remove only local absolute-path metadata. |
| data/reports/model_calibration/mos_v3_7_predictions_20260618.md | reports/daily_predictions/20260618.md | PUBLIC_READY | Human-readable fixed-scope prediction report. |
| data/processed/model_calibration/mos_v3_7_predictions_20260619.json | data/predictions/20260619.json | SANITIZE_THEN_PUBLISH | Frozen v3.7 probability output; retain probabilities and remove only local absolute-path metadata. |
| data/reports/model_calibration/mos_v3_7_predictions_20260619.md | reports/daily_predictions/20260619.md | PUBLIC_READY | Human-readable fixed-scope prediction report. |
| data/processed/model_calibration/mos_v3_7_predictions_20260620.json | data/predictions/20260620.json | SANITIZE_THEN_PUBLISH | Frozen v3.7 probability output; retain probabilities and remove only local absolute-path metadata. |
| data/reports/model_calibration/mos_v3_7_predictions_20260620.md | reports/daily_predictions/20260620.md | PUBLIC_READY | Human-readable fixed-scope prediction report. |
| data/processed/model_calibration/mos_v3_7_predictions_20260621.json | data/predictions/20260621.json | SANITIZE_THEN_PUBLISH | Frozen v3.7 probability output; retain probabilities and remove only local absolute-path metadata. |
| data/reports/model_calibration/mos_v3_7_predictions_20260621.md | reports/daily_predictions/20260621.md | PUBLIC_READY | Human-readable fixed-scope prediction report. |
| data/processed/model_calibration/pending_hard_binding_20260621.json | data/predictions/pending_hard_binding_20260621.json | SANITIZE_THEN_PUBLISH | Immutable pending-binding ledger; publish only after stripping local path metadata. |

## Post-Match and HARD Artifacts

| Source | Status | Reason |
| --- | --- | --- |
| data/processed/model_calibration/20260620_post_match/ground_truth_receipts.json | MANUAL_REVIEW_REQUIRED | Operator-attested source provenance is not independently public-verifiable. |
| data/processed/model_calibration/20260620_post_match/hard_receipts_20260620.json | MANUAL_REVIEW_REQUIRED | Contains operator-attested results and frozen snapshot path metadata. |
| data/processed/model_calibration/20260620_post_match/match_reconciliation_table.json | MANUAL_REVIEW_REQUIRED | Derived from operator-attested results; verify source provenance first. |
| data/reports/model_calibration/20260620_post_match/mos_postmatch_diagnostic_summary_20260620.md | MANUAL_REVIEW_REQUIRED | Narrative depends on operator-attested result inputs. |
| data/processed/model_calibration/20260621_post_match/ground_truth_receipts_completed.json | PUBLIC_READY | Independently sourced ESPN final-result bindings with URLs and source hashes. |
| data/processed/model_calibration/20260621_post_match/hard_receipts_20260621_completed.json | SANITIZE_THEN_PUBLISH | Valid HARD receipts; remove local snapshot paths before release. |
| data/processed/model_calibration/20260621_post_match/match_reconciliation_table_completed.json | PUBLIC_READY | Completed v3.7 reconciliation against independently bound results. |
| data/processed/model_calibration/20260621_post_match/mos_rolling_update_20260621_completed.json | MANUAL_REVIEW_REQUIRED | Rolling snapshot includes 2026-06-20 operator-attested records; verify public source provenance before publishing performance claims. |
| data/reports/model_calibration/20260621_post_match/ground_truth_source_binding_report.md | PUBLIC_READY | Independent source-binding record for the completed review. |
| data/reports/model_calibration/20260621_post_match/match_reconciliation_completed_report.md | PUBLIC_READY | Completed evaluation report using independent ESPN results. |
| data/reports/model_calibration/20260621_post_match/mos_rolling_update_20260621_completed.md | MANUAL_REVIEW_REQUIRED | Rolling snapshot includes 2026-06-20 operator-attested records; verify public source provenance before publishing performance claims. |
| scripts/complete_20260621_hard_post_match_review.py | MANUAL_REVIEW_REQUIRED | Contains temporary local ESPN payload input paths; parameterize before publishing. |
| models/post_match_review.py | PUBLIC_READY | Post-match review support. |

## Governance, Monitoring, and Methodology

| Source | Status | Proposed path |
| --- | --- | --- |
| data/processed/model_calibration/20260621_post_match/mos_rolling_update_20260621_completed.json | MANUAL_REVIEW_REQUIRED | data/rolling_monitoring/rolling_update_20260621.json |
| data/reports/model_calibration/20260621_post_match/mos_rolling_update_20260621_completed.md | MANUAL_REVIEW_REQUIRED | reports/post_match_evaluations/20260621_rolling.md |
| data/processed/model_calibration/ground_truth_gate.json | PUBLIC_READY | governance/ground_truth_gate.json |
| data/processed/model_calibration/mos_execution_mode_controller.json | PUBLIC_READY | governance/execution_mode_controller.json |
| data/reports/model_calibration/mos_layer_governance_policy.md | PUBLIC_READY | governance/layer_governance_policy.md |
| data/processed/model_calibration/mos_correction_flow_lock.json | SANITIZE_THEN_PUBLISH | governance/correction_flow_lock.json |
| data/reports/model_calibration/mos_data_leak_prevention_report.md | PUBLIC_READY | governance/data_leak_prevention_report.md |
| data/reports/model_calibration/mos_discipline_dashboard.md | PUBLIC_READY | governance/discipline_dashboard.md |
| data/processed/model_calibration/mos_rolling_performance_tracker.json | MANUAL_REVIEW_REQUIRED | data/rolling_monitoring/performance_tracker.json |
| data/processed/model_calibration/rolling_system_health.json | PUBLIC_READY | data/rolling_monitoring/system_health.json |
| data/processed/model_calibration/mos_liveness_index.json | PUBLIC_READY | data/rolling_monitoring/liveness_index.json |
| data/processed/model_calibration/hard_sample_ingestion_log.json | SANITIZE_THEN_PUBLISH | data/rolling_monitoring/hard_ingestion_log.json |
| data/reports/model_calibration/rolling10_readiness_status.md | PUBLIC_READY | reports/rolling10_readiness_status.md |
| td_joint_distribution_model.md | PUBLIC_READY | methodology/td_joint_distribution_model.md |
| scoreline_generator.md | SANITIZE_THEN_PUBLISH | methodology/scoreline_generator.md |
| data/processed/model_calibration/mos_v3_7_stabilized_system.json | SANITIZE_THEN_PUBLISH | methodology/mos_v3_7_stabilized_system.json |
| scripts/ground_truth_gate.py | PUBLIC_READY | scripts/governance/ground_truth_gate.py |
| scripts/run_hard_sample_runtime_monitor.py | PUBLIC_READY | scripts/governance/run_hard_sample_runtime_monitor.py |

## Important Public-Release Caveat

Rolling snapshot includes 2026-06-20 operator-attested records; verify public source provenance before publishing performance claims.
