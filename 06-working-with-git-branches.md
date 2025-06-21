# Introducing Git Branches

## 01. What are Branches?

## 02. The Master branch (or main)

- The default branch name is _master_
- _master_ branch doesn't do anything very special.
- It is just like any other branch
- Many people designate master branch as a single source of truth
- In 2020, GitHub renamed the default branch from _master_ to _main_.
- The default git branch is still _master_.

## 03. What is HEAD?

- HEAD is simply a pointer that refers to the current "location" in the repository.
- It points/refers to a particular branch reference.

## 04. Working with the `Branches`

### View all the Branches - `git branch`

```
git branch
```

### Create & Switch Branches - `git branch <BRANCH_NAME>`

- **Create a Branch**

```
# Syntax - To create a new branch
git branch <BRANCH_NAME>
OR
git checkout <BRANCH_NAME>

# Examples
git branch development
git branch bugfix


# Create a branch & switch to it
git switch -c <BRANCH_NAME>
git switch -c integration

OR

git checkout -b <BRANCH_NAME>
git checkout -b integration
```

- **Switch to other branch** - `git switch` & `git checkout`

```
# Method-01: Switch to other git branch using 'git switch'
git switch <BRANCH_NAME_TO_SWITCH_TO>



# Method-02: Switch to other git branch using 'git checkout'
git checkout <BRANCH_NAME_TO_SWITCH_TO>
```

## 05. Deleting and Renaming Branches

- **Delete a Branch**

```
# Delete a Branch
git branch -d <BRANCH_NAME_TO_DELETE>
OR
git branch --delete <BRANCH_NAME_TO_DELETE>



# Forcefully deleting a branch if there is any dependencies
git branch -d <BRANCH_NAME> --force

OR

git branch -d <BRANCH_NAME> -D
```

- **Renaming a Branch** - `-m`

- IMP: To rename a branch you have to be on that branch.

```
# Switch to the branch you want to rename
git checkout <BRANCH_NAME>

# Rename the branch
git branch -m <BRANCH_NAME>
```

## 06. Switching Branches with unstaged changes

## Hands-on Excersice - Git Branches
