```bash
# Checkout previous branch
git checkout -

# Get SHA of latest commit
git rev-parse HEAD

# Show the content of the stash item stash@{1}
git stash show -p 1

# Use grep to search commit messages
git log --grep="text"

# Examine dangling commits, for example for recovering a lost stash entry
git fsck --no-reflog > fsck
awk '{print $3}' fsck | xargs -I $ git show $ > out
```
