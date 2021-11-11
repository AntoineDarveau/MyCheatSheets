# Cheat sheet for git
## Rebasing (One way to update your branch)
General idea: "rebase local changes before pushing to clean up your work, but never rebase anything that you’ve pushed somewhere" (https://git-scm.com/book/en/v2/Git-Branching-Rebasing)

## Merging (other way to update a branch)
Better if your branch has been pushed and others are working on it.

## Stash (uncommited changes 😲)
- When you want to change branch but you can't since you have uncommited changes, but the changes are not ready to be commited!
```shell
git stash  # When you're in the branch
# ... change branch, do whatever you want ...
# ... go back to the branch ...
git stash pop  # Resume to were you were
```
Be careful since `git stash pop` will remove the stash from the stash list. If you don't want that, use `git stash apply`
- If you forgot which branch it was or stashed too many things, then use
```shell
git stash list
```
to show the available stash. `git stash pop` will pop the `stash@{0}` by default.

## Track a remote branch
```shell
git fetch <remote name> <branch name>
git branch --track <branch name> <remote name>/<branch name>
```

## Choose which 
