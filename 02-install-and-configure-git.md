# Install and Configure `Git`

In this section, we will learn following topics:

_1. Install and Configure Git on Linux_

_2. Install and Configure Git on Windows_

## 01. Install and Configure `Git` on Linux machines

### Step-1.1: Install `Git`

- Install Git on Amazon Linux 2/CentOS/RHEL

  ```
  sudo yum install -y git
  ```

- For installing Git on other linux distributions, kindly refer this link: https://www.git-scm.com/download/linux

### Step-1.2: Verify the `Git` installation

- On terminal, run following command to check if the git is installed on the system:

```
# Display the current installed version of the Git
git --version
```

### Step-1.3: Configure Git

- To configure Git, you must define some global variables:
  1. **user.name**
  2. **user.email**
- Both are required for you to make commits.

```
# Replace <USER_NAME> with the user name
git config --global user.name "<USER_NAME>"

# Replace <USER_EMAIL> with your e-mail address
git config --global user.email "<USER_EMAIL>"
```

- You may run the following command to check all the git variables (including email and name):

```
git config --list

OR

git config -l

# You must see "user.name" and "user.email" variables updated with your details
```

## 02. Install and Configure `Git` on Windows machines

### Step-2.1: Download, Install and Configure Git

- Download the Git binary from https://git-scm.com/download/win
- Once the executable is download, click on it to launch the installation.

### Step-2.2: Verify the Git installation

- In order to check if the Git is properly installed navigate to **Start menu** >> **Command Prompt**

```
git --version

# Above command should give you current installed version of the Git; something like this
git version 2.41.0.windows.3
```

### Step-2.3: Configure Git

- To configure Git, you must define some global variables:
  1. **user.name**
  2. **user.email**
- Both are required for you to make commits.

```
# Replace <USER_NAME> with the user name
git config --global user.name "<USER_NAME>"

# Replace <USER_EMAIL> with your e-mail address
git config --global user.email "<USER_EMAIL>"
```

- You may run the following command to check all the git variables (including email and name):

```
git config --list

OR

git config -l

# You must see "user.name" and "user.email" variables updated with your details
```
