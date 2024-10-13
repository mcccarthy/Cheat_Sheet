# Version Control (Git) Cheat Sheet

## Common Git Commands

| Command                     | Description                                       | Example                              |
|-----------------------------|---------------------------------------------------|--------------------------------------|
| `git clone <repo-url>`      | Clone a repository into a new directory.         | `git clone https://github.com/user/repo.git` |
| `git init`                  | Initialize a new Git repository.                 | `git init`                           |
| `git status`                | Show the status of changes.                       | `git status`                         |
| `git add <file>`            | Add a file to the staging area.                  | `git add index.html`                 |
| `git commit -m "<message>"` | Commit changes with a message.                   | `git commit -m "Initial commit"`    |
| `git push <remote> <branch>`| Push changes to a remote repository.             | `git push origin main`              |
| `git pull <remote> <branch>`| Fetch and merge changes from a remote repository. | `git pull origin main`               |
| `git fetch <remote>`        | Fetch changes from a remote repository without merging. | `git fetch origin`               |

* * *

## Branching and Merging

| Command                        | Description                                       | Example                              |
|--------------------------------|---------------------------------------------------|--------------------------------------|
| `git branch`                   | List all branches in the repository.              | `git branch`                         |
| `git branch <branch-name>`     | Create a new branch.                              | `git branch feature-branch`         |
| `git checkout <branch-name>`    | Switch to a specified branch.                    | `git checkout feature-branch`       |
| `git checkout -b <branch-name>` | Create and switch to a new branch.               | `git checkout -b feature-branch`    |
| `git merge <branch-name>`      | Merge a specified branch into the current branch.| `git merge feature-branch`           |
| `git branch -d <branch-name>`  | Delete a specified branch.                       | `git branch -d feature-branch`      |

* * *

## Stashing and Resetting Changes

| Command                          | Description                                       | Example                              |
|----------------------------------|---------------------------------------------------|--------------------------------------|
| `git stash`                      | Stash the changes in a dirty working directory.   | `git stash`                          |
| `git stash list`                | List all stashed changes.                        | `git stash list`                    |
| `git stash apply`               | Apply the latest stashed changes.                | `git stash apply`                   |
| `git stash pop`                 | Apply the latest stashed changes and remove it from the stash. | `git stash pop`           |
| `git reset <file>`              | Unstage a file.                                 | `git reset index.html`              |
| `git reset --hard`              | Reset the working directory to the last commit (discard all changes). | `git reset --hard`         |
| `git reset --soft <commit>`     | Move the HEAD pointer to a previous commit, keeping changes staged. | `git reset --soft HEAD~1`  |

---

This cheat sheet provides a quick reference for essential Git commands, covering the basics of version control, branching and merging, and how to manage changes effectively. Feel free to expand it with additional commands or explanations as you continue to work with Git!


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side