# github-footprint-audit

This repository is a written handover audit for the **HeziLiu** GitHub account (Account ID 28861483), prepared as the account transitions to a new maintainer.

It captures, in one place and based on live GitHub API data rather than memory:

- **`AUDIT.md`** — the full account footprint: profile details, every repository under the account, organization team membership, and workflow/CI health across the existing repositories.
- **`.github/workflows/audit-smoke.yml`** — a deliberately failing CI job used as an end-to-end proof that the account's CI retry procedure (re-running only failed jobs) works correctly.
- **`NOTES.md`** (via the `audit-notes` branch) — a short handover note for the incoming maintainer.

Everything an incoming maintainer needs to understand the account's state on day one should be findable here.
