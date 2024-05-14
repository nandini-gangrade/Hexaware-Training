# Git Commands 

| Command                       | Description                                                                                              | Example Usage                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| git init                      | Initializes a new Git repository in the current directory.                                               | git init                                                 |
| git clone [repository_url]    | Clones a remote repository from the specified URL to your local machine.                                 | git clone https://github.com/example/repository.git      |
| git add [file_name]           | Adds changes in the specified file to the staging area.                                                  | git add file.txt                                         |
| git add .                     | Adds all changes in the current directory and its subdirectories to the staging area.                    | git add .                                                |
| git commit -m "[commit_message]" | Commits the staged changes with a descriptive commit message.                                           | git commit -m "Add new feature"                         |
| git status                    | Displays the current status of the repository.                                                           | git status                                               |
| git log                       | Displays a list of commits in reverse chronological order.                                               | git log                                                  |
| git branch                    | Lists all branches in the repository and indicates the current branch with an asterisk (*).              | git branch                                               |
| git branch [branch_name]      | Creates a new branch with the specified name.                                                           | git branch new-feature                                   |
| git checkout [branch_name]    | Switches to the specified branch.                                                                        | git checkout main                                        |
| git merge [branch_name]       | Merges the changes from the specified branch into the current branch.                                    | git merge new-feature                                    |
| git pull                      | Fetches changes from the remote repository and merges them into the current branch.                      | git pull origin main                                     |
| git push                      | Pushes local commits to the remote repository.                                                           | git push origin main                                     |
| git remote -v                 | Lists all remote repositories associated with the current repository along with their URLs.             | git remote -v                                            |
| git diff                      | Shows the difference between the working directory and the staging area.                                 | git diff                                                 |
| git diff --staged             | Shows the difference between the staging area and the last commit.                                       | git diff --staged                                        |
| git reset [file_name]         | Unstages changes in the specified file, keeping them in the working directory.                           | git reset file.txt                                       |
| git reset --soft [commit_hash] | Moves the HEAD to a specified commit, preserving staged and unstaged changes.                             | git reset --soft HEAD~1                                  |
| git reset --hard [commit_hash] | Resets the working directory and staging area to match the specified commit.                             | git reset --hard 1234567                                 |
| git revert [commit_hash]      | Reverts the changes introduced by a specified commit, creating a new commit to record the reversal.      | git revert 1234567                                       |
| git cherry-pick [commit_hash] | Applies the changes introduced by a specified commit onto the current branch.                             | git cherry-pick 1234567                                  |

These commands cover a wide range of Git operations, including repository initialization, cloning, staging changes, committing, branching, merging, fetching, pushing, status checks, and more. Each command plays a specific role in managing version control and collaborating on software projects.
