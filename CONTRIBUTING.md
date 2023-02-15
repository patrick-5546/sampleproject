# Contributing

This repository's infrastructure features pinned dependency management, a documentation site, an automated release process,
GitHub integration, VS Code integration, and much more.

## Setup for Local Development

1. [Install tox](https://tox.wiki/en/latest/installation.html)
2. Clone the repository

## Tox

[tox](https://tox.wiki/en/latest/index.html) is used to automate and standardize testing across
local development environments and CI/CD pipelines.

### Tox Configuration

The tox configuration for this repository can be found in `tox.ini`.

### Tox Environments

Each tox environment defined there accomplishes a specific purpose:

- `testenv`:
    - Checks if the package can be built (may be commented out)
    - Runs tests and generates a coverage report source file `.coverage`
- `coverage`: converts `.coverage` to human readable formats
    - `html`: used to create the Coverage Report page
    - `json`: used to create the coverage badge in the README
- `dev`: used to create a development environment with all project and environment dependencies
    - When in the development environment, the commands that are run in each environment can be run in your terminal
- `docs`: builds the docs to ensure that they are in a valid state
- `format`: runs the formatters
- `lint`: runs the linters
- `upgrade`: updates the [dependencies](#dependencies)

#### Running Tox Environments

- `tox -e <environment>` will run a single environment
- `tox` will run all the environments in `envlist`

Known issues running tox environments:

| Environment | Issue                                           | Solution                     |
| ----------- | ----------------------------------------------- | ---------------------------- |
| `coverage`  | `coverage combine` outputs "No data to combine" | Delete `.coverage` and rerun |

#### Tox Development Environments

The `tox devenv` command will create a virtual environment and install the environment's dependencies in it.

- To create a virtual environment with all project and environment dependencies, run `tox devenv -e dev .venv`.
- Using a virtual environment: [activate Python virtual environments](https://realpython.com/python-virtual-environments-a-primer/#activate-it)

## Dependencies

Dependencies are defined in `pyproject.toml`.
They are pinned and managed using [pip-tools](https://pip-tools.readthedocs.io/en/latest/).
The pinned dependencies can be found in `requirements/`.

### How to Add a Dependency

1. Add the dependency to `pyproject.toml`; where you add the dependency depends on what type of dependency it is:
    - Add project dependencies to the `dependencies` list
    - Add [environment](#tox-environments)-specific dependencies to the corresponding list below `[project.optional-dependencies]`
2. Run the `upgrade` tox environment: `tox -e upgrade`
3. If you are using the development environment, [recreate it](#tox-development-environments)
4. Commit and push the changes
