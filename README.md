# Bitbucket-Branching-Tutorial
Tutorial for using Bitbucket for git branching and maintain.

## Prerequisite
For understanding this tutorial, you need to know basic git commands & concepts (including setup), know how to use Bitbucket as a VCS Server. You need to have a repository in your bitbucket account & in your local machine with master branch.

## Create new branch
* __FROM BITBUCKET__ - Go to branches from the left menu > Create branch > Enter branch name _dev_ (or anything else) > click Create-button.

## Fetch new remote branch to your local machine VCS
* __USING GIT GUI__ - Open the git GUI window on your local repository > Top menu 'Remote' > Fetch From > Origin. 
Then top menu Branch > Create > Enter Branch name (local) > Select Starting Revision option to 'Tracking branch' > Select the newly created branch on your remote repo (i.e. origin/dev) > Click Create-button. __Just recheck that the current branch (on the top left of the window) set to 'dev'__.

* __USING GIT BASH__ - run these command git fetch && git checkout test

## Make changes & commit
* After making some changes to your repository commit the changes. You should already know how to do that.
