# Docs

## Running Docs Locally

1. Create and use the `dev` [development environment](./contributing.md#tox-development-environments)
2. Run the development server: `mkdocs serve`
    - If you are using VS Code, see the [VS Code Integration page](./vscode.md#docs)

## Known Issues

!!! warning "`mkdocs serve` coverage report"

    By default, `mkdocs serve` rebuilds all files whenever a watched file is saved.
    However, an issue arises when it is integrated with [mkdocs-coverage](https://github.com/pawamoy/mkdocs-coverage),
    which is used to generate the Coverage Report page: if a watched file is while `mkdocs serve` is running,
    you will get the warning `mkdocs_coverage.plugin: No such HTML report directory: htmlcov`,
    and the Coverage Report page will not be able to be displayed.

    A workaround is to use dirty reloading, which only re-builds files that have changed: `mkdocs serve --dirtyreload`,
    however this often causes inaccurate navigation and reloading behavior.
