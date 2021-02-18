# github-cheatsheet

These are *github* commands that I frequently use yet constantly forget.

## Undoing commits

### Undo previous commit
```
git reset HEAD~1
```
### Soft reset of first commit
```
git update-ref -d HEAD
```

## Rebase

### Combine last 3 commits in interactive mode
```
git rebase -i HEAD~3
```
### Rebase dev on top of main (will re-write dev's commit history)
```
git checkout dev
git rebase main
```

## Working with Branches

### Create and switch to a new branch
```
git checkout -b hello
```
### Merge new_branch with main, squash commits, and wait for manual commit
```
git checkout main
git merge --squash --no-comit new_branch
```
### Compare branches
```
git diff branch1..branch2
```

### If dev branch is behind main after merge
```
git checkout main
git pull
git checkout dev
git pull
git merge main
git push
```

### Delete a remote branch
```
git push origin --delete branch
```

### I want to work on my own branch, submit a pull request to the master branch, then continue working on my branch
See: https://stackoverflow.com/questions/23008551/what-is-the-proper-way-to-continue-working-on-a-branch-containing-a-pr-under-rev
