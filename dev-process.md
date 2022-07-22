# Dev Process

## To Do

## In progress

### Creating branch

1. `git checkout main`
2. `git checkout -b {issue type}-{issue number}`

### Commit messages

1. #{issuenumber} concise, descriptive message
2. If you need to include more information, put it in the issue itself or the pull request
   1. **please do not put a detailed commit description**, i.e. keep it under 50 characters

### Creating a PR (Pull Request)

1. Search our repository for open or closed [Pull Requests](https://github.com/fax-app/notes/pulls) that relate to your submission. You don't want to duplicate effort.
2. Open a [Pull Request](https://github.com/fax-app/notes/compare?expand=1) if one has not been created already.
4. Name the PR as follows:
>[{issue type}-{issue number}] {issue name}

### Merge main

1. `git checkout main`
2. `git checkout {issue branch}`
3. `git merge main`
4. Resolve conflicts
   1. gitlens vscode extension can help
5. `git commit -m "merge main into {issue branch}`
6. `git push`

## In Review

1. Make sure main has been merged in
2. Run unittests:
   1. fax_server
      1. Run the following command to run all unittests and create a coverage report in the htmlcov/ in the root of the project folder:
         1. `pytest --cov=project --cov-report html:htmlcov`
      2. Flags to add:
         1. `-s` -> will capture output from the tests
         2. `--setup-show` -> will show the fixtures being created and destroyed

## QA


## Product Review

## Done