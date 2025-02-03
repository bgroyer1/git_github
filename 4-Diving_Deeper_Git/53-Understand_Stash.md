# Understanding Git Stash

#### Git stash

```git
    git stash
```

- Stash allows us to store changes without committing them to the branch

#### Stash message

```git
    git stash push -m "push message"
```

- connect your stash with a message so you know what you've stashed!

#### Stash List

```git
    git stash list
```

- a list of all previous stashes within a certain timeframe

#### Stash Apply

```git
    git stash apply
```
  
- revert your working directory to the most recent stash

#### Index

```git
    git stash apply 1
```

- Revert to a specific stash, denoted by index in your stash list

#### Stash Drop

```git
    git stash drop
    git stash drop stash@{2}
```

- Deletes the most recent stash
- Can also specify a specific stash to drop
- permanent

#### Stash clear

```git
    git stash clear
```

- removes **all** stashes in the list
- permanent

