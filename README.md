# Test Release Repository

## Overview

This repository is designed to test **semantic release** functionality with **UV** package manager in a controlled environment.

## Repository Rules

- **Main branch protection**: The `main` branch is protected against direct pushes
- **Pull Requests only**: All changes must be submitted via pull requests
- **Automated releases**: GitHub Actions handles semantic versioning and merges to `main`

## Workflow

1. Develop on feature branches
2. Submit pull requests for review
3. GitHub Actions automatically:
    - Performs semantic release calculations
    - Merges from `dev` to `main` using `bypass` permissions
    - Updates version numbers according to semantic versioning

## Technologies

- **UV**: Python dependency management
- **GitHub Actions**: CI/CD automation
- **Semantic Release**: Automated versioning

## Purpose

This is a testing environment for validating semantic release workflows and automation patterns.
