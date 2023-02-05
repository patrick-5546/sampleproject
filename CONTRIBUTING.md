# Contributing Guide

## Setup

1. [Install tox](https://tox.wiki/en/latest/installation.html)
2. Clone repository
3. Create development environment: In the root directory of the repository, `tox devenv -e dev .venv`
4. Use development environment: [activate Python virtual environments](https://realpython.com/python-virtual-environments-a-primer/#activate-it)

## Commands

Since all dependencies noted below are installed in the development environment,
they can be run independently in the terminal.

- `tox`
    - Tests using [pytest](https://pypi.org/project/pytest/)
    - Lint environment:
        - Checks style using [flake8](https://pypi.org/project/flake8/)
        - Type checks using [mypy](https://pypi.org/project/mypy/)
    - Coverage environment: generates coverage reports using [coverage](https://pypi.org/project/coverage/)
        - To view coverage report, open `htmlcov/index.html` in a browser
        - If you get the error "No data to combine" while running `coverage combine`, delete `.coverage`
- `tox -e format`
    - Formats using [black](https://pypi.org/project/black/)
    - Sorts dependencies using [isort](https://pypi.org/project/isort/)
- `tox -e upgrade`
    - Upgrade dependencies using [pip-tools](https://pypi.org/project/pip-tools/)

## VS Code Integration

Relevant files can be found in  [`.vscode/`](.vscode).

- Recommended extensions: recommends helpful extensions to be installed
- Pytest with coverage
- Format on save
- Ruler at line length limit
- Show trailing whitespace
