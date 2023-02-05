# Contributing Guide

## Setup

1. [Install tox](https://tox.wiki/en/latest/installation.html)
2. Clone repository
3. Create development environment: In the root directory of the repository, `tox devenv .venv`
4. Use development environment: [activate Python virtual environments](https://realpython.com/python-virtual-environments-a-primer/#activate-it)

## Commands

- `tox`
    - Tests using [pytest](https://pypi.org/project/pytest/)
    - Formats using [black](https://pypi.org/project/black/)
    - Type checks using [mypy](https://pypi.org/project/mypy/)
    - Generates coverage reports using [coverage](https://pypi.org/project/coverage/)
        - To view coverage report, open `htmlcov/index.html` in a browser
- All `tox` dependencies are installed in the development environment so that they can be run independently
