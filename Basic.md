# Basic Workshop

- Introduce Git (branches, version control, going back in history)
- PSA: Most, if not all, of the git commands covered in this workshop will have `-h` (aka: `--help`) as an option to see what the command can do

## Setup & Installation

- // TODO

## Project Setup

### Initialising A New Project

- Useful for existing local projects you may have forgotten to setup version control for

```properties
git init
git remote add origin <URL>
```

### Cloning An Existing Project

- Useful for downloading remote repositories

```properties
git clone <URL>
cd <repo-name>
```

## Changes

- A change can be a new file, or a deleted file, ... - if the project changed in any way, git will know that it has been changed

### Viewing Changes

- It's nice to double check that you've staged what you should have staged!

- #### Via Git Status

```properties
git status
```

- #### Via Git Diff

```properties
git diff
```

### Staging Changes

```properties
git add <file> <options>
# Or to add all files, use
git add . <options>
```

- Useful options
  - `-p` gives an interactive view for staging changes
  - `-u` only updates files that git has tracked and not _new_ files

### Unstaging (Resetting) Changes

```properties
git reset <file> <options>
# Or to unstage all files, use
git reset . <options>
```

- Useful options
  - `--hard` _**DANGER**_ this will wipe all of the changes made since the last commit
  - `-p` same as `git add <file> -p`, it brings up an interactive view for unstaging changes

## Commits

### Creating A Commit

- When you create a commit, it will take all of the changes that have been staged so far and bundle that up into a single commit

```properties
git commit <options>
```

- Useful options
  - `-m "My commit message"` adds a commit message to the commit, otherwise you will have to use the interactive prompt
- Options you can use without using `git add` to stage changes beforehand
  - `-p` brings up an interactive view for committing changes
  - `-a` will commit all changes

### Viewing Past Commits

```properties
git log
```

### Pushing Commits

- Everything so far has all been local and the remote repository needs updating!
- Pushing will update the remote repository with the commit(s) you have just made

```properties
git push <options>
# Or to push directly to the same branch on the remote repo, use
git push <remote-name> head
```

- Useful options
  - `-f` _**DANGER**_ force updates the remote and overwrites any more recent changes
  - `-u <remote-name> <branch-name>` links a local branch to a remote branch, so you can then use `git push` and `git pull` without arguments
