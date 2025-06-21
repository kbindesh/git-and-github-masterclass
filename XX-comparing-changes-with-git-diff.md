# Showing changes in Git - git diff

## 01. Introduction

- git diff command can be used to view the changes between commits, branches, files, working directory and more.

## 02. Understand how git diff works

```
# Create a new directory

# Initialize the repo
git init

# Create a file stage it and conmmit it
touch cars.txt

git add cars.txt
git commit -m "initial commit"

# Modify the cars.txt file | Add text "tata curve" | Stage and Commit
git add cars.txt
git commit -m "add curve"

# Modify the cars.txt file | Add text "tata harrier" | Stage and Commit
git add cars.txt
git commit -m "add harrier"

[Three commits so far, let's see how git diff works]

# git diff without any additional options will list all the untracked changes
git diff

[You won't see anything, as we do not have any untracked changes here]
[Make some modifications, and then try running git diff]

[Modify the cars.txt file | Add text "altroz"]

# Now, again check the difference
git diff
```
