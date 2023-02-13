# Contributing

Welcome to the project!

We encourage contribution in a manner consistent with the [Code of Conduct](CODE_OF_CONDUCT.md).
The following will guide you through the process.

There are a number of ways you can contribute:

1. [Asking questions](#questions)
1. [Requesting features](#feature-requests)
1. [Reporting bugs](#bug-reporting)
1. [Contributing code or documentation](#contributing-code-or-documentation)

## License Agreements

If your contribution modifies the git repository, the following agreements must be established.

*Note:*  License agreements are only needed for adding, modifying, and deleting artifacts kept within the repository.
In simple terms, license agreements are needed before pull requests can be accepted.
A license agreement is not needed for submitting feature request, bug reporting, or other project management.

### Individual Contributor License Agreement

In order to contribute to this repository, an
[Individual Contributor License Agreement (ICLA)](.github/senzing-individual-contributor-license-agreement.pdf)
must be completed, submitted and accepted.

### Corporate Contributor License Agreement

If the contribution to this repository is on behalf of a company, a
[Corporate Contributor License Agreement (CCLA)](.github/senzing-corporate-contributor-license-agreement.pdf)
must also be completed, submitted and accepted.

### Project License Agreement

The license agreement for this repository is stated in the
[LICENSE](LICENSE) file.

## Questions

Please do not use the GitHub issue tracker to submit questions.

TODO: Instead, use ???

1. ??? Slack ???
1. ??? stackoverflow.com ???

## Feature Requests

All feature requests are "GitHub issues".
To request a feature, create a
[GitHub issue](https://help.github.com/articles/creating-an-issue/)
in this repository.

When creating an issue, there will be a choice to create a "Bug report" or a "Feature request".
Choose "Feature request".

## Bug Reporting

All bug reports are "GitHub issues".
Before reporting on a bug, check to see if it has
[already been reported](https://github.com/search?q=+is%3Aissue+user%3Asenzing).
To report a bug, create a
[GitHub issue](https://help.github.com/articles/creating-an-issue/)
in this repository.

When creating an issue, there will be a choice to create a "Bug report" or a "Feature request".
Choose "Bug report".

## Contributing code or documentation

To contribute code or documentation to the repository, you must have
[License Agreements](#license-agreements) in place.
This needs to be complete before a [Pull Request](#pull-requests) can be accepted.

### Setting up a development environment

#### Set Environment variables

These variables may be modified, but do not need to be modified.
The variables are used throughout the installation procedure.

```console
export GIT_ACCOUNT=senzing
export GIT_REPOSITORY=libpostal
```

Synthesize environment variables.

```console
export GIT_ACCOUNT_DIR=~/${GIT_ACCOUNT}.git
export GIT_REPOSITORY_DIR="${GIT_ACCOUNT_DIR}/${GIT_REPOSITORY}"
export GIT_REPOSITORY_URL="git@github.com:${GIT_ACCOUNT}/${GIT_REPOSITORY}.git"
```

#### Clone repository

Get repository.

```console
mkdir --parents ${GIT_ACCOUNT_DIR}
cd  ${GIT_ACCOUNT_DIR}
git clone ${GIT_REPOSITORY_URL}
cd ${GIT_REPOSITORY_DIR}
```

### Coding conventions

TODO:

### Testing

TODO:

### Pull Requests

Code in the main branch is modified via GitHub pull request.
Follow GitHub's
[Creating a pull request from a branch](https://help.github.com/articles/creating-a-pull-request/)
or
[Creating a pull request from a fork](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) instructions.

Accepting pull requests will be at the discretion of Senzing, Inc. and the repository owner(s).
