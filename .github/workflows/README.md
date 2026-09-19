# Workflows

This directory contains GitHub Actions workflows used to automate repository checks.

## CI

The `ci.yml` workflow is a template. Update its commands for the language, framework, and tooling used by the project.

The CI stages are:

1. **Build** — confirm the project builds successfully.
2. **Lint** — check formatting and lint rules.
3. **Tests** — run the automated test suite.
4. **Static Analysis** — run type checking, compiler analysis, or other static checks.
5. **Security Analysis** — run dependency and security checks.
6. **Repository Checks** — verify required repository files and configuration.

## Before pushing

Run the same checks locally whenever practical. Do not rely on GitHub Actions to discover basic problems after every push.

Before opening a pull request, verify:

- The project builds successfully.
- Formatting and linting pass.
- Tests pass.
- Static analysis passes.
- Security/dependency checks pass when available.
- No secrets, credentials, generated files, or unrelated changes are included.
- The final diff is reviewed.

The exact commands depend on the project. Replace the placeholder commands in `ci.yml` and document the local equivalents in the project's development documentation.

## CD

The `cd.yml` workflow is a deployment template. Keep it disabled or configured only after the project has a defined release/deployment process.
