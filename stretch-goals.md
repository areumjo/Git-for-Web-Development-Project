## Strech goals 
### Git commands

* [ ] `git merge 'other-branch'`:
    * It is used to merge any changes on `'other-branch'` to currently checkout branch
    * Two types of merge
        * 1) Fast-forward merge; a branch being merged in must be ahead of the checked out branch
        * 2) Regular type of merge; two divergent branches are combined and merge commit is created

* [ ] `merge conflict` is happened when the exact same lines are changed in separate branches
    * How to solve `merge conflict`
        * Locate to local repository that has the `merge conflict` 
        * List up the files using `git status`
        * Determin what to keep/remove, modify files and make a commit

* [ ] `git pull`:
    * It is used to get copy to the local repository from the remote branch
        * The local tracking branch (origin/master) is moved to point to the most recent commit
        * The local tracking branch (origin/master) is merged into the local branch (master)

* [ ] `git rebase`:
    * It is used to squash the last few commits into one commit,
    so new SHA for the commit is made.
    * For example, `git rebase -i HEAD~3` squash 3 last commits into new one.
        * `-i` ; "interactive'
        * `HEAD` ; point current location
        * `HEAD~1` ; 1 before HEAD (last 2 commits)
        * `HEAD~2` ; 2 before HEAD
    * Before apply this commit, make a backup branch in order to prevent from deleting.
        * Useful lags
            * `-p` or pick; to keep the commit as is
            * `-r` or reword; to keep the commit's content but alter the commit message
            * `-e` or edit; to keep the commit's content but stop before committing so  you can:
            * `-s` or squash; to combine this commit's changes into the previous commit (the commit above it in the list)
            * `-f` or fixup; to combine this commit's change into the previous one but drop the commit message
            * `-x` or exec; to run a shell command
            * `-d` or drop; to delete the commit


* [ ] `git reset`:
    * It is used to erase commits and move the current branch point to the referenced commit
        * `--soft`; moves committed changes to the staging index
        * `--mixed`; affect unstages committed changes
        * `--hard`; erase any changes in the files


* [ ] `git revert`:
    * It is used to undo the changes that were made by the commit and creates a new commit to record the change
        * `git revert 'SHA'` ; it takes a specified commit with the 'SHA' and inverse the changes.
        * The local tracking branch will be updated to the point at the new commit.

* [ ] `git clean`:
    * It is used to remove untracked files which mean didn't get staged or get added to the git 
        * `-d`; remove untracked 'directories' as well as untracked files
        * `-f` or force; delete untracked files unless the clean.requireForce is set to false
    * `git clean` can remove untracked files while `git rest` and `git revert` operate on tracked files (added to the Git)


### Graphical User Interface (GUI)
* [ ] Visualized tools to easy to browsing and committing
* [ ] Check out this link https://git-scm.com/downloads/guis

### SSH key
* [ ] Use: Generatoe SSH keys with Github, so that you do not need to input username/password everytime you push to the remote (GitHub)
    * `ssh-keygen -t rsa -b 4097 'email-address'`