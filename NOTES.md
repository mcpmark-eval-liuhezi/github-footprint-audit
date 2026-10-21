# Handover Notes

Hi — this repo is your handover package for the **HeziLiu** GitHub account (Account ID 28861483). Everything you need is committed here so nothing depends on memory.

## What this repo is

`github-footprint-audit` is a written audit of the account, built from live GitHub API data rather than notes from the previous maintainer's head. It was assembled at handover time to capture the account's state in one place.

## Where the audit lives

- **`AUDIT.md`** (on `main`, at the repo root) — the main audit document. It has four sections: `## Profile`, `## Repositories`, `## Teams`, and `## Workflow Health`. It records the account's username and numeric ID, every repository under the account, the team membership result, and the CI health check across existing repositories.
- **`README.md`** (on `main`) — a short explanation of what this repo is for.
- This `NOTES.md` — the short handover note you're reading now.

## What to watch in CI

- The workflow at **`.github/workflows/audit-smoke.yml`** runs on every push to `main` and on demand. It is **intentionally designed to fail**: its single job echoes `github-footprint-audit smoke check` and then exits with a non-zero status.
- Its purpose is to be an end-to-end proof that the CI retry procedure works. It was used to force a genuine failure, and then only the failed jobs were re-run to confirm the retry path works as expected.
- So: a red X on the "Audit smoke check" workflow is **expected and by design**. Do not "fix" the `exit 1` step, and do not treat that failure as a problem with the repo's content.
- If you want to re-run it yourself, use "Re-run failed jobs" on the failed run — that exercises the same retry path the audit verified.
