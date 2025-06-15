# Git Basics

## Setup Git Repository (local)

### Step-XX: Create a project folder/directory

- Git works by checking for changes to files within a certain _folder or a directory_.
- So let's create a folder to serve as our project directory and let Git know about it, so it can start tracking changes.
- Start by creating an empty folder for your project, and then initialize a Git repository inside it:

  ```
  # Create a folder
  mkdir <DIRECTORY_NAME>

  # Change the directory to our project directory
  cd <DIRECTORY_NAME>
  ```

### Step-XX: `Initialize` the project folder as Git repo - `git init`

- Now, initialize your new repository and set the name of the default branch to main:

```
# Initialize a directory as git repo with a default branch created i.e master
git init

# (Optional) To initialize a repo create an initial branch
git init --initial-branch=<NEW_BRANCH_NAME>

# (Optional) Initialize a repo with an initial branch
git init -b <NEW_BRANCH_NAME>
```

- After initializing the repository, you should see output similar to this example:</br></br>

```
Initialized empty Git repository in /home/<user>/repository_name/.git/ </br>
  Switched to a new branch 'main'
```

### Step-XX: Check the Git Repository status - `git status`

- Now, use a `git status` command to show the status of the working tree:
- git status gives information on the current status of a git repository and it's contents.

```
git status
```

## Understanding `.git` folder (hidden)

- `git init` command creates an empty repository - basically a `.git` directory (hidden) with subdirectories for objects, refs/heads, refs/tags, and template files.
- An initial branch without any commits will be created.
- If you want to initialize a repo and at the same time create an initial branch, use `--initial-branch` option, as follows:

## `Git Workflow` - Work on stuff >> Stage it >> Commit it

### Start a new Project folder/directory

- Create a new folder/directory for application files, say **MyFirstApp**.

### Initilize the Repository - `git init`

```
# Get inside above created folder
cd MyFirstApp

# Initialize the directory as a git repo
git init

# (Optional) To initialize a repo create an initial branch
git init --initial-branch=<NEW_BRANCH_NAME>
```

### Add the code files to the Project directory

- Create few app files (e.g. html, css) in the project folder and save it.

### Check the Status of a Repo - `git status`

```
git status
```

### Stage the changes - `git add`

```
# To stage all the untracked changes
git add .

# (Optional) To stage a particular file/s
git add <UNTRACKED_FILE_01_NAME> <UNTRACKED_FILE_02_NAME>
```

### (Optional) Unstage the changes - reset | restore | rm

- You can unstage a file in the Git index and undo a git add operation, any of the following three commands will work:

  1. git reset
  2. git restore
  3. git rm

- **Method-01**: Using `git reset`

  ```
  # Undo the last 'git add' and keep changes in the working dir
  git reset --soft HEAD

  # Unstage specific file/s
  git reset <FILENAME_TO_UNSTAGE>

  # Unstage all the changes
  git reset

  # Discard all the changes entirely
  git reset --hard HEAD
  ```

- **Method-02**: (_Recommended_) Using git restore

  ```
  # To unstage a specific file/s
  git restore --staged <FILENAME_TO_UNSTAGE>

  # To unstage all the changes
  git restore --staged .
  ```

### Commit the changes - git commit

- Commit the changes which are staged before.

```
git commit -m "Start app development"
```

### For getting the list of all the commits - `git log`

```
git log

git log --oneline

git log --all
```
