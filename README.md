# Test Release Repository

## Overview

This repository is designed to test **semantic release** functionality with **UV** package manager in a controlled environment.

## Repository Rules

- **Main branch protection**: The `main` branch is protected against direct pushes
- **Pull Requests only**: All changes must be submitted via pull requests
- **Automated releases**: GitHub Actions handles semantic versioning after merge to `main`

## Workflow

1. Develop on `dev` using Conventional Commits (`feat:`, `fix:`, `BREAKING CHANGE:`).
2. Open a PR from `dev` to `main`.
3. On PR events (`opened`, `synchronize`, `reopened`), CI runs with `uv`.
4. When the PR is merged to `main`, semantic release runs and:
   - creates/pushes a Git tag (`vX.Y.Z`)
   - creates the GitHub release
   - does **not** push any commit to `main` (`--no-commit --no-changelog`)

## Technologies

- **UV**: Python dependency management
- **GitHub Actions**: CI/CD automation
- **python-semantic-release**: Automated versioning

## Purpose

This is a testing environment for validating semantic release workflows and automation patterns.

## Important Note

Because `main` is protected and only accepts PRs, release writes are limited to tags and GitHub releases.
If you need `CHANGELOG.md` committed on `main`, you must use a dedicated bot/App with bypass permissions (or open an automated PR for changelog updates).
