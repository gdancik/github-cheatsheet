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
### Delete a remote branch
```
git push origin --delete branch
```
