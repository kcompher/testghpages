### What's a fork, and when should i use one?
A fork is a copy of a Git repository "connected" with the project you forked from (upstream). When you collaborate on code, it's pretty common forking a project, cloning to your local machine, making the changes you're up to, pushing to your fork, and submitting a merge request (MR) to merge your code into the original project.

You fork a repository whenever you want to contribute to a project which you don't have access to, as it's not your own or your team's. This is how open source projects hosted by GitLab get so much collaboration from the community.

While the process of merging branches into master within the same repo is called a ``merge request``, the process of pushing changes upstream between a forked and upstream repo is called submitting a ``pull request.``

##### How to sync a fork
Say the repo upstream has updated its master, and your fork is now out of date, and you want your update your fork's branches. 

###### from command line
- Change the current working directory to your local project. Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.

	```
	git fetch upstream
``` 

- Check out your fork's local master branch.

	```
	git checkout master
```

- Merge the changes from upstream/master into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes. 

	```
	git merge upstream/master 
``` 

###### from Gitlab

https://about.gitlab.com/2016/12/01/how-to-keep-your-fork-up-to-date-with-its-origin/

GitLab can do that for you with no pain! Yay! What you need to do is very simple: enable GitLab Repository Mirroring!

First. Mirror your fork:

Under your forked project's Settings, navigate to Mirror Repository:
