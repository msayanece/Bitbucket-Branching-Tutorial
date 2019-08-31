# Bitbucket-Branching-Tutorial
Tutorial for using Bitbucket for git branching and maintain.

## Prerequisite
For understanding this tutorial, you need to know basic git commands & concepts (including setup), know how to use Bitbucket as a VCS Server. You need to have a repository in your bitbucket account (Admin) & in your local machine with master branch.

## Create new branch
* __FROM BITBUCKET__ - Go to branches from the left menu > Create branch > Enter branch name _dev_ (or anything else) > click Create-button.

## Change Branch Permission
* __BRANCH PERMISSION FOR DEV__ - Go to Bitbucket settings > Branch permissions > Add a branch permission > Under Select branch by name or pattern enter 'dev' > Write access to whoever you want to give PUSH permission (you may choose 'Everybody') > Merge via pull request to whoever you want to give PUSH permission (you may choose 'Everybody')
* __BRANCH PERMISSION FOR MASTER__ - Go to Bitbucket settings > Branch permissions > Add a branch permission > Under Select branch by name or pattern enter 'master' > Write access to only the reviewer > Merge via pull request to nobody.

## Pull Request Settings
* __DEFAULT REVIEWER__ - You may set a default reviewer who will be responsible for review a pull request.
* __DEFAULT DESCRIPTION__ - You may set a default description like below...
```
Hi,

Kindly look into these changes and review it. 


I request you to pull the changes.
```

## Fetch new remote branch to your local machine VCS
* __USING GIT GUI__ - Open the git GUI window on your local repository > Top menu 'Remote' > Fetch From > Origin. 
Then top menu Branch > Create > Enter Branch name (local) > Select Starting Revision option to 'Tracking branch' > Select the newly created branch on your remote repo (i.e. origin/dev) > Click Create-button. __Just recheck that the current branch (on the top left of the window) set to 'dev'__.
* __USING GIT BASH__ - run these command git fetch && git checkout test

## Make changes & commit
* After making some changes to your repository commit the changes. You should already know how to do that.
