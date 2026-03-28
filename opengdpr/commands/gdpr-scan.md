---
description: Run OpenGDPR compliance scan on the current project
allowed-tools: Read, Bash, Grep, Glob, Write
argument-hint: [mode: a|b|c]
---

Run the OpenGDPR GDPR compliance scanner on this project.

## Mode Selection

The user may specify a mode as an argument:
- **a** (default) — Code Scan: automated regex-based scan of the codebase
- **b** — Checklist Interview: guided Q&A across 288 compliance checkpoints
- **c** — Full Audit: combines Code Scan + Interview + risk matrix

## Instructions

1. Load the GDPR skill from `skills/gdpr/SKILL.md`
2. If mode is **a** or **c**, first run the deterministic scanner:
   ```bash
   python3 skills/gdpr/scripts/scan_codebase.py . --pretty
   ```
3. Follow the SKILL.md instructions for the selected mode
4. Reference materials are in `skills/gdpr/references/`
5. Severity matrix is in `skills/gdpr/assets/gdpr-severity-matrix.json`
