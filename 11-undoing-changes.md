# Undoing changes (Rollback changes to any prev commit)

## 01. Checking out to old commits - `git checkout`

```
[Make some modification in the repo and commit the changes (commit-1)]

[Make some more modification in the repo and commit the changes (commit-2)]

[Now, the HEAD is pointing to commit-2]

# List all the commits to get the commit details (msg, ID)
git log
OR
git log --oneline

# Rollback the changes to any previous commit
git checkout <COMMIT_ID>
git checkout 586f664

[The preceding command will move the HEAD to previous commit with DETACHED HEAD]

# To check, where is the HEAD pointing to
git log --oneline

git status
[You will find HEAD in the dettached state]
```

Now, you will have couple of options to fix the detached HEAD problem:

1. Stay in the detached HEAD to observe the contents of old commits

2. Reattach HEAD by moving it to a branch (say master)

3. Create a new branch and switch to it. The HEAD will be no longer in detached state.

### 1.1 Re-attaching `HEAD` to a branch (e.g. master)

```
[Make sure HEAD is in the detached state]

# Moving the HEAD to Master branch
git switch master

# To check the status
git status

# Check the commits on Master branch
git log --oneline
```

### 1.2 Create a new branch and switch to it

```
[Make sure HEAD is in the detached state]

# Create a new branch from the old commit
git switch -c <NEW_BRANCH_NAME>

# Check the status to know the HEAD position | will be pointing to new branch
git status

[Now, you can make modification on the new branch and commit the changes]
git add .
git commit -m "commit msg"
```

## 02. Discarding changes with `git checkout`

- Let's say you made some changes to a file and you do not want to keep them.
- To revert all the new changes you made to your last commit, you can use:

```
git checkout HEAD <filename>
```

## 03. Unstaging changes with `git restore`

## 04. Undoing commits - **git reset**
