# Webflyx

**Webflyx** is a hands-on practice project built to reinforce core Git concepts. It forms part of the *Git Fundamentals* module from the Boot.dev course. This repository illustrates key version control techniques such as repository setup, branching, merging, rebasing, commit management, and collaboration with remote repositories.

## Key Concepts Learned

### 1. Setup and Configuration

- Configured Git user details and global settings.
    - Verified configuration using `git config --get user.name` and `git config --get user.email`.
    - Set user information with `git config --add --global user.name "GITHUB_USERNAME"` and `git config --add --global user.email "EMAIL_ADDRESS"`.
    - Changed the default branch name locally using `git config --global init.defaultBranch master` (note: GitHub’s default branch is `main`).
- Initialized local repositories and practiced fundamental Git commands.
    - Created a repository using `git init`.
- Used `git status` to monitor repository status.
    - Files exist in three states: untracked, staged, or committed.
- Staged files using `git add <FILE_PATH>`.
- Learned that Git stores snapshots of the repository at each commit, rather than diffs.
    - Saved snapshots with `git commit -m "COMMIT_MESSAGE"`.
- Explored commit history via `git log`.
    - A repository is a sequence of commits, each representing the repository's state at a point in time.
    - Git logs include who made the commit, when, and what was changed.
- Viewing the `.git` directory’s contents directly shows raw data; using `xxd` reveals hexadecimal content.
- To inspect commit content, use `git cat-file -p <COMMIT_HASH>`.
- Git optimizes storage by storing pointers to unchanged files instead of duplicating them with each commit.

***

### 2. Branching and Merging

- A branch is a pointer to a commit.
- Display branches with `git branch` and rename branches using `git branch -m OLD_NAME NEW_NAME`.
- Created branches via:
    - `git branch BRANCH_NAME`
    - `git switch -c BRANCH_NAME`
    - `git checkout -b BRANCH_NAME`
- Created feature branches to isolate work.
- Merged branches using fast-forward and non-fast-forward merges.
    - Git finds the "best common ancestor" or "merge base."
    - Replays changes from the feature branch onto the main branch starting from the merge base.
    - Creates a new special merge commit with two parent commits.
<img width="671" height="293" alt="image" src="https://github.com/user-attachments/assets/d4820551-71b4-40a4-be73-12adc565ea33" />
- Fast-forward merges occur if the merge base equals the branch-off point, adding no new commits.

***

### 3. Rebasing

- Rebase shifts the merge base to enable fast-forward merges.
- Used to maintain a clean, linear commit history.
- Understood key differences between merging and rebasing.

***

### 4. Reset and Revert

- Practiced resetting to previous commits:
    - `git reset --soft <COMMIT>` moves HEAD but leaves staging as-is, keeping changes staged.
    - `git reset --hard <COMMIT>` resets HEAD, staging, and working directory, discarding all changes since that commit.

***

### 5. Remote Repositories and GitHub

- Differentiated local and remote repositories.
- Pushed to and pulled from remote GitHub repositories.
- Managed collaborative workflows with pull requests.

***

### 6. .gitignore Usage

- Used `.gitignore` to exclude unwanted or sensitive files from version control.


## Understanding How Git Works

- Git tracks changes made by one or more authors over time.
- Branches support parallel development lines, which can later be merged.
- A Git repository is a directory with a hidden `.git` folder containing all version control data.


## Summary

This project gave hands-on experience with Git, reinforcing best practices for effective source code management both individually and in teams.

***
