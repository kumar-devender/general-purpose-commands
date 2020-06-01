#### Push to different account
* Generate SSH Key for new account and create a new entry of host in config like below. 
Provide path of newly generated ssh key in host IdentityFile file.
* when prompted enter `id_rsa_user1` as filename after following command 
`ssh-keygen -t rsa`
```
  Host github-personal
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_personal
```

* Add remote origin like this.
```
git remote add origin git@<Host-name-in-ssh-config-file>:<github-user-name>/hexagonal-architecture.git
```

* In case the github repository already pointing to a remote address then remove existing remote address
```
git remote rm origin
```
#### Remove undesired files from remote repository
```
git rm --cached -r .DS_Store
```

#### Amend commit message
```
git rebase -i HEAD~X
# X is the number of commits to go back
# Move to the line of your commit, change pick into edit,
# then change your commit message:
git commit --amend
# Finish the rebase with:
git rebase —continue
```
#### Amend first commit message
```
git rebase -i --root
```
#### Undo commits without losing change
```
git reset --soft HEAD~2X
```
#### Commit more files in the existing commit

#### Commit more files in the existing commit
```
git add the_left_out_file
git commit --amend --no-edit
```
#### Basic Command
```
git add .
git commit -m"any useful message"
git push -u origin <origin-name>
git checkout <branch-name>
git checkout <commit-hash>
git pull
git fetch
git merge --squash featute
git cherry-pick <commmit-hash>
git revert <commmit-hash>
git reset <commmit-hash>
git log --all --decorate --oneline --graph
```
#### Undo a Merge
* `git merge --abort`



#### Git add commit, fetch, add, pull, rebase
* `git add` selects changes, tells git to start tracking a file
* `git commit` records changes LOCALLY, commits your current changes on your local repository, creates a new revision with a log
* `git push` shares changes, pushes you local repo upstream, sends all the pending changes to the remote repository to which your branch is mapped 
  * Fetch
    * git fetch really only downloads new data from a remote repository - but it doesn't integrate any of this new data into your working files.
    * git fetch is the command that tells your local git to retrieve the latest meta-data info from the original.
  * Pull
    * Update your current HEAD branch with the latest changes from the remote server.
    * `git pull` does a `git fetch` followed by a `git merge`
    * git pull on the other hand does that AND brings (copy) those changes from the remote repository.


#### Git Rebase

```
git checkout feature
git rebase master
```
* Moves the entire feature branch to begin on the tip of the master branch, effectively incorporating all of the new commits in master
* Perfectly linear project history


