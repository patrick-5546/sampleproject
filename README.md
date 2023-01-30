# A sample Python project

[![Test][testbadge]][testfile]
![Coverage][covbadge]

![Python Logo](https://www.python.org/static/community_logos/python-logo.png "Sample inline image")

A sample project that exists as an aid to the [Python Packaging User
Guide][packaging guide]'s [Tutorial on Packaging and Distributing
Projects][distribution tutorial].

This project does not aim to cover best practices for Python project
development as a whole. For example, it does not provide guidance or tool
recommendations for version control, documentation, or testing.

[The source for this project is available here][src].

The metadata for a Python project is defined in the `pyproject.toml` file,
an example of which is included in this project. You should edit this file
accordingly to adapt this sample project to your needs.

---

This is the README file for the project.

The file should use UTF-8 encoding and can be written using
[reStructuredText][rst] or [markdown][md] with the appropriate [key set][md
use]. It will be used to generate the project webpage on PyPI and will be
displayed as the project homepage on common code-hosting services, and should be
written for that purpose.

Typical contents for this file would include an overview of the project, basic
usage examples, etc. Generally, including the project changelog in here is not a
good idea, although a simple “What's New” section for the most recent version
may be appropriate.

## Initializing the repository

Steps to complete after using this template to create a repository.

### Update Badges

1. Update the `testbadge` and `testfile` URLs in this file with the repository owner and name where applicable
2. Create an empty secret gist named `covbadge.json` and copy its ID
3. Update the `covbadge` URL in this file with the repository owner and gist ID where applicable
4. Update the "Make badge" step of "Coverage" in [`.github/workflows/tests.yml`](.github/workflows/test.yml) with the
   repository owner, repository name, and gist ID where applicable
5. Create a GitHub personal access token with the "gist" scope and copy its value
6. Create a repository secret named "GIST_TOKEN" and paste the token

### Update Tests

1. Update `source` in [`.coveragerc`](.coveragerc) accordingly

## Preparing for release

Steps to complete once ready to publish a release.

1. Go through [`pyproject.toml`](pyproject.toml) and update the relevant fields
2. Uncomment `testenv` dependencies and commands for build and twine in [`tox.ini`](tox.ini)
3. Create a repository secret named "pypi_password" with the corresponding value
4. Releases will be pushed to PyPI once they are published on GitHub

[testbadge]: https://github.com/patrick-5546/sampleproject/actions/workflows/test.yml/badge.svg
[testfile]: https://github.com/patrick-5546/sampleproject/actions/workflows/test.yml
[covbadge]: https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/patrick-5546/845b19d91f3d03c94677f6fae6eb414c/raw/covbadge.json
[packaging guide]: https://packaging.python.org
[distribution tutorial]: https://packaging.python.org/tutorials/packaging-projects/
[src]: https://github.com/pypa/sampleproject
[rst]: http://docutils.sourceforge.net/rst.html
[md]: https://tools.ietf.org/html/rfc7764#section-3.5 "CommonMark variant"
[md use]: https://packaging.python.org/specifications/core-metadata/#description-content-type-optional
