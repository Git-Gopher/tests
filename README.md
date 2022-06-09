# Tests

Integration tests for git-gopher. Tests have been created on orphan branches, meaning that each branch represents a separate test. However, all tests share the same github history, meaning that pull requests, issues etc are shared. When creating tests on go-gopher you should manually filter your data (or just leave it in if it's acceptable) when creating a enriched model.
Testing should also pull down an isolated branch when testing such that all branches are not fetched for each test. The `main` branch should be conserved as a directory.

Obviously when branching you want to use the `--orphan` flag. Eg: `git branch --orphan test/two-parents-merged`

## Syntax

Some care should be taken to ensure consistent syntax when creating tests. The syntax is the following:

| type   | syntax                                              |
| ------ | --------------------------------------------------- |
| branch | `test/<test-name>/<number-of-branch>`               |
| pr     | `test/<test-name>/<number-of-branch>/<pr-title>`    |
| issue  | `test/<test-name>/<number-of-branch>/<issue-title>` |

## Branches

Test branches should be prefixed with `test/` along with a descriptive name. Eg: `test/two-parents-merged/0`. Obviously some tests may span multiple branches so all tests should be labeled with a branch number . Eg: `test/two-parents-merged/0`. Attempt not to delete the branches after you have used them unless it's part of the test

### Commits

This may depend on the type of test that we are doing, however in order to aid reusability of some tests we should be making genuine commit messages, such as one a student would make. You can also use verbiage if you like (Eg: `fix: login component state bug`)

### Issues

A drawback of using a single repository for all of our tests is that they must share the same github issues/prs. In order to combat we need to be using a consistent syntax for labelling these. Suggested is when creating an issue use the name of the test in the title, followed by the the name of the test. Eg: `test/two-parents-merged/0/issue-title`. The body of the issue can be anything

### Pull Requests

Pull request should follow the same sort of format as the issue titles. Eg: `test/two-parents-merged/0/pr-title`

## Test List

| test                    | description                         |
| ----------------------- | ----------------------------------- |
| test/two-parents-merged | check that a commit has two parents |
