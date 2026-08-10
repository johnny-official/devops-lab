# Rubric — Server Performance Stats

Grading criteria for `proj01-ServerPerformanceStats`. Each item is scored **Pass (P)** or **Fail (F)**. A project is **Complete** only when every required item passes. Bonus items are optional and not required.

## Requirements (must pass)

- [ ] **Runs on any Linux server** — script executes without dependency-specific assumptions.
- [ ] **Total CPU usage** — reported correctly using the `100 - idle` formula.
- [ ] **Total memory usage** — free vs used, including percentage.
- [ ] **Total disk usage** — free vs used, including percentage.
- [ ] **Top 5 processes by CPU usage** — list shown with the required fields.
- [ ] **Top 5 processes by memory usage** — list shown with the required fields.

## Code quality (must pass)

- [ ] **Executable** — shebang present (`#!/bin/bash`) and correct permissions.
- [ ] **No shell errors** — passes `shellcheck server-stats.sh` (no blocking issues).
- [ ] **Portable output** — values are human-readable and clearly labelled.

## Learning / self-review prompts

- Why is CPU usage computed as `100 - idle` instead of read directly?
- What units does `free` report, and why does the script divide by `1024^2`?
- How does the script account for reserved disk space?

## Bonus (optional)

- [ ] Takes optional arguments (e.g. `-v` verbose, `-t` top count).
- [ ] Adds error handling when commands are unavailable.
