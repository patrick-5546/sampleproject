# Docs

The Docs were created using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/),
a Markdown static site generator with a material design theme. Consult their
[Setup](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/) and
[Reference](https://squidfunk.github.io/mkdocs-material/reference/) docs pages for a
comprehensive list of available features.

## Running Docs Locally

1. Create and use the `dev` [development environment](./contributing.md#tox-development-environments)
2. Run the development server: `mkdocs serve`
    - If you are using VS Code, see the [VS Code Integration page](./vscode.md#docs)

## Building for Offline Usage

To build for offline usage, uncomment the `offline` plugin in `mkdocs.yml`
before running `mkdocs build`. For what this does, refer to
[the related Material for Mkdocs docs page](https://squidfunk.github.io/mkdocs-material/setup/building-for-offline-usage/).
