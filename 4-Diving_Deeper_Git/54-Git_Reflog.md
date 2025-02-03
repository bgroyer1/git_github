# Bringing Back Lost Data

- Created a new branch to practice reflog
- Created a file, committed it
- Created another file, committed that
- Decided we don't want the new file, used git reset to move the head back by one commit
- Now, we've changed our minds, and we want the lost file back

```git
    git reflog
```

- This shows us all our actions in git
- We are able to revert to the previous head, even though it is no longer in the git log, using git reflog
- These changes are held for **30 days**

#### Recreating branches

```git
    git checkout <commit_id>
    git switch -c branch
```

- Readding a deleted branch requires two steps: checking out the commit from that branch, and then creating a branch while in that detached head state