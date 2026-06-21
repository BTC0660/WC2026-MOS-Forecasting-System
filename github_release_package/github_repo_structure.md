# Proposed GitHub Repository Structure

```text
WC2026-MOS/
  README.md
  LICENSE
  docs/
    source_policy.md
  methodology/
    frozen_v3_7.md
    td_joint_distribution_model.md
  governance/
    ground_truth_gate.json
    execution_mode_controller.json
    layer_governance_policy.md
  calibration/
    rolling10_readiness_status.md
    system_health.json
  post_match_reviews/
    20260621_sources.md
    20260621_reconciliation.md
  data/
    predictions/
    post_match/
    hard_receipts/
    rolling_monitoring/
  scripts/
    inference/
    evaluation/
    governance/
  reports/
    daily_predictions/
    post_match_evaluations/
    system_audits/
```

## Operating Boundary

- `v3.7` remains the sole production probability writer.
- `v3.8`-`v4.0` are diagnostic-only and must not feed probabilities.
- Raw inputs, source payloads, API integration scripts, credentials, caches, backups, and unverified-result artifacts remain outside the public package.
