## Workflow

1. **Working Directory:**
   - The working directory is where you edit your files and make changes to your project. These changes are not yet tracked by Git.

2. **Staging Area (Index):**
   - The staging area, also known as the index, is a middle-ground between your working directory and your Git repository. It's where you prepare changes before committing them.
   - When you're satisfied with the changes you've made to your files in the working directory and want to include them in the next commit, you use the `git add` command to stage those changes.

3. **Staging Changes:**
   - Staging changes allows you to selectively choose which modifications you want to include in the next commit. You can stage specific files or parts of files using the `git add` command with appropriate options.
   - For example:
     ```
     git add file1.txt      # Stage changes in file1.txt
     git add directory/     # Stage changes in all files within the directory
     git add -p             # Interactively stage changes, allowing you to review and select changes chunk by chunk
     ```

4. **Committing Changes:**
   - Once you've staged the changes you want to include in the next commit, you create a commit using the `git commit` command. This captures a snapshot of the staged changes and adds a commit message to describe what was done.
   - For example:
     ```
     git commit -m "Add new feature"      # Commit changes with a commit message
     git commit -am "Update documentation" # Stage all modified files and commit with a message
     ```
   - The `-m` option allows you to provide a commit message directly on the command line. If you omit this option, Git will open a text editor for you to enter a commit message.

5. **Committing Best Practices:**
   - It's good practice to make each commit focused and atomic, meaning it should represent a single logical change or set of related changes.
   - Commit messages should be descriptive, concise, and written in the imperative tense (e.g., "Add feature" instead of "Added feature").
   - Regular, well-structured commits help in understanding the history of the project and facilitate collaboration with other developers.

By following this workflow of working on changes in the working directory, staging specific modifications, and committing those changes to the repository, you can effectively manage the evolution of your project and maintain a clean and organized version history.

## Detailed explanation of how adding a feature and maintaining a linear commit graph works in Git.

1. **Starting Point:**
   - Initially, you have a clean and linear commit history with the `master` branch pointing to the latest commit.

     ```
     o---o---o  master
     ```

2. **Adding a Feature Branch:**
   - You create a new branch, say `feature`, to work on a new feature. This branch starts at the same commit as `master`.

     ```
     o---o---o  master, feature
     ```

3. **Developing the Feature:**
   - You make changes and commit them to the `feature` branch. As you progress, the `feature` branch diverges from the `master` branch.

     ```
     o---o---o  master
          \
           A---B---C  feature
     ```

4. **Rebasing the Feature Branch (Optional):**
   - To maintain a linear commit history, you can rebase the `feature` branch onto the latest commit of the `master` branch. This replays your changes on top of the latest `master` commit.

     Before Rebasing:
     ```
     o---o---o  master
          \
           A---B---C  feature
     ```

     After Rebasing:
     ```
     o---o---o  master
              \
               A'---B'---C'  feature
     ```

5. **Fast-Forward Merge:**
   - Once the feature is complete and rebased (if necessary), you merge the `feature` branch into `master`. Since there are no diverging changes, Git performs a fast-forward merge.

     ```
     o---o---o---A'---B'---C'  master, feature
     ```

6. **Linear Commit History:**
   - With the merge complete, you have a clean and linear commit history. Each commit represents a meaningful change, and the history is easy to follow.

     ```
     o---o---o---A'---B'---C'  master
     ```

By following this workflow, you ensure that your commit history remains linear and easy to understand. Rebasing feature branches onto the latest `master` commit before merging helps keep the history clean and avoids unnecessary merge commits. This approach simplifies collaboration and makes it easier to track changes over time.

----

### Sprint Cycle Workflow:

1. **Start of Sprint:**
   - Sprint begins with a planning meeting where features and tasks for the sprint are identified and assigned.
   - Developers create feature branches from the `dev` branch to work on individual features or tasks.

2. **Feature Development (2 Weeks):**
   - Developers work on their respective feature branches, implementing new features or making changes.
   - Regular code reviews, testing, and collaboration take place during the development phase.

3. **Merge to Dev (End of 2 Weeks):**
   - At the end of the two-week sprint, developers merge their feature branches into the `dev` branch.
   - Integration testing and validation of merged features occur on the `dev` branch to ensure compatibility and stability.

4. **Staging (QA) (End of 4 Weeks):**
   - After two sprints (4 weeks), the `dev` branch is merged into the `staging` branch for further testing and quality assurance (QA).
   - QA testers perform extensive testing on the `staging` branch to identify and address any issues or bugs.

5. **Master (Customer Release) (End of Month):**
   - At the end of each month, the `staging` branch is merged into the `master` branch for release to customers.
   - This represents the end of the sprint cycle, with new features and updates delivered to customers in a stable release.

### Git Branching Workflow:

- **Feature Branches:**
  - Developers create feature branches from the `dev` branch to work on specific features or tasks.
  - Each feature branch should have a clear and descriptive name, reflecting the feature being developed.

- **Dev Branch:**
  - Acts as the integration branch where individual feature branches are merged for testing and validation.
  - Developers merge their feature branches into `dev` at the end of each two-week sprint.

- **Staging Branch:**
  - Serves as the QA environment where features from the `dev` branch are thoroughly tested before release.
  - Merged with `dev` every month for a new release cycle.

- **Master Branch:**
  - Represents the production-ready codebase that is released to customers at the end of each sprint cycle.
  - Merged with `staging` at the end of each month to release new features and updates to customers.

By following this sprint cycle workflow and Git branching strategy, you can ensure a structured and organized approach to feature development, testing, and release management, while maintaining clear separation between development, testing, and production environments.
