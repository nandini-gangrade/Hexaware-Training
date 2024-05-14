# Git Commands Cheat Sheet

## Basic Commands

### `git init`
- **Description**: Initializes a new Git repository in the current directory.
- **Usage**: Use this command when starting a new project to create a Git repository to track changes.
- **Example**:
  ```bash
  git init
  ```
- **Output**: 
  ```
  Initialized empty Git repository in /path/to/your/directory/.git/
  ```

### `git add .`
- **Description**: Adds all files in the current directory to the staging area.
- **Usage**: Use this command when you want to stage all changes for commit.
- **Example**:
  ```bash
  git add .
  ```
- **Output**: No output unless there's an error.

### `git reset`
- **Description**: Undoes changes and brings back files from the staging area to the Working area.
- **Usage**: Use this command to unstage files or to undo changes in the working directory.
- **Example**:
  ```bash
  git reset
  ```
- **Output**: No output unless there's an error.

### `git add <file>`
- **Description**: Adds a specific file to the staging area.
- **Usage**: Use this command when you want to stage only specific changes for commit.
- **Example**:
  ```bash
  git add index.html
  ```
- **Output**: No output unless there's an error.

### `git commit -m "<message>"`
- **Description**: Commits changes with a descriptive message.
- **Usage**: Use this command to save your changes to the Git repository along with a meaningful message.
- **Example**:
  ```bash
  git commit -m "Initial commit"
  ```
- **Output**: 
  ```
  [master (root-commit) 5737b1f] Initial commit
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 index.html
  ```

### `git status`
- **Description**: Shows the status of files in the working directory.
- **Usage**: Use this command to see which files are staged, unstaged, or untracked.
- **Example**:
  ```bash
  git status
  ```
- **Output**:
  ```
  On branch master
  Your branch is up to date with 'origin/master'.

  nothing to commit, working tree clean
  ```

## Git Stash

### `git stash`
- **Description**: Temporarily stores changes for later use.
- **Usage**: Use this command when you want to stash changes without committing them.
- **Example**:
  ```bash
  git stash
  ```
- **Output**: No output unless there's an error.

## Interactive Rebase

### `git rebase -i`
- **Description**: Interactively rebase commits.
- **Usage**: Use this command to rewrite commit history interactively.
- **Example**:
  ```bash
  git rebase -i HEAD~3
  ```
- **Output**: Opens the interactive rebase editor.

## Branching

### `git checkout <branch>`
- **Description**: Switches to a different branch.
- **Usage**: Use this command to navigate between existing branches.
- **Example**:
  ```bash
  git checkout feature-branch
  ```
- **Output**: 
  ```
  Switched to branch 'feature-branch'
  ```

### `git checkout -b <branch>`
- **Description**: Creates and switches to a new branch.
- **Usage**: Use this command to create a new branch and switch to it.
- **Example**:
  ```bash
  git checkout -b new-feature
  ```
- **Output**: 
  ```
  Switched to a new branch 'new-feature'
  ```

### `git merge <branch>`
- **Description**: Merges changes from another branch.
- **Usage**: Use this command to incorporate changes from one branch into another.
- **Example**:
  ```bash
  git merge feature-branch
  ```
- **Output**: 
  ```
  Merge made by the 'recursive' strategy.
  ```

### `git push --set-upstream origin <branch>`
- **Description**: Publishes branch to remote repository.
- **Usage**: Use this command to push a branch to a remote repository.
- **Example**:
  ```bash
  git push --set-upstream origin feature-branch
  ```
- **Output**: 
  ```
  Counting objects: 3, done.
  ```

## Git Log

### `git log`
- **Description**: Shows commit history.
- **Usage**: Use this command to view the history of commits in the repository.
- **Example**:
  ```bash
  git log
  ```
- **Output**: Displays commit history.

### `git log --author=<author>`
- **Description**: Filters commits by author.
- **Usage**: Use this command to filter commits based on the author's name or email.
- **Example**:
  ```bash
  git log --author="John Doe"
  ```
- **Output**: Displays commit history filtered by author.

### `git log -p`
- **Description**: Shows commit history with patch.
- **Usage**: Use this command to view commit history along with the diff for each commit.
- **Example**:
  ```bash
  git log -p
  ```
- **Output**: Displays commit history with diff for each commit.

### `git log -S<word> -p`
- **Description**: Searches commits for specific changes.
- **Usage**: Use this command to search commits for specific changes.
- **Example**:
  ```bash
  git log -S"bugfix"
  ```
- **Output**: Displays commits with changes related to the specified word.

### `git log -p /<word>`
- **Description**: Highlights search results in commit history.
- **Usage**: Use this command to highlight search results in commit history.
- **Example**:
  ```bash
  git log -p /bugfix
  ```
- **Output**: Displays commit history with search results highlighted.

### `git log -p <space>`
- **Description**: Pages down in commit history.
- **Usage**: Use this command to scroll down in commit history.
- **Example**:
  ```bash
  git log -p <space>
  ```
- **Output**: Scrolls down in commit history.

### `git log -p <n>`
- **Description**: Navigates to next match in commit history.
- **Usage**: Use this command to move to the next match in commit history.
- **Example**:
  ```bash
  git log -p <n>
  ```
- **Output**: Moves to the next match in commit history.

### `git log -p <N>`
- **Description**: Navigates to previous match in commit history.
- **Usage**: Use this command to move to the previous match in commit history.
- **Example**:
  ```bash
  git log -p <N>
  ```
- **Output**: Moves to the previous match in commit history.

## Undoing Changes

### `git revert <commit_id>`
- **Description**: Reverts changes introduced by a commit.
- **Usage**: Use this

 command to revert the changes introduced by a specific commit.
- **Example**:
  ```bash
  git revert <commit_id>
  ```
- **Output**: No output unless there's an error.

### `git reset --soft`
- **Description**: Undoes commit and keeps changes in staging area.
- **Usage**: Use this command to undo a commit while keeping changes staged.
- **Example**:
  ```bash
  git reset --soft HEAD~1
  ```
- **Output**: No output unless there's an error.

### `git reset --hard`
- **Description**: Undoes commit and discards all changes.
- **Usage**: Use this command to discard all changes introduced by a commit.
- **Example**:
  ```bash
  git reset --hard HEAD~1
  ```
- **Output**: No output unless there's an error.

## Cloning

### `git clone <repository_url>`
- **Description**: Clones a repository from GitHub.
- **Usage**: Use this command to create a local copy of a remote repository.
- **Example**:
  ```bash
  git clone https://github.com/username/repository.git
  ```
- **Output**: 
  ```
  Cloning into 'repository'...
  ```
