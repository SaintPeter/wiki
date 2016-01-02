How To Contribute To The Wiki
============================

*This guide covers how to use GitHub Desktop as well as the Git command line*

*As such there might be 2 sets of directions. Pick what you need*

## Initial: One Time Setups
 - Have a GitHub Account
 - Get Git on your computer
	 - [GitHub Desktop](https://desktop.github.com/). Also comes with Git Shell (a command line interface)
	 - Other Git clients like Git Bash
 - Go to the [Wiki Repo](https://github.com/FreeCodeCamp/wiki)
	- **CAREFUL:The Wiki is stored at a different repo than the main FCC site**
	- The above link is where you need to go
 - Click on **Fork** if you don't already have a Fork
	 - This will recreate the Wiki Repo under your username

|Vocabulary|Meaning|
|----------|-------|
|Repository| A data structure to manage a project or set of files and the changes it receives.|
|Repo| A shorter way to say Repository |
	 
 ### Cloning 
 *The following image is a reference to both sets of directions* 
 ![Grabbing the Git URL](images\How-To-Contribute-To-The-Wiki\Grabbing-The-Git-URL.PNG)
 
 #### Github Desktop Directions
 On ***your*** forked repository page, click the button that looks like a screen with an arrow. This will open GitHub Desktop to clone it automatically.
 
 If it doesn't do it automatically, you can:
 + Open GitHub Desktop yourself
 + click on the Arrow on the top
 + Select Clone
 + Pick the fork your wish to clone
 + Click on "Clone wiki"
 + Select where to clone it into
 ![GitHub Desktop Cloning](images\How-To-Contribute-To-The-Wiki\GitHub-Desktop-Cloning.PNG)
 
 
 #### Command Line Directions
`git clone <GIT Repository URL>`

example: `git clone https://github.com/CaroleAnneHannon/wiki.git`

You can grab the repository URL on your fork. The image above shows a button that will copy it to your clipboard. 

|Vocabulary|Meaning|
|----------|-------|
|Fork|A repository made from another repository|
|Clone|A local instance made from a repository|


----------

----------


## Part 1: Rebasing
The original repo will be changed over time; it's really important to **rebase** in order to keep your branch up to date


![Branch needing a rebase](http://i.imgur.com/9XE0a61.png)


### Doing a rebase
#### Command Line
***Viewing Remote Connections***

`git remote -v`

You will see *origin* which your repository

You will also most likely see *FreeCodeCamp* which should have the FreeCodeCamp/wiki.git connection. This is the original repo.
This command doesn't actually do anything other than show you what the connection names are, which is useful for the next few commands.

***Make a new branch if you need to***

`git branch <BRANCHNAME>`

example: git branch channon

***Select your branch***

`git checkout <BRANCHNAME>`

example: git checkout channon

*channon is the branch this tutorial is using*

***Rebase***
`git rebase <REMOTENAME>/<REMOTEBRANCH>`
becomes:
`git rebase FreeCodeCamp/master`

***Push from the branch in github to your local machine***
`git push <REMOTENAME> <REMOTEBRANCH>`
becomes:
`git push origin channon`

Now the branch should be up to date

![Branch that doesn't need to rebase](http://i.imgur.com/QLhmRDv.png)


#### GitHub Desktop

The Sync feature does not work well. Right click on the repo, open in Git Shell, and do the command line version as stated above.


|Vocabulary|Meaning|
|----------|-------|
|Rebase|the act of bringing down a branch to overwrite the current one|
|Push|writes the rebase to a branch|
|Commit|changes made to a repository|


----------

----------

## Part 2: Getting Ready to Edit
Get to your directory on your local machine

*Github Desktop note*
You can right click and use "Open in Explorer"
Also if you cut your directory into another location, GitHub desktop will then no longer be able to find it and ask you the new location. This makes it very easy to move to a different location.

**Understanding how the wiki works**
All of the files for the wiki are .md files. These are **markdown** files. They use [markdown language](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for the formatting of the files.

 - The Bonfire pages begin with Bonfire
 - The Waypoints pages begin with Waypoint
 - The JavaScript references pages begin with js
 - The Zipline pages begin with Zipline
 - The Basejump pages begin with Basejump
 - There are no spaces in the file names. use - instead
 - Files should be Title Cased (the first letter of each word should be capitalized)

Simply edit the file on your machine, or make a new one.

----------

----------

## Part 3: Promoting