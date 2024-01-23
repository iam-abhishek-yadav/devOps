
# Git Learning Concepts

## Basic Concepts

- **Git:**
  - Fast, distributed revision control system with a rich command set.
  
- **Repository:**
  - *Definition:* `.git/` folder tracking changes, local or remote.
  - *Key Concepts:* Local and remote repositories.

- **Clone:**
  - *Definition:* Create a local copy of a repository.
  - *Command:* `git clone [repository URL]`.

- **Commit:**
  - *Definition:* Snapshot of project changes.
  - *Commands:* `git add [file]`, `git commit -m "Message"`.

- **Branch:**
  - *Definition:* Parallel development line.
  - *Commands:* `git branch`, `git branch [branch_name]`, `git checkout [branch_name]`.

- **Merge:**
  - *Definition:* Combine changes from different branches.
  - *Command:* `git merge [branch_name]`.

- **Pull and Push:**
  - *Pull:* Fetch and integrate changes.
  - *Push:* Upload local commits.
  - *Commands:* `git pull origin [branch_name]`, `git push origin [branch_name]`.

- **Remote:**
  - *Definition:* Version of repository on another server.
  - *Commands:* `git remote -v`, `git remote add [remote_name] [remote_URL]`.

## Intermediate Concepts

- **Pull Request (PR):**
  - Proposed changes for review and merge.

- **Resolve Conflicts:**
  - Manual conflict resolution.

- **Tagging:**
  - Reference specific points in history.

- **Stash:**
  - Temporarily save changes.

## Advanced Git Concepts

### Rebase

- **Definition:**
  - Git command to modify commit history by incorporating changes from one branch into another.

- **Key Concept:**
  - Creates a linear history by moving, combining, or squashing commits, maintaining a cleaner and more organized history.

- **Use Case:**
  - Useful for maintaining a clean and organized commit history, especially in long-running feature branches.

### Cherry-Pick

- **Definition:**
  - Git command to select specific commits from one branch and apply them to another branch.

- **Key Concept:**
  - Enables the selective application of changes without merging entire branches, providing flexibility in incorporating specific features or fixes.

- **Use Case:**
  - Useful when you want to include specific changes from one branch into another without merging the entire branch.

### Hooks

- **Definition:**
  - Scripts that run automatically at different points in the Git workflow.

- **Key Concept:**
  - Allow customization and automation of actions, triggering scripts before or after specific Git events like committing, pushing, or merging.

- **Use Case:**
  - Enforce code style, run tests, or perform additional checks automatically as part of the Git workflow.

### Submodules

- **Definition:**
  - Repositories embedded within another repository.

- **Key Concept:**
  - Enable the inclusion of external repositories as part of a project, maintaining a connection to a specific version of an external project.

- **Use Case:**
  - Useful for managing dependencies or incorporating shared code from external repositories while keeping them separate and versioned.

### Git Workflows

- **Definition:**
  - Established patterns of collaboration and version control practices.

- **Key Concept:**
  - Different workflows define how developers collaborate, manage branches, and release software using Git. Examples include Gitflow and GitHub flow.

- **Use Case:**
  - Choosing an appropriate workflow helps organize and streamline the development process, providing a structured approach to collaboration.
