## To Do

## In progress
### Creating branch
1. `git checkout main`
2. `git checkout -b {issue type}-{issue number}`

### Commit messages
1. #{issuenumber} concise, descriptive message
2. If you need to include more information, put it in the issue itself or the pull request
   1. **please do not put a detailed commit description**, i.e. keep it under 50 characters

### Creating pull request
1. go to repo on github.com
2. name the request as follows:
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

## QA

## Product Review

## Done