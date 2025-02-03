# Understanding & Creating Branches

## Git Branch

```git
    git branch
```

- shows a list of all branches in your project

## Create Branch

```git
    git branch <new_branch>
```

- new branches do not need quotation marks
- new branch names can not contain spaces
  
## Switch Branch With Checkout

```git
    git checkout <new_branch>
```

- switches to another branch
- all the git commits from the main branch are moved to the new branch
- all commits have the same ID's as main branch commits

## Create branch and switch with checkout

```git
    git checkout -b <new_branch-2>
```

- creates a new branch and immediately switches you to it

## Git Switch

```git
    git switch <branch_name>
```

- newer syntax to stop checkout from handling so many separate operations

## Create Branch and switch to it

```git
    git switch -c <new_branch>
```

- another way to create a branch and immediately switch to it

