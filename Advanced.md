# Advanced workshop

## Branches

- Branches let you make changes to the codebase on another copy of it, so the changes you push to branch A, will not affect branch B

### Creating Branches

- #### Via Git Branch

```properties
git branch <new-branch-name>
```

- #### Via Git Checkout
- This will both create the branch as well as switch the current head to that branch

```properties
git checkout -b <new-branch-name>
```

### Listing Branches

- This is useful to do to know what branches are available!

```properties
git branch -a
```

- This command will show both the local branches (in white) as well as the remote branches (in red)

### Switching Branches

```properties
git checkout <branch-name>
```

- Useful options
  - `-f` _**DANGER**_ this will remove _forever_ the local changes that have not been committed yet

### Merging Branches

- pull, rebase, merge

### Deleting Branches

- Branches can easily be deleted locally

```properties
# To delete a merged branch safely, use:
git branch -d <branch-name>

# To force delete a branch, use:
git branch -D
```

- Generally as a rule of thumb, using `-d` is preferred over `-D`, as the latter doesn't care if the branch is merged or not.

## Stashing Changes

-

## Cherry-picking

-

## Merge Conflicts

-

## Changing History

-
