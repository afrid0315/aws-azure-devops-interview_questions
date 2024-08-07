#### 1.Git rebase vs git merge?
**Answer.** Git Rebase: Rewrites the commit history by moving or combining commits. Results in a linear history, but use with caution in shared branches.

Git Merge: Integrates changes from one branch into another, creating a merge commit. Preserves the commit history but can result in a more complex history graph.

Choose between them based on your project's needs and collaboration workflow. Use rebase for a cleaner history or merge for a more explicit record of changes.

#### 2. What is difference between git and github?
**Answer.** Git: Git is a distributed version control system (VCS) that allows users to track changes in source code during software development. It provides features for branching, merging, and collaborating on code with others.

GitHub: GitHub is a web-based platform built around Git that provides hosting for Git repositories, collaboration tools, and additional features such as issue tracking, project management, and code review. It serves as a central hub for developers to share and collaborate on code.

#### 3. How do you undo a deleted branch?
**Answer.** Certainly!

To undo a deleted branch in Git:

1. **Find the Commit**: Use `git reflog` to find the commit hash of the deleted branch.
   ```bash
   git reflog
   ```

2. **Recreate the Branch**: Use the commit hash to recreate the branch.
   ```bash
   git checkout -b <branch-name> <commit-hash>
   ```

3. **Push the Branch**: If it was a remote branch, push it back to GitHub.
   ```bash
   git push origin <branch-name>
   ```

This process restores a deleted branch by referencing its last commit, allowing you to recover it from Git's history.

#### 4. About git revert and reset commands?
**Answer.** `git revert` maintains proper history by creating a new commit that undoes changes, but the changes from the reverted commit will be undone in your files. 
In contrast, `git reset` can move the HEAD to a different commit: using `--soft` keeps all changes in the staging area without altering files, and using `--hard` moves the HEAD and discards changes in both the staging area and working directory, effectively deleting files.

#### 5. What should I do if I need to undo changes after pushing to GitHub?
**Answer.** If you need to undo changes after pushing to GitHub, use `git revert` to maintain history and avoid conflicts. First, run `git revert <commit-hash>` to create a new commit that undoes the specified commit, then push the revert commit with `git push origin <your-branch>`. If you must use `git reset`, you need to reset to the previous commit with `git reset --hard <commit-hash>` and then force push using `git push --force origin <your-branch>`. Be cautious with force-pushing as it rewrites history and can disrupt other collaborators' work.

#### Git commands?
**Answer.** git clean -df -> to clean git repositories d-directories, f-files
