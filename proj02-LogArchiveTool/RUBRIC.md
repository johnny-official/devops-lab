# Rubric — Log Archive Tool

Grading criteria for `proj02-LogArchiveTool`. Each item is scored **Pass (P)** or **Fail (F)**. A project is **Complete** only when every required item passes.

## Requirements (must pass)

- [ ] **Accepts a log directory** — the tool lets the user specify the log directory.
- [ ] **Compresses logs into `tar.gz`** — creates a valid archive of the selected logs.
- [ ] **Stores archives in a new directory** — uses a dedicated archive folder.
- [ ] **Logs archive date/time** — writes the archive timestamp to a log file.

## Code quality (must pass)

- [ ] **Executable** — shebang present (`#!/bin/bash`) and correct permissions.
- [ ] **No shell errors** — passes `shellcheck logarchive.sh` (no blocking issues).
- [ ] **Handles missing input** — validates that the log directory exists.

## Learning / self-review prompts

- How does `find -mtime` select only logs older than the retention period?
- Why are `-print0` and `--null` used with `tar` (safe handling of spaces/filenames)?
- What happens if `$log_dir` is empty when option 4 is run?

## Bonus (optional)

- [ ] Accepts the log directory as a command-line argument (not only interactive).
- [ ] Cron scheduling is configurable rather than hard-coded.
