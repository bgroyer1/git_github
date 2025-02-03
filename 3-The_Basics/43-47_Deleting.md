# Deleting files

## Check files in your Working Directory

```git
    git ls-files
```

- Shows which files are in your current working directory
- Git status shows which files are currently in the staging area, or have changes that are NOT in the staging area

## Deleting from working directory

- Removed a file from the working directory
- It is **still in my staged files** to be added to future commits
- Running git status shows modified and deleted files in the current working directory

## Git add/rm 

```git
    git add <file name>
    git rm <file name>
```

- Removes file from both working directory and staging area
- Git Status will show the name of files deleted from the working directory
- git add <file name> will **delete removed files from the staging area** 
- git rm <file name> wil do the same thing
- I'm going to use rm, the other one feels confusing

## Getting rid of unstaged changes

```git
    git checkout <filename>
    git checkout .
    git restore <filename>
    git restore .
```

- All of these will undo unstaged changes in the working directory
- Checkout was the original one, but git added restore to stop checkout from being used for everything
- I'm going to use git restore in my own coding

## Removing new files added to working directory

```git
    git clean -dn
    git clean -df
```

- The flag -d means we want to delete untracked files
- The flag -n means we want to list the files to that will be deleted
- The flag -f in combination with -d will delete the files from your working directory

## Undoing Staged Changes

```git
    git reset <path_to_file>
    git checkout <file_name>
```

- git reset removes files from the staging area
- Git checkout then undoes the unstaged changes
- This is the "older" way of doing this

```git
    git restore --staged <file>
    git checkout <file-name>
```

- Restore is **the more explicit** command, and should be used in this situation
- Reset has other uses, so it's better to leave it to what its primary focus is

## Git Reset

### Soft Reset

```git
    git reset --soft HEAD~1
    git log
```
- Removes last commit

### Default reset

```git
    git reset HEAD~1
```

- Removes latest commit
- Removes changes added to the staging area

### Git Hard Reset

```git
    git reset --hard HEAD~1
```

- Removes latest commit
- Removes changes in the staging area
- Removes changes in the working directory

## Deleting Branches

### Merge Delete

```git
    git branch -d <branch_name>
```

- Only allows you to delete a branch if the changes have been merged into the current branch

```git
    git branch -D <branch_name>
```

- Deletes a branch , even if the changes haven't been merged
- Note you can delete multiple branches in one command