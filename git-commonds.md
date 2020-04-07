#### Push to different account
* Generate SSH Key for new account and create a new entry of host in config like below. 
Provide path of newly generated ssh key in host IdentityFile file.
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
#### Undo commits without losing change
```
git reset --soft HEAD~2X
```

#### Commit more files in the existing commit
```
git add the_left_out_file
git commit --amend --no-edit
```
