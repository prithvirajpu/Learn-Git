# 📘 LEARN GIT BASICS

## 🐧 Basic Linux Commands

---

| Command                              | Description                                        |
| ------------------------------------ | -------------------------------------------------- |
| `mkdir <folder-name>`                | Create a new folder                                |
| `cd <folder-name>`                   | Change directory                                   |
| `cd ..`                              | Move one level up in the directory tree            |
| `ls`                                 | List all files/folders in the current directory    |
| `ls -a`                              | List all files including hidden files              |
| `ls -l`                              | List files in long format with permissions         |
| `pwd`                                | Print the current working directory path           |
| `touch <filename>`                   | Create a new file                                  |
| `vim <filename>` / `nano <filename>` | Open a file in a terminal-based text editor        |
| `cat <filename>`                     | Display contents of the file                       |
| `cp <source> <destination>`          | Copy files or folders                              |
| `mv <source> <destination>`          | Move or rename files/folders                       |
| `rm -rf <filename>`                  | Remove file or folder (forcefully and recursively) |
| `clear`                              | Clear the terminal screen                          |
| `history`                            | Show previously used commands                      |
| `man <command>`                      | Show manual/help page for the given command        |
| `echo <text>`                        | Print text to terminal                             |
| `chmod +x <file>`                    | Make a file executable                             |
| `sudo <command>`                     | Run command as superuser (admin privileges)        |
| `df -h`                              | Show disk space in human-readable format           |
| `top`                                | Display real-time running processes                |
| `ps aux`                             | Show all running processes                         |
| `kill <pid>`                         | Kill a process with given process ID               |
| `grep "<text>" <filename>`           | Search for text in a file                          |
| `find <path> -name "<filename>"`     | Search for a file by name                          |
| `tar -xvf <file>.tar`                | Extract a .tar archive                             |
| `unzip <file>.zip`                   | Extract a .zip archive                             |
| `curl <url>`                         | Fetch data from a URL (basic API call/testing)     |
| `wget <url>`                         | Download files from the internet                   |

---

---

# 🧠 Important Git Terms to Know Before Getting Started

| Term                     | Description                                                                                                            |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| **Repository (repo)**    | A project folder tracked by Git. Can be local or hosted on platforms like GitHub, GitLab, etc.                         |
| **Working Directory**    | The actual files and folders you’re currently working on in your system.                                               |
| **Staging Area (Index)** | A place where changes are added (`git add`) before they are committed. Think of it as a “preview” of your next commit. |
| **Commit**               | A snapshot of the staged changes. Commits include a unique ID and message.                                             |
| **HEAD**                 | A pointer to the latest commit in the current branch.                                                                  |
| **Branch**               | A lightweight movable pointer to a commit. Used to develop features independently from the main codebase.              |
| **Merge**                | Combine changes from one branch into another. Typically done to integrate feature branches into the main branch.       |
| **Conflict**             | Happens when Git cannot automatically resolve differences between two branches. Must be resolved manually.             |
| **Clone**                | Copy of a remote repository to your local machine (`git clone`).                                                       |
| **Pull**                 | Fetch and merge changes from the remote repository to your current branch (`git pull`).                                |
| **Push**                 | Upload local commits to the remote repository (`git push`).                                                            |
| **Remote**               | A version of your repository hosted on the internet or network (e.g., GitHub).                                         |
| **Fork**                 | A personal copy of someone else's repository, typically used for proposing changes.                                    |
| **Stage (Staged)**       | Files added to the staging area using `git add` and ready to be committed.                                             |
| **Unstage**              | Removing files from the staging area using `git restore --staged`. Changes remain in working directory.                |
| **Revert**               | Creates a new commit that undoes changes of a previous commit without modifying the history.                           |
| **Reset**                | Moves HEAD and optionally modifies staging/working directory. Can delete commit history if used carelessly.            |
| **Checkout**             | Switch branches or restore files (`git checkout`).                                                                     |
| **Rebase**               | Reapplies commits on top of another base commit to create a cleaner project history.                                   |
| **Tag**                  | A reference to a specific commit, often used for marking releases (`v1.0.0`).                                          |
| **Stash**                | Temporarily saves uncommitted changes for later use (`git stash`). Useful when switching branches without committing.  |
| **.gitignore**           | A file that tells Git which files/folders to ignore in tracking (e.g., node_modules, .env).                            |

---

## 🔧 Basic Git Commands

| Command                           | Description                                                |
| --------------------------------- | ---------------------------------------------------------- |
| `git init`                        | Initialize a new Git repository in the current directory   |
| `git status`                      | Show the status of working directory and staging area      |
| `git add <filename>`              | Add specific file to staging area                          |
| `git add .`                       | Add **all** changes (new/modified/deleted) to staging area |
| `git commit -m "your message"`    | Commit the staged changes with a message                   |
| `git log`                         | Show commit history                                        |
| `git reset <commit>`              | Reset the current branch to the specified commit           |
| `git restore <filename>`          | Restore file content from the latest commit                |
| `git restore --staged <filename>` | Unstage a file without discarding changes                  |
| `git diff`                        | Show changes not yet staged                                |
| `git diff --staged`               | Show staged changes that will be committed                 |
| `git rm <filename>`               | Remove a file from working directory and staging area      |
| `git mv <old> <new>`              | Rename or move a file                                      |

---

## 🧳 Stashing Changes

| Command           | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| `git stash`       | Stash current changes in a hidden stack                      |
| `git stash pop`   | Re-apply the last stashed changes and remove them from stash |
| `git stash list`  | Show all stashed changes                                     |
| `git stash apply` | Apply the last stash without removing it                     |
| `git stash clear` | Remove all stashed entries                                   |

---

## 🌿 Branching & Merging

| Command                         | Description                                        |
| ------------------------------- | -------------------------------------------------- |
| `git branch`                    | List all branches                                  |
| `git branch <branch-name>`      | Create a new branch                                |
| `git checkout <branch-name>`    | Switch to another branch                           |
| `git checkout -b <branch-name>` | Create and switch to a new branch                  |
| `git merge <branch-name>`       | Merge the specified branch into the current branch |
| `git rebase <branch>`           | Reapply commits on top of another base branch      |
| `git branch -d <branch-name>`   | Delete a branch                                    |

---

## 🌐 Working with Remote Repositories

| Command                            | Description                                         |
| ---------------------------------- | --------------------------------------------------- |
| `git clone <repo-url>`             | Clone a remote repository to your local machine     |
| `git remote -v`                    | View remote connections                             |
| `git remote add origin <repo-url>` | Add a new remote repository                         |
| `git push -u origin <branch>`      | Push branch to remote (set upstream)                |
| `git push`                         | Push local changes to remote                        |
| `git pull`                         | Fetch and merge changes from the remote repository  |
| `git fetch`                        | Download latest changes from remote without merging |

---

## 🛠 Advanced Git Commands

| Command                    | Description                                                       |
| -------------------------- | ----------------------------------------------------------------- |
| `git revert <commit>`      | Create a new commit that undoes the changes of a previous commit  |
| `git cherry-pick <commit>` | Apply a single commit from another branch                         |
| `git tag <tagname>`        | Create a tag for marking specific points in history (e.g. v1.0.0) |
| `git clean -fd`            | Remove untracked files and directories                            |
| `git blame <file>`         | Show who made each change in a file                               |
| `git show <commit>`        | Show details of a specific commit                                 |

---

## ✅ Best Practices.

- Always write **meaningful commit messages**
- Use **branches** for features and fixes
- Keep `main` or `master` branch clean and stable
- Regularly **pull** changes when working in a team
- Use `.gitignore` to avoid committing unnecessary files
