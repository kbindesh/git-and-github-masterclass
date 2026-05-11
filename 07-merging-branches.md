# Merging Git Branches

_Branch merging_ is a git mechanism to move the changes from one git branch into another.

- [git merge](https://git-scm.com/docs/git-merge) documentation

## 01. Perform a Branch Merge using `Git` CLI

- **Scenario**: Assume that you are developing a new feature (login), and you want to merge the changes into `main` branch (live code).

```
# Create and switch to a branch - To avoid messing up the working version of your project
git checkout -b feature-login

# Develop functionality | Once ready, stage and commit them to your new feature-branch
git add .
git commit -m "Added login functionality"

# Switch to the destination branch (main/master)
git switch main

# Perform the branch merge
git merge feature-login
```

## 02. Perform a Branch Merge on `GitHub`

- This is the standard way to merge branches in a team setting because it allows for code reviews and automatic conflict checks.

### Lab: Merging branch on `GitHub` via web interface

- **Scenario**
  - Imagine that you are building a web application and you have the following branches:
    1. `main` branch: For your live webapp code.
    2. `feature-login` branch: Branch where you've built a new login page functionality.
  - And you would like to merge the `feature-login` branch to `main` branch.

- **Step-by-Step Process**
  1. **Push your changes**
     - Ensure your feature-login branch is pushed to GitHub.

  2. **Create a Pull Request (PR)**
     - Navigate to your repository on GitHub.
     - Click Compare & pull request (often appears in a yellow banner after a recent push).
     - Set base to `main` and compare to your `feature-login` branch.

  3. **Review and Discuss**
     - Add a title and description of your changes.

     - Team members can now comment on specific lines of code.

  4. **Check for Conflicts**
     - GitHub will automatically check if the branches can be merged cleanly.

     - If there are "merge conflicts" (changes to the same lines in both branches), you must resolve them before proceeding.

  5. **Merge**
     - Scroll to the bottom and click **Merge pull request**, then Confirm merge.
  6. **Clean-up**
     - Click **Delete branch** to keep your repository tidy.
