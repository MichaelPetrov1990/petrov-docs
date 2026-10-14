# Git workflow

## Default branch

- `main` is the default branch.
- Don't commit directly to `main` for issue work. All changes go through a pull request.

## Issue-driven branches and PRs

- Only create branches and PRs for work tied to a GitHub issue.
- Name branches `issue-<number>-<short-kebab-title>`, for example `issue-1-add-claude-md`.
- Open one branch and one PR per issue.
- Link the PR to its issue with `Closes #<number>` in the PR description, so merging closes the issue.

## Steps

1. Branch off the latest `main`:

   ```sh
   git fetch origin main
   git checkout -b issue-<n>-<short-title> origin/main
   ```

2. Commit with clear, descriptive messages.
3. Push: `git push -u origin issue-<n>-<short-title>`
4. Open a PR against `main` that references the issue.
