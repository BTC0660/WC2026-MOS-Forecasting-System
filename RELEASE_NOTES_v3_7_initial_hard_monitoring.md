# WC2026 MOS v3.7 Frozen Production Release - Initial HARD Monitoring Build

## Included

- Frozen v3.7 probability engine as the sole production prediction layer.
- Ground-truth gate with SOFT/HARD execution controls.
- Append-only HARD receipt validation and source-binding workflow.
- Rolling-10 monitoring, currently 8/10 provisional.
- 2026-06-20 internal HARD evaluation artifacts, marked for source-provenance review.
- 2026-06-21 independently sourced ESPN HARD evaluation artifacts.

## Current Limitations

- The rolling sample is below the 10-match activation threshold.
- Exact scoreline and tail metrics are high-variance at this sample size.
- Public performance claims require provenance review of operator-attested 2026-06-20 results.
- v3.8-v4.0 remain diagnostic-only; they do not alter v3.7 probabilities.

## Next Steps

1. Collect two additional independently sourced HARD samples.
2. Re-evaluate rolling-10 diversity and validity gates.
3. Publish only manifest-approved, sanitized, and source-reviewed artifacts.
4. Keep v3.7 frozen; do not retrain or add probability corrections during this release cycle.
