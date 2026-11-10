# api2md GitHub Action Demo

This repository demonstrates how to use `api2md` as a GitHub Action to automatically generate API documentation and validate OpenAPI specs in a CI/CD pipeline.

## What This Demonstrates

- **Local vs. Production Specs:** `old.yaml` represents the current production API, while `new.yaml` represents an incoming change from a developer.
- **CI/CD Automation:** The `.github/workflows/docs.yml` file runs `api2md` every time a Pull Request is opened.
- **Markdown Generation:** It automatically validates the spec and generates a `docs/API.md` file.
- **Breaking Change Detection:** It can catch breaking changes (like removed parameters) before they merge.

## How to Test It

1. Open a Pull Request to the `main` branch.
2. The GitHub Action will automatically trigger.
3. Check the "Actions" tab to see the validation logs.
4. Check the "Files changed" tab to see the auto-generated Markdown diff.