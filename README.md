## Auto-assign PR to commit authors

This repository provides a GitHub Actions workflow that **automatically assigns a pull request to all commit authors** (excluding bots).

Japanese version: `README.ja.md`

## Why this is useful

- **No more “who should own this PR?”**: authors are assigned automatically.
- **Works well for pair/mob PRs**: multiple commit authors can be assigned.
- **Stays up-to-date**: when new commits are added, new authors get added as assignees.

## Behavior

- Adds **missing** commit authors as assignees (keeps existing assignees)
- Skips bots and commits without a linked GitHub user
- Designed to run on `opened` and `synchronize` (new commits on PR)