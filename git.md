# Git Notes
---

List all remote repositories associated with the local repository:

    git remote -v

Show how local pushes/pulls to remote:

    git remote show <name>

Delete remote branch origin/HEAD created by GitHub:

    git remote set-head origin -d

Reorder git commits:

    git rebase -i HEAD~<n>
  
    n = Number of commits from the HEAD (inclusive) to reorder

Undo failed rebase:

    git rebase --abort

Push all commits up to a given commit:

    git push <remote> <commit_hash>:<branch>

Pull remote branch onto the local without a merge commit (only if fast-forwardable):

    git pull <remote> <branch> --rebase

Set default remote upstream when pushing/ pulling

    git push -u <remote> [<branch>]

Overwrite the remote branch forcibly:

    git push -f <remote> <branch>

Pull/ merge remote conflicts in favor of the remote changes:

    git pull <remote> <branch> --strategy-option|-X theirs
	
	  git fetch <remote> <branch>
	  git merge --strategy-option|-X theirs

Show unstaged changes:

		git diff

Show staged changes:

		git diff --cached|--staged

