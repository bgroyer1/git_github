# Commiting "Detached Head" Changes

- We added a dummy file to the working directory
- Switched to detached head mode, added a file, made some changes
- Switched **back to main**, got a message saying if we want to save the changes made in detached head mode, you have to create a branch

```git
    git branch <branch_name> <commit_id>
```

- This created a new branch that stored the changes made while in detached head mode
- Note when i stashed changes and attempted to merge, i got a merge conflict warning, and had to resolve the conflict

```git
    git log
    git checkout <commit_id>
    git add .
    git commit -m 'adding files in detached head mode'
    git branch detached-head-mode-2
    git switch main
```

- The above method is basically the same thing, except we created the branch *while we were in detached head mode*, instead of creating a branch with the changes *after* switching back to main