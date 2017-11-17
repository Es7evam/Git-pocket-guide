# Forks guide
Almost everything about forks, including how to use, some conventions and good programming practices.
 
## Getting Started

Forks are copies of repositories that you save on your own github. Forking allows you to change the project without affecting the original one.
Also they allow you to make changes in a project that isn't yours and then submitting a *pull request*.

### Creating and configuring new forks
In order to fork a repo, it is easier to go to github website and then click at the fork button, top right on the page.
You'll be redirected to your copy of the project, which you can clone as usual using ``git clone link``

After that, you must configure the fork so you can push and pull from both your fork and the original one.
First, you may type
```
git remote -v
```
and check if the output is something like:
```
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
``` 
So, in order to set the original repository as an upstream, you must use the following command:
```git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git```

If you want to check if everything went smooth, you may use ``git remote -v`` again and the output should be something like
```
git remote -v
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```


### Syncing and using forks
In the current working directory to your local project, in order to sync the local repo with the original remote one, this way the changes at the master branch will be pulled from the repo.
Then you must merge it with your local one, as the following commands:
```
git fetch upstream
git merge upstream/master
```
If there are no conflicts they will be merged.
If you want to fetch all the branches at once, you may use ``git fetch --all``.

Don't forget that if you want to push or pull the changes from a repo you must now specify which one you want, using, for example, if you want to push changes at the original repo and at the branch master:
```
git push upstream master
```

So, here follows a table with the commands commented until now
Command | Function
:-------------------- | -----------------------
git remote -v     | List remotes.
git remote add upstream OriginalLink| Adds the original repo as an "upstream" remote.
git fetch | Download objects and refs from another repo.

### Pull requests
Pull requests are, as the name implies, a request that a project accept changes you have made to its code, including them into it.
In order to make pull requests, the simplest way is to navigate into *New pull request* at the left hand side of the page on your fork at github and then selecting the branch you want to make the pull request from.
It isn't possible to send pull requests natively through command line, but you can check [this repo](https://github.com/jd/git-pull-request) that enables you to do so.

## Some external official links
- [configuring a remote fork](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
- [syncing a fork](https://help.github.com/articles/syncing-a-fork/#platform-linux)
- [git fetch documentation](https://git-scm.com/docs/git-fetch)

