#### 1.Git rebase vs git merge?
**Answer.** Git Rebase: Rewrites the commit history by moving or combining commits. Results in a linear history, but use with caution in shared branches.

Git Merge: Integrates changes from one branch into another, creating a merge commit. Preserves the commit history but can result in a more complex history graph.

Choose between them based on your project's needs and collaboration workflow. Use rebase for a cleaner history or merge for a more explicit record of changes.

#### 2. What is difference between git and github?
**Answer.** Git: Git is a distributed version control system (VCS) that allows users to track changes in source code during software development. It provides features for branching, merging, and collaborating on code with others.

GitHub: GitHub is a web-based platform built around Git that provides hosting for Git repositories, collaboration tools, and additional features such as issue tracking, project management, and code review. It serves as a central hub for developers to share and collaborate on code.

#### 3. How do you undo a deleted branch?
**Answer.** 

#### 4. About git revert and reset commands?
**Answer.** `git revert` maintains proper history by creating a new commit that undoes changes, but the changes from the reverted commit will be undone in your files. 
In contrast, `git reset` can move the HEAD to a different commit: using `--soft` keeps all changes in the staging area without altering files, and using `--hard` moves the HEAD and discards changes in both the staging area and working directory, effectively deleting files.

#### Git commands?
**Answer.** git clean -df -> to clean git repositories d-directories, f-files
