# Branches guide
Almost everything about branches, including how to use, some conventions and good programming practices.
 
## Getting Started

All projects come with the master branch already created. It is usually used cleanly and you must do the "dirty work" in another branch and then use pull requests

### Creating and pushing new branches

Command | Function
:-------------------- | -----------------------
git branch nameOfBranch     | Create new branch with the given name.
git checkout nameOfBranch	| Set the current working branch as this one.
git push origin nameOfBranch| Pushes the branch to remote repo.
git branch 					| List all branches. * represents the current one.
git push --all 				| Pushes all the branches to remote repo.

### Merging branches

After you finish implementing the funcionalities and using the git as you'd normally use, you'll need to merge the current branch (currBranch) with the another one (anotherBranch)
For that, you'll need to do the following:

```
git checkout anotherBranch
git merge origin currBranch
git push 
```

### Conventions when working with branches.
In case you're working in a big team, remember that commits are atomic. So check  ``git status`` before you commit.
Remember as well to pull changes from git when starting to work, in order to avoid overwrites at codes.