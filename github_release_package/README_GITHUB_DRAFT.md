# WC2026 MOS Forecasting System

WC2026 MOS is a World Cup 2026 probabilistic forecasting and post-match evaluation system. It produces fixed-match probability distributions, locks those pre-match snapshots, and evaluates them only after independently sourced final results are bound through a fail-closed HARD receipt workflow.

## Current System State

- **v3.7** is the frozen production predictor and the only probability-output layer.
- **v3.8-v4.0** are read-only diagnostic, structural, and monitoring layers.
- The ground-truth gate and append-only HARD receipt process are active.
- Rolling monitoring is **8/10 provisional**; it is not a statistically valid calibration window.

## What It Does

- Produces fixed-match v3.7 probability forecasts.
- Stores immutable pre-match hashes and scoreline distributions.
- Binds independently sourced final results through HARD receipts.
- Runs post-match reconciliation and rolling-10 monitoring.
- Preserves diagnostic-only structure analysis outside the prediction path.

## What It Does Not Do

- No live betting automation.
- No automatic retraining.
- No correction-layer overwrite of v3.7 probabilities.
- No evaluation from unverified or inferred match results.

## Methodology Overview

1. A frozen probability engine emits 1X2, BTTS, O/U 2.5, xG, and scoreline distributions.
2. Ground-truth enforcement blocks evaluation when final sourced results are absent.
3. HARD receipts bind an immutable pre-kickoff prediction hash to a final independent result.
4. Evaluation fails closed: rejected or unbound records never enter rolling metrics.

## Key Outputs

- Daily prediction reports and JSON snapshots.
- HARD receipt and source-binding records.
- Match reconciliation tables and rolling updates.
- Governance, integrity, and diagnostic-only system reports.

## Current Performance Snapshot

| Metric | Current rolling HARD snapshot |
| --- | --- |
| HARD_ACCEPTED | 8 |
| rolling-10 state | 8/10 provisional |
| 1X2 accuracy | 62.5% |
| Top-1 scoreline accuracy | 12.5% |
| Top-5 scoreline hit rate | 37.5% |
| BTTS accuracy | 62.5% |
| O/U 2.5 accuracy | 50.0% |
| Tail positive hit rate | 0.0% |

## Important Caveat

The sample is too small for statistically significant conclusions. The first four accepted records are operator-attested and should receive public-source provenance review before external performance claims are made. No calibration or model update is enabled while the rolling window remains provisional.

## License and Disclaimer

This repository is for research and analytical use only. It is not betting advice, financial advice, or a recommendation to wager. Match-result sources and release artifacts must be independently reviewed before publication.
