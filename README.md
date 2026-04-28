# sportzstatz.github.io — Legacy generated mirror

> **Status (2026-04-28):** Legacy. **Not** the canonical BoardWise frontend.

This GitHub Pages repo is a **legacy generated static mirror** of an
older sports-prediction surface. It is still being updated by an
automated job on 7050 (most recent push: `Update shared morning board
…`), but it is no longer the product surface BoardWise users are
directed to.

## Canonical BoardWise surface

| Layer | Where | Repo |
|---|---|---|
| Public site | <https://useboardwise.com> | [`sportzstatz/boardwise-frontend`](https://github.com/sportzstatz/boardwise-frontend) (Cloudflare Pages) |
| Public API  | <https://api.useboardwise.com> | [`sportzstatz/boardwise-api`](https://github.com/sportzstatz/boardwise-api) (Cloudflare Tunnel → 7060) |

For the full architecture and the role of every BoardWise repo, see
[`sportzstatz/boardwise-ops`](https://github.com/sportzstatz/boardwise-ops):

- `docs/final-architecture.md`
- `inventory/repo-source-map.md`

## Disposition

- **Do not** treat this repo as the source of truth for BoardWise UI
  or data. Anything published here lags behind, may use a different
  data path, and is not part of the BoardWise serving contract.
- **Do not** add new product features to this repo.
- The repo is intentionally **not archived yet**: the daily generator
  still pushes to it and disabling that path is out of scope for this
  README. Archival is a follow-up operator decision tracked in
  `boardwise-ops` `roadmap/open-technical-debt.md`.
- Generated files in this repo (`index.html`, `data.json`,
  `mlb/`, `ncaamb/`, `nhl/`) are overwritten by the publisher on each
  run. Do not hand-edit them; edits will be lost.

## How to re-route or retire

When the operator decides to retire this mirror:

1. Stop the publisher job on 7050 that pushes to this repo.
2. Replace `index.html` with a minimal redirect page pointing to
   `https://useboardwise.com` (or archive the repo and disable
   GitHub Pages on it).
3. Update `boardwise-ops/docs/final-architecture.md` and
   `inventory/repo-source-map.md` to reflect the retirement.

## Pointer for AI coding agents

If you are an AI agent reading this: this repo is **legacy**. The
canonical BoardWise frontend repo is `sportzstatz/boardwise-frontend`
and the canonical API repo is `sportzstatz/boardwise-api`. Do not
push product changes here.
