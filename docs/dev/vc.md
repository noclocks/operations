# Version Control

No Clocks, LLC implements version control in all software projects. We use version control to track changes to code, collaborate with team members, and manage releases.

This document outlines our version control practices, including the tools we use, the branching strategy we follow, and the best practices we adhere to.

## Contents

- [Version Control](#version-control)
  - [Contents](#contents)
  - [Overview](#overview)
  - [Git Flow](#git-flow)
  - [Git Clients](#git-clients)
  - [Git Best Practices](#git-best-practices)
  - [Branching Strategy](#branching-strategy)
  - [Versioning](#versioning)
  - [Release Process](#release-process)
  - [References](#references)

## Overview

Below is a list of version control systems we use:

- [Git](https://git-scm.com/)
- [GitHub](https://github.com)

We also can use the following version control platforms as necessary:

- [GitLab](https://gitlab.com)
- [Bitbucket](https://bitbucket.org)
- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/)

## Git Flow

No Clocks, LLC uses the [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/) branching model for software development. The Git Flow model consists of two main branches:

- `main`: The main branch contains the latest stable release of the software.
- `develop`: The develop branch contains the latest development changes.
- `feature`: Feature branches are created from the develop branch and are used to develop new features.
- `release`: Release branches are created from the develop branch and are used to prepare for a new release.
- `hotfix`: Hotfix branches are created from the main branch and are used to fix critical bugs in the stable release.
- `support`: Support branches are created from the main branch and are used to maintain older releases.

## Git Clients

No Clocks, LLC uses a variety of Git clients to interact with Git repositories. Below is a list of Git clients we use:

- [Git](https://git-scm.com/) (command-line)
- [GitHub Desktop](https://desktop.github.com/)
- [GitKraken](https://www.gitkraken.com/)
- [Sourcetree](https://www.sourcetreeapp.com/)
- [Visual Studio Code](https://code.visualstudio.com/) with Git integration
- [PyCharm](https://www.jetbrains.com/pycharm/) with Git integration
- [RStudio](https://www.rstudio.com/) with Git integration

## Git Best Practices

No Clocks, LLC follows the following best practices when using Git:

- Commit early and often.
- Write clear and descriptive commit messages.
- Use feature branches for new development work.
- Use pull requests for code reviews.
- Keep commits small and focused.
- Use merge commits to preserve the history of changes.
- Use tags to mark releases.
- Use `.gitignore` files to exclude unnecessary files from version control.
- Use `.gitattributes` files to configure Git behavior.
- Use Git hooks to automate tasks.
- Use Git submodules for managing dependencies.
- Use Git LFS for large files.
- Use Git aliases for common commands.
- Use Git bisect for debugging.
- Use Git rebase with caution.
- Use Git cherry-pick with caution.
- Use Git reflog to recover lost commits.
- Use Git stash to save work in progress.
- Use Git blame to track changes to code.
- Use Git log to view commit history.
- Use Git diff to view changes between commits.
- Use Git reset to undo changes.
- Use Git revert to undo commits.
- Use Git clean to remove untracked files.

## Branching Strategy

No Clocks, LLC follows the following branching strategy when using Git:

- `main`: The main branch contains the latest stable release of the software. Changes are merged into the main branch using pull requests.
- `develop`: The develop branch contains the latest development changes. Feature branches are merged into the develop branch using pull requests.
- `feature`: Feature branches are created from the develop branch and are used to develop new features. Feature branches are merged into the develop branch using pull requests.
- `release`: Release branches are created from the develop branch and are used to prepare for a new release. Release branches are merged into the main branch using pull requests.
- `hotfix`: Hotfix branches are created from the main branch and are used to fix critical bugs in the stable release. Hotfix branches are merged into the main branch using pull requests.
- `support`: Support branches are created from the main branch and are used to maintain older releases. Support branches are merged into the main branch using pull requests.

## Versioning

No Clocks, LLC follows the [Semantic Versioning](https://semver.org/) standard for versioning software. Semantic Versioning consists of three numbers separated by dots: `MAJOR.MINOR.PATCH`. The numbers have the following meanings:

- `MAJOR`: Incremented for incompatible changes.
- `MINOR`: Incremented for new features.
- `PATCH`: Incremented for bug fixes.
- `PRE-RELEASE`: Optional pre-release version.
- `BUILD-METADATA`: Optional build metadata.
- `VERSION`: The full version number.

## Release Process

No Clocks, LLC follows the following release process when releasing software:

1. Create a release branch from the develop branch.
2. Update the version number in the software.
3. Update the changelog with the changes in the release.
4. Test the software to ensure it is working correctly.
5. Merge the release branch into the main branch.
6. Tag the release with the version number.
7. Deploy the release to production.
8. Update the documentation with the new release information.
9. Notify users of the new release.
10. Celebrate the release with the team!
11. Monitor the release for any issues.
12. Create a support branch for the release if necessary.
13. Update the version number in the develop branch for the next release.

## References

- [Git](https://git-scm.com/)
