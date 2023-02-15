# Creating a Release

Things to do once ready to publish a release.

1. Go through [`pyproject.toml`](https://github.com/patrick-5546/sampleproject/blob/main/pyproject.toml) and update the
   relevant fields
2. In [`tox.ini`](https://github.com/patrick-5546/sampleproject/blob/main/tox.ini), uncomment `testenv` commands
3. In this file, uncomment badges and uncomment and update their URLs with the package name where applicable
4. Create a repository secret named "PYPI_API_TOKEN" with the corresponding value
5. Releases will be pushed to PyPI once they are published on GitHub
