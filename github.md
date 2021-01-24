Instead of traditional “undo” systems, Git has its own system with completely different terminology, which includes such terms like git clean, git rm, git reset and so on. Each of these commands has specific functions and is used for undoing changes on the local and public repositories.

#Reviewing old commits
Undoing a committed snapshot

The git checkout command will checkout the previous commit, b235bf4, putting the repository in a state before the improvements commit happens. As a result of checking, the repository state will be "detached HEAD". Being in a detached state means that each new commit made will be orphaned when branches are switched back to an established branch. Orphaned commits are prepared for being deleted by Git garbage collector that runs on a configured interval permanently destroying orphaned commits. For avoiding this,make sure that you are on a branch. From the detached HEAD state of the repo, you can invoke git checkout -b new_branch_without_improvement_commit . Consequently, you will have a new branch named new_branch_without_improvement_commit and switch to that state. Now we have a new history timeline without the 234be24 commit. At this stage, when we no longer have the 234be24 commit, we can look at some undoing strategies.


For avoiding this,make sure that you are on a branch. From the detached HEAD state of the repo, you can invoke git checkout -b new_branch_without_improvement_commit . Consequently, you will have a new branch named new_branch_without_improvement_commit and switch to that state. Now we have a new history timeline without the 234be24 commit. At this stage, when we no longer have the 234be24 commit, we can look at some undoing strategies.
