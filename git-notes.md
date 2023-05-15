# Git Notes

## Config 
```
git config --global alias.<name-of-alias> 'command for alias'
ex: config --global alias.undo 'reset --hard HEAD~1'

git config --list
```

## Remote Branches 
``` 
git push origin <local-branch>:<remote-branch>
git remote add
git remote #See all remotes
```

## Commits 
```
git commit --amend ...
git commit --amend --author="Jonathan Wilson <email>" # Change the author of the last commit 

git cherry-pick <commit1> <commit2> <commit3> ... --strategy-option theirs # Overwrite your local commits with remote 
```

### Squash commits 
```
c0 - the last commit in the log that was made before your changes
c1, c2, c3
git rebase -i c0
In the interactive mode change pick to squash or s. Leave the top one as pick. 
```

## Inspection 
```
git diff my-file
git diff master...<branch> # compares the changes between two branches: master and branch. The ... notation is known as the "triple-dot" syntax, and it represents a range of commits.
I will display the changes that are unique to branch since it diverged from master.

git log
```

## Security 
```
ssh-keygen -t ed25519 -C "my-name@email.com"
cat ~/.ssh/id_ed25519.pub # Paste this into your SSH keys in Github
```
