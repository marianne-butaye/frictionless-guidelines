# Contributing to a frictionless project

This project accepts contributions. In order to contribute, you should
pay attention to a few things:

1. your code must follow the coding style rules
2. your code must be unit-tested
3. your code must be documented
4. your work must be signed (see below)

# Coding and documentation Style

Refer to [pep8](https://www.python.org/dev/peps/pep-0008/)

# Submitting Modifications

The contributions should be submitted through GitHub Pull Requests.

1. Create a branch off `master` for each new feature/bug fix you'd like to implement
```bash
$ git checkout master
$ git checkout -b feat/my_feature_branch
$ #git checkout -b fix/my_fix_branch
$ #git checkout -b chore/my_refactor_branch
```
2. Write your code, tests showing your code works and fails properly (using [pytest](https://docs.pytest.org/en/latest/)) and documentation as Sphinx docstrings (see [reStructuredText](http://docutils.sourceforge.net/rst.html))
3. Before pushing to remote repository, make sure your branch is up to date with the latest `master` version:
```bash
$ git fetch
$ git checkout master
$ git merge origin/master
$ git checkout feat/my_feature_branch
$ git rebase master  # You might have to solve conflicts here
```
4. Push your branch to remote repository
```bash
$ git push origin my_feature_branch
```
5. On GitHub, create a new [pull request](https://github.com/adeo/network_security_api/pulls) to merge `feat/my_feature_branch` into `master`
6. The pull request creation will trigger [CircleCI](https://circleci.com/gh/adeo/network_security_api) to run all project tests
7. At least one other member of dev team must review the pull request and give its approval
    - If the pull request is rejected, go back to **step 2** to fix what's wrong
8. Once approval has been given, the *author* of the pull request must merge it into `master` branch using the **Merge pull request** mode.
