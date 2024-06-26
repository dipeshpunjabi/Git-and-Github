
## Git Commands 

### Branch Management

1. **Create and switch to a new branch:**
    ```sh
    git checkout -b feature-branch
    ```
2. **List all branches:**
    ```sh
    git branch
    ```
3. **Delete a branch:**
    ```sh
    git branch -d feature-branch
    ```
4. **Undo the last commit:**
    ```sh
    git revert HEAD
    ```
5. **Create new branches:**
    ```sh
    git checkout -b conflict-branch
    git checkout -b feature1
    ```

### Merging and Conflict Resolution

1. **Merge a branch into the main branch:**
    ```sh
    git checkout main
    git merge feature1
    ```
2. **Create a merge conflict by changing the same file and line in different branches:**
    - Make changes in `feature1` branch.
    - Switch to `conflict-branch` and make changes in the same file and line.
3. **Merge main into conflict-branch:**
    ```sh
    git checkout conflict-branch
    git merge main
    ```
    Resolve merge conflicts as necessary.

### Remote Repositories

1. **Add a remote repository:**
    ```sh
    git remote add origin git@github.com:sky-39/Jedi-test.git
    ```
2. **Fork a repository and clone it:**
    ```sh
    git clone git@github.com:sky-39/social-media.git
    ```
3. **Create a branch on your fork, make changes, and open a pull request:**
    - Create branch, make changes, commit, push to your fork, and open a PR on GitHub.

### Git Aliases and Hooks

1. **Create a Git alias for `git log --oneline`:**
    ```sh
    git config --global alias.gitlol "log --oneline"
    ```
2. **Create a pre-commit hook:**
    - Add your hook script in `.git/hooks/pre-commit`

### Stashing and Restoring Changes

1. **Stash changes to switch branches without committing:**
    ```sh
    git stash
    git checkout branch1
    git checkout branch2
    git stash apply
    ```

### Undoing Changes

1. **Restore a deleted file:**
    ```sh
    git restore <filename>
    ```
2. **Amend the last commit:**
    ```sh
    git add <file_name>
    git commit --amend --no-edit
    ```
3. **Discard all changes and revert to the last commit:**
    ```sh
    git reset --hard HEAD
    ```

### Viewing and Cherry-Picking Commits

1. **Show changes introduced by a specific commit:**
    ```sh
    git show <commit-hash>
    ```
2. **Change a commit message after committing:**
    ```sh
    git commit --amend
    ```
3. **Incorporate changes from another branch without merging:**
    ```sh
    git cherry-pick <commit-hash>
    ```

### Rebase and Squash Commits

1. **Squash several commits into a single commit before pushing:**
    ```sh
    git rebase -i master
    ```

### File Management

1. **Unstage a file:**
    ```sh
    git reset HEAD <path-to-file>
    ```
2. **Ignore specific files and directories:**
    - Add to `.gitignore`:
      ```
      *.yml
      config/
      ```

### Fetching and Rebasing

1. **Fetch latest changes without merging:**
    ```sh
    git fetch origin
    git rebase origin/main
    ```

### Branch and Commit Recovery

1. **Recover a deleted branch:**
    ```sh
    git checkout -b <branch-name> <commit-hash>
    ```

### Cleaning and Removing Files

1. **Remove untracked files and directories:**
    ```sh
    git clean -f -d
    ```

### Managing Sensitive Information

1. **Remove a commit with sensitive information from local and remote repositories:**
    ```sh
    git reset --hard <commit-id>
    git push --force
    ```

### Additional Operations

1. **Delete a remote branch:**
    ```sh
    git push origin -d <branch-name>
    ```

## Assignment

1. **Create a Git repository for all assignments and upload them:**
    - Ask peers to code review your assignments and review theirs.

2. **Create a pull request on an open-source library:**
    - Link to the pull request: [Open Source PR](https://github.com/sky-39/node/pull/new/first-open-source-akash)

## Test Project

- Link to the test project used for the assignment: [Jedi Test Project](https://github.com/sky-39/Jedi-test.git)

