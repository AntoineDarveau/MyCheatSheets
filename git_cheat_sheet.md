## When you want to change branch but you can't since you have uncommited changes, but the changes are not ready to be commited!
```shell
git stash  # When you're in the branch
# ... change branch, do whatever you want ...
# ... go back to the branch ...
git stash pop  # Resume to were you were