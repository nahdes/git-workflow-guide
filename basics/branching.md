# Git Branching Commands

This is a quick reference for common Git branching commands.

| Command                                  | Description                                                          |
| ---------------------------------------- | -------------------------------------------------------------------- |
| `git branch`                             | List all local branches. Use `-r` for remote branches, `-a` for all. |
| `git branch <branch-name>`               | Create a new branch from the current commit.                         |
| `git checkout <branch-name>`             | Switch to an existing branch.                                        |
| `git checkout -b <branch-name>`          | Create a new branch and switch to it immediately.                    |
| `git branch -d <branch-name>`            | Delete a local branch (use `-D` to force delete unmerged branches).  |
| `git branch -m <old-name> <new-name>`    | Rename a branch.                                                     |
| `git merge <branch-name>`                | Merge the specified branch into the current branch.                  |
| `git push origin <branch-name>`          | Push a local branch to the remote repository.                        |
| `git push origin --delete <branch-name>` | Delete a remote branch.                                              |
| `git fetch`                              | Update remote branch information without merging.                    |
| `git pull origin <branch-name>`          | Fetch and merge changes from a remote branch.                        |
