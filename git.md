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

#### Basic Git Scenarios (Source: Linkedin)

1. You accidentally committed sensitive credentials in Git. How do you remove them from history?

2. How do you undo your last commit without losing your changes?

3. You need to discard local changes in a specific file. How would you do it?

4. What happens if you run git reset --hard HEAD~1?

5. How can you recover a deleted branch?

6. You accidentally committed changes to the wrong branch. How do you move them to the correct branch?

7. How do you revert a specific commit without affecting other changes?

8. You cloned a repository but forgot to specify --recurse-submodules. How do you initialize submodules afterward?


Branching & Merging Scenarios

9. How do you rebase a feature branch onto the main branch?

10. What is the difference between git merge and git rebase? When would you use each?

11. A merge conflict occurs while merging a feature branch into main. How do you resolve it?

12. You want to merge only a specific commit from another branch. How do you do that?

13. How do you delete a remote branch that is no longer needed?

14. Your main branch is ahead of your local branch. How do you update your branch without affecting your commits?

15. What happens if you try to merge a branch that has already been merged?


Remote Repository & Collaboration Scenarios

16. Your team is working on the same file, and a colleague has already pushed changes. How do you avoid overwriting their work?

17. You made some local commits but need to push them to a remote branch with a different name. How do you do that?

18. How do you force push a commit while ensuring you don't overwrite other team members' work?

19. A team member deleted a remote branch. How can you recover it if you still have it locally?

20. You need to contribute to an open-source project. What steps will you take to fork and create a pull request?

21. How do you revert a pushed commit that is causing issues in production?

Advanced Git Scenarios

22. You need to squash multiple commits into one before pushing. How do you do that?

23. How do you rewrite commit history to change a commit message from a few commits ago?

24. Explain how git cherry-pick works and when you would use it.

25. How do you create and apply patches in Git?

26. You have diverged from the remote branch, and your local commits conflict with remote changes. How do you fix this?

27. You need to find out who made changes to a specific line in a file. What command do you use?

28. How do you temporarily save changes that are not ready to be committed?

29. Your Git repository has become very large. How do you reduce its size without affecting its history?

30. Explain the difference between git revert and git reset. When would you use each?

31. What is git blame?
