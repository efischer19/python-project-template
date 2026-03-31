# blueprint-repo-blueprints

> The language-agnostic grandparent template from which all other blueprint repos are derived.

## What Is This?

This is a **GitHub template repository** that provides the foundational directory structure, documentation, and configuration shared by all downstream blueprint repositories. It contains no language-specific content — only the universal scaffolding that every project needs.

## How to Use This Template

1. Click the **"Use this template"** button at the top of the repository page on GitHub.
2. Choose a name for your new repository (e.g., `blueprint-python`, `blueprint-node`).
3. Clone your new repository and begin adding language-specific content.

For more details on GitHub template repositories, see the [official documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository).

## What's Included

| Path | Purpose |
| :--- | :--- |
| `meta/adr/` | Architecture Decision Records — the logbook of *why* decisions were made |
| `meta/plans/` | Project plans and roadmaps |
| `docs-src/` | Source files for generated documentation (e.g., MkDocs) |
| `scripts/` | Utility and automation scripts |
| `.github/` | GitHub-specific configuration (issue templates, PR templates) |

### Key Files

- **`LICENSE.md`** — MIT License
- **`CODE_OF_CONDUCT.md`** — Contributor Covenant Code of Conduct
- **`SECURITY.md`** — Security policy and vulnerability reporting
- **`CONTRIBUTING.md`** — Guidelines for contributing to the project
- **`meta/adr/TEMPLATE.md`** — Template for new Architecture Decision Records
- **`meta/adr/ADR-001-use_adrs.md`** — The founding ADR: use ADRs to document decisions

## Getting Started

After creating a new repository from this template:

### 1. Replace Template Placeholders

Search the repository for the following placeholders and replace them with values appropriate for your project:

| Placeholder | Description | Example |
| :--- | :--- | :--- |
| `{{PROJECT_NAME}}` | Your repository / project name | `my-awesome-project` |
| `{{GITHUB_OWNER}}` | GitHub username or organization | `my-org` |
| `{{APP_NAME}}` | Application directory name (in `templates/readme/apps.md`) | `web-app` |
| `{{LIB_NAME}}` | Library directory name (in `templates/readme/libs.md`) | `core-utils` |
| `{{CATEGORY_NAME}}` | Feature category (in `docs-src/feature-request-automation.md`) | `data-pipeline` |
| `{{PROJECT_URL}}` | Public URL for your project (in `meta/ROBOT_ETHICS.md`) | `https://example.com` |

### 2. Customize Key Files

- **`README.md`** — Replace this content with your project's description.
- **`mkdocs.yml`** — Update site name, description, and URL after replacing placeholders.
- **`docs-src/index.md`** — Replace the placeholder setup instructions with your own.
- **`meta/DEVELOPMENT_PHILOSOPHY.md`** — Review and adjust principles to fit your project's needs.
- **`SECURITY.md`** — Update contact information for vulnerability reporting.

### 3. Set Up Local Development

```bash
# Install pre-commit hooks
pip install pre-commit
pre-commit install

# Run local quality checks
./scripts/local-ci-check.sh

# Build documentation (optional)
pip install -r docs-requirements.txt
./scripts/build-docs.sh
```

### 4. Verify CI

Push a change or open a pull request to confirm the CI workflow runs and passes in your new repository.

## Design Principles

- **Minimal by design.** Downstream blueprints add language-specific tooling, CI/CD, and dependencies.
- **Documentation-first.** Every significant decision is captured in an ADR.
- **AI-friendly.** The structure and conventions are designed to work well with AI-assisted development workflows.

## License

This project is licensed under the [MIT License](./LICENSE.md).
