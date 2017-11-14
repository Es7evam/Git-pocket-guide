# Initial configuration and repository creation guide
Small guide on how to initially setup your git account, start, clone and use repositories.
 
## Initial configurations

In order to start working with git through command line, you must first set the global configs in your computer.

Set the name you want atached to your commit transactions:
```
git config --global user.name YourUsername
```

Set the email you want attached to your commit transactions:
```
git config --global user.email YourEmail
```

Enables helpful colorizationof command line output (optional):
```
git config --global color.ui auto
```

### Creating new repositories
As you probably saw at the root of this repository, git repos contain a README.md and a LICENSE file. 
In case you're interested in learning about README.md formatting check the root guide of this repo and if you want to learn about LICENSE files check [this link](https://help.github.com/articles/licensing-a-repository/)

Command | Function
:-------------------- | -----------------------
git init nameOfRepo     | Create new repository with specified name 
git clone urlOfRepo	| Downloads completely the repository of specified url

### Making changes at repository
Usually file changes at git are atomic, that is, for every change in a functionality that you do, you commit once. Do not let it pile.
Commits descriptions are made in infinitive verb form, for example "Add file X", not in the past (Added, in this case, is wrong).
At the end of commits the punctuation is not used, since they must be descriptive and you don't have lots of characters this is a convention.

Command | Function
:-------------------- | -----------------------
git status | Lists all new or modified files to be committed
git add FileName | Snapshots the file in preparation for versioning
git mv FileName NewName | Renames file at local repo and versioning.
git reset FileName | Unstages the file, but preserve its contents
git diff | Shows file differences between added files and remote ones
git diff --staged | Shows file differences between staging and the last file version.

### Commiting, pushing and pulling into repository
As commented above, it is commits are atomic and for them to be available for other contributors and users of the project, you must push the changes into the remote repository so they can access it.
It is usual as well to pull changes from the remote repo when starting to work, in this way you can avoid conflicts easier (see [branches](https://github.com/Es7evam/Git-pocket-guide/tree/master/branches) for more information about this).

Command | Function
:-------------------- | -----------------------
git commit -m "Descriptive message about commit" | Records file snapshots permanently in version history
git push | Pushes current branch into remote repository.
git pull | Pulls branch from remote repository.
