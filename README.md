# Bitbucket-Branching-Tutorial
Tutorial for using Bitbucket for git branching and maintain.

## Prerequisite
For understanding this tutorial, you need to know basic git commands & concepts (including setup), know how to use Bitbucket as a VCS Server. You need to have a repository in your bitbucket account (Admin) & in your local machine with master branch.

## REPOSITORY SETUP
This is a one time setup process...

### STEP 1 - Create new branch
* __FROM BITBUCKET__ - 
1. Go to branches from the left menu 
2. Create branch 
3. Enter branch name _dev_ (or anything else) 
4. click Create-button.

### STEP 2 - Change Branch Permission
* __BRANCH PERMISSION FOR DEV__ - 
1. Go to Bitbucket settings 
2. Branch permissions 
3. Add a branch permission 
4. Under Select branch by name or pattern enter 'dev' 
5. Write access to whoever you want to give PUSH permission (you may choose 'Everybody') 
6. Merge via pull request to whoever you want to give PUSH permission (you may choose 'Everybody')
* __BRANCH PERMISSION FOR MASTER__ - 
1. Go to Bitbucket settings 
2. Branch permissions 
3. Add a branch permission 
4. Under Select branch by name or pattern enter 'master' 
5. Write access to only the reviewer 
6. Merge via pull request to nobody.

### STEP 3 - Pull Request Settings
* __DEFAULT REVIEWER__ - You may set a default reviewer who will be responsible for review a pull request.
* __DEFAULT DESCRIPTION__ - You may set a default description like below...
```
Hi,

Kindly look into these changes and review it. 


I request you to pull the changes.
```

### STEP 4 - Fetch new remote branch to your local machine VCS
* __USING GIT GUI__ - 
1. Open the git GUI window on your local repository 
2. Top menu 'Remote' 
3. Fetch From 
4. Origin. 

5. Then top menu Branch 
6. Create 
7. Enter Branch name (local) 
8. Select Starting Revision option to 'Tracking branch' 
9. Select the newly created branch on your remote repo (i.e. origin/dev) 
10. Click Create-button. __Just recheck that the current branch (on the top left of the window) set to 'dev'__.
* __USING GIT BASH__ - run these command 
```
git fetch && git checkout test
```

## GENERAL COMMIT-UPDATE-PUSH-PULL_REQUEST-MERGE
This is repetitive process. ___You should be always checked out the branch 'dev' in your local machine.___ For every changes you have made in your repository, the below process need to be maintained by a developer... 

### STEP 1 - Make changes & commit
* After making some changes to your repository, add the files to staged changes and then commit the changes with commit message. You should already know how to do that.

### STEP 2 - Update (Pull) remote changes to your local
* After a successful commit, pull or update the remote (Bitbucket) changes to your local machine. You should already know how to do that. But if you are new please follow the below process...

* __GIT BASH__ - Use the below command in your git bash...
```
git pull origin dev
```
* __GIT GUI__ - 
1. First check your current branch _'dev'_ is selected 
2. Go to 'Tools' on your top menu bar 
3. Add.. 
4. Under Name write Pull or Update (this will be the tool name) 
5. Under Command write _'git pull origin dev'_ 
6. make sure that the last checkbox named 'Add globally' is unchecked (It should not be checked as it will add the tool menu for all your repos) 
7. At last, click on the 'Add' button.
* __PHP STORM__ - 
1. (make sure that the dev branch is selected on the below right corner of your IDE) 
2. Press CTRL + T 
3. Click OK.

### STEP 3 - Push your commit to the Bitbucket server
* After a successful update, push your commit/s to the remote server. You should already know how to do that.

### STEP 4 - Pull request the new dev commits
* After a successful push to your Bitbucket server, you should be able to see the new commits in your dev branch of Bitbucker server.
1. Click on the _'Pull requests'_ from the left menu on your Bitbucket website. 
2. Create a pull request 
3. Carefully observe the arrow (From left to right) > in the left side the ___'dev'___ branch must be selected 
4. And in the right side the ___'master'___ branch must be selected. 
5. Under title write the pull request title (should be meaningful) 
6. The description should be already populated by your defauld settings 
7. Under Reviewers select the person who will be responsible to review the code changes & resolve the conflits (If you set your default reviewer earlier, it should be autopopulated) 
8. Click on 'Create pull request' button.

### STEP 5 - Make changes & commit
* After making some changes to your repository commit the changes. You should already know how to do that.



















