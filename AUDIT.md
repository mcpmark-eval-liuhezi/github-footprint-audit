# Account Audit — HeziLiu

This document is a written audit of the **HeziLiu** GitHub account, generated from live GitHub API responses at the time of handover. It exists so that the state of the account is captured on paper rather than living in one person's head.

## Profile

- **Username:** `HeziLiu`
- **Numeric user id:** `28861483`
- **Profile URL:** https://github.com/HeziLiu
- **Name:** Hezi Liu
- **Company:** BUPT/GZU
- **Location:** Beijing/Guiyang
- **Bio:** "treat me like a tree"
- **Public repositories:** 4
- **Account created:** 2017-05-22

## Repositories

Repositories found under the account (as returned by search, with forks included):

1. `Little-rookie` — Undergraduate coursework (Java) — https://github.com/HeziLiu/Little-rookie
2. `Big-Buzzard` — For future.... — https://github.com/HeziLiu/Big-Buzzard
3. `CodingInterviewChinese2` — 《剑指Offer》第二版源代码 (C++) — fork — https://github.com/HeziLiu/CodingInterviewChinese2
4. `awesome-chatgpt-prompts-zh` — ChatGPT 中文调教指南 (fork) — https://github.com/HeziLiu/awesome-chatgpt-prompts-zh

## Teams

**None** — no organization team membership was found for this account. The token used for this audit resolves to the organization `mcpmark-eval-liuhezi`, but that organization reports **zero teams** that the account belongs to, and no member lists could therefore be recorded.

## Workflow Health

Checked workflow runs in every repository found under the account (`Little-rookie`, `Big-Buzzard`, `CodingInterviewChinese2`, `awesome-chatgpt-prompts-zh`):

- **All four repositories report zero workflows.** Because no workflows exist, no workflow runs — and therefore no failed runs — exist in any of the account's pre-existing repositories. Nothing was re-run and there is nothing to re-run.

As the CI retry-proof smoke check required for handover, this repository contains `.github/workflows/audit-smoke.yml`. That workflow runs on pushes to the default branch (`main`) and on demand (`workflow_dispatch`) and performs a single job with a single step that echoes `github-footprint-audit smoke check` and then exits non-zero — a **genuine failure, not a simulated one**. The intent is to force a real failing run, then re-run **only its failed jobs** to demonstrate end to end that the CI retry procedure works. The results of that smoke check and its retry are recorded in this repository's pull request comments.
