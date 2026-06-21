# GitHub Commit Plan

This is a command plan only. It does not initialize, commit, add a remote, or push anything.

## Pre-Commit Review

1. Review `github_public_file_manifest.json` and include only `PUBLIC_READY` files.
2. Create reviewed sanitized export copies for `SANITIZE_THEN_PUBLISH` entries.
3. Do not include `MANUAL_REVIEW_REQUIRED` items until source provenance and privacy review are complete.
4. Keep `data/manual_inputs/`, `data/backups/`, raw API payloads, prediction logs, caches, and credential-related files excluded.

## Suggested Commands

```bash
git init
git status
git add README.md LICENSE methodology governance calibration data/predictions data/post_match data/hard_receipts data/rolling_monitoring scripts/inference scripts/evaluation scripts/governance reports
git commit -m "Initial MOS v3.7 frozen production release"
git remote add origin <YOUR_GITHUB_REPOSITORY_URL>
git push -u origin main
```

Run `git add` only after the selected paths contain the reviewed public export. Do not use `git add .`.

## Recommended Initial Add Set

- README, license, methodology, governance, and source-policy documentation.
- Sanitized frozen prediction exports and their public reports.
- 2026-06-21 ESPN source-binding and reconciliation artifacts.
- HARD gate, receipt-monitor, and evaluation scripts after path/config review.

## Exclude

- `.env*`, credentials, tokens, cookies, API-key material, caches, and `.DS_Store`.
- Raw `data/manual_inputs/`, backup trees, temporary payloads, and prediction logs.
- Pre-binding failed-review duplicates and unverified operator-attested result artifacts.

## Manual Review Required

- All manifest entries marked `SANITIZE_THEN_PUBLISH` or `MANUAL_REVIEW_REQUIRED`.
- Any API integration script or source-policy document that references environment variables.
- Rolling performance files that include 2026-06-20 operator-attested records.
