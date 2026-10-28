# Local automation review — 28 October 2026

Selected source scripts inspected read-only in the parent workspace. This is not a complete audit of every file, a security review, or a runtime test. Some temporary directories were inaccessible. No database, mail or infrastructure scripts were executed.

## Evidence used for portfolio additions

- `weekly_pdb_clone_updated.sh`: Bash/SQL*Plus online PDB clone workflow, schedule guard, environment discovery, logging and status emails.
- `weekly_pdb_clone_noarchivelog.sh`: separate clone workflow with source-mode checks, dry-run path and an interruption handler that attempts to restore READ WRITE. Includes destructive target-replacement operations and temporary source downtime; do not publish or run without separate review and authorization.
- `build_user_table_6_updates.mjs`: comparison of baseline/current vulnerability exports and previous remediation records using direct/logical matching keys; severity counts and tracking categories.
- `update_issue_status.mjs`: preserves source columns, adds a status column, marks selected rows as rescan pending and performs formula checks/rendering.
- `update_vulnerability_status_20sep.mjs`: formats and updates historical summary reporting. Some summary values are explicitly supplied, not automatically calculated by this script; do not portray this file alone as a fully automated comparison engine.
- `build_rman_restore_runbook.py`: structured Word-document generation with Python. Other WebLogic document-generation scripts were identified in the inventory, not fully audited.

## Public-content boundaries

The portfolio includes sanitized capability summaries, not these original scripts or their environment-specific values. No unverified time savings, production success rates, security-remediation outcomes or sole-authorship claims were added. Confirm deployment history and measured outcomes before adding such claims.
