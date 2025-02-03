# Merging Branches, Heads, and Switch

## Merging

```git
    git checkout main
    git merge second-branch
```

- Change to the main branch, then merge changes from other branches to the main branch
- Merges are logged in git log

## Understanding the head

```git
    git checkout main
```
- The head always refers to the latest commit in a branch by default
- In git log, you can see which commit is acting as the head for each branch. In my log, third-branch and second-branch each have different heads than main 

## Detached Head

```git
    git checkout <unique_id>
```

- When we checkout a previous commit, we aren't checking out a branch anymore, as checking out a branch always goes to that branches latest head
- We are checking out a commit that is sort of floating in the middle of nowhere, and it's called a detached head

## Create a branch out of detached head changes

```git
    git switch -c <new_branch_name>
```

- adding the -c flag allows you to create a new branch of changes you made while working in a detached head
- You can undo this with git switch -

