# CLAUDE.md

## Repository Purpose

Administrative scripts and configurations for the personal LAN setup ('HARZNET'). Contains scripts for various systems on the LAN (Synology NAS/DSM, networking). Does NOT contain personal dotfiles — those live in the `dotfiles` repository.

## Known Structure

- `experiments/` — deliberate playground and backup directory, not production code; ignore when reviewing
  - `experiments/superpowers/` — brainstorming specs and implementation plans from Claude sessions (gitignored, local only); check here for prior design decisions before starting new work
- `node_modules/` — exists locally but is gitignored; not committed to the repo

## Tooling

- GitHub Actions SHAs are manually verified and pinned — do not flag pinned SHAs as outdated without checking first
- Renovate: `renovate.json` in `.github/` is the repository-specific Renovate entry point; the `schedule` override there is intentional
- pre-commit hook runs `lint-staged` (Prettier + cspell) on `*.json`, `*.md`, `*.yml`
