# Rubric — Nginx Log Analyser

Grading criteria for `proj03-NginxLogAnalyser`. Each item is scored **Pass (P)** or **Fail (F)**. This project is still **in progress**; once a script is added, grade against the criteria below.

## Requirements (must pass)

- [ ] **Analyses an Nginx access log** — reads a log file passed to the script.
- [ ] **Top 5 IP addresses** — most frequent request origins.
- [ ] **Top 5 requested paths** — most requested URLs.
- [ ] **Top 5 response status codes** — counts of each HTTP status.
- [ ] **Top 5 user agents** — most frequent user agents.

## Code quality (must pass)

- [ ] **Executable** — shebang present (`#!/bin/bash`) and correct permissions.
- [ ] **Accepts file path** — takes the log file as an argument (e.g. `./nginx-log-analyser.sh access.log`).
- [ ] **No shell errors** — passes `shellcheck` on the script (no blocking issues).
- [ ] **Clear output** — results are labelled and sorted.

## Learning / self-review prompts

- How do `awk` / `sort` / `uniq -c` combine to count and rank log fields?
- Which field positions in a standard Nginx log correspond to IP, path, status, and user agent?

## Bonus (optional)

- [ ] Handles missing or empty log files gracefully.
- [ ] Supports a default log path when no argument is given.
