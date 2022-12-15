# Translated metadata for PX4

This repository contains translated metadata for PX4 (parameters, events, ...).

Note that all steps to update are run in CI.

Directories:
- `metadata/`: Synced metadata from PX4.
- `to_translate/`: Extracted strings from metadata to be translated.
- `translated/`: Translated metadata strings.

Update steps:
- CI syncs px4 metadata to `metadata/`
- Execute script:
  `./scripts/prepare_to_ts_all.sh`
- Crowdin (or any other): translate `to_translate/*.ts`
- Push translated files to `translated/`
- Compress and update summary file:
  `./scripts/update_summary.py translated`

