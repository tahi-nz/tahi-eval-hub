# Tahi Eval Hub (published site)

This repository is **only** the static GitHub Pages site for the Tahi evaluation hub.

**Live URL:** https://tahi-nz.github.io/tahi-eval-hub/

Do not put secrets, API keys, or Caitlyn credentials here. Source, workflows, and live execution stay in the private [`tahi-nz/tahi-test-runner`](https://github.com/tahi-nz/tahi-test-runner) repo. A GitHub-hosted Actions job there builds `pages/` and force-pushes the current hub into this repo.

## What is public

The site itself is on the open internet (GitHub Pages on a Free org). Unsigned visitors can see Tier 0–1 results, prompts, and Tahi responses — the same model as the previous `barlconz.github.io` hub.

Assignment, machine-review drafts, verdicts, user admin, and remote-run stay behind hub username + passphrase (Eval Hub Apps Script).

## What is not here

- The pytest runner and rubric import
- GitHub Actions that call Caitlyn
- Apps Script (`Code.gs` lives in `tahi-nz/artifact-consumer-tahi`)
- The Eval Hub Google Sheet and Drive response JSON

## Do not edit this repo by hand

Changes belong in `tahi-test-runner`. The next publish replaces `main` with an orphan commit of the current hub (so this git history does not accumulate every run).
