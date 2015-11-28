# Overview
### What is a Pull Request?
A pull request (PR) is a method of submitting proposed changes to the Free Code Camp Repo (or any Repo, for that matter).  You will make changes to copies of the files which make up Free Code Camp in a personal fork, then apply to have them accepted by Free Code Camp proper.

### Methods
There are two methods of creating a Pull for Free Code Camp:

1. Editing files via the GitHub Interface
1. Editing files on a local clone

# Important: ALWAYS EDIT ON A BRANCH
Take away only one thing from this document, it should be this:  Never, EVER make edits to the `Staging` branch.  ALWAYS make a new branch BEFORE you edit files.  This is critical, becuase if your PR is not accepted, your copy of `staging` will be forever sullied and the only way to fix it is to delete your fork and re-fork.

# Editing via the GitHub Interface
**Note:** Editing via the GitHub Interface is not reccomended, since it is not possible to update your fork via GitHub's interface without deleting and recreating your fork.

1. Create a Fork of the FCC Repo
1. [Create a branch](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/) within your fork.  
Note: Branch naming is important.  
Use a name like `fix/short-fix-description` or `feature/short-feature-description`  
Review the [Contribution Guidelines](https://github.com/FreeCodeCamp/FreeCodeCamp/blob/staging/CONTRIBUTING.md) for more detail.
1. Edit the file and commit the changes.

# Editing via your Local Fork
This is the reccomended method.  Read about [How to Setup and Maintain a Local Instance of Free Code Camp](https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/How-To-Fork-And-Maintain-a-Local-Instance-of-Free-Code-Camp).

1. Perform the maintenence step of rebasing `staging`
1. Ensure you are on the `staging` branch
1. Create a branch with git:  
`git checkout -B branch/name-here`  
Note: Branch naming is important.  
Use a name like `fix/short-fix-description` or `feature/short-feature-description`  
Review the [Contribution Guidelines](https://github.com/FreeCodeCamp/FreeCodeCamp/blob/staging/CONTRIBUTING.md) for more detail.
1. Edit your file(s) locally with the editor of your choice
1. Add your edited files:  
`git add path/to/filename.ext`
1. Commit your edits:  
`git commit -m "Brief Description of Commit"`
1. [Squash your commits](https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/git-rebase#squashing-multiple-commits-into-one), if there are more than one.
1. Push your commits to your GitHub Fork:
`git push -u origin branch/name-here`

# Common Steps

1. Once the edits have been committed, you will be prompted to create a pull request on your fork's Github Page.
1. By default, all pull requests should be againt the FCC main repo, `staging` branch.
1. Make a clear title for your PR which sucinctly indicates what is being fixed.  Do not add the issue number in the title.  
Examples:  
`Add Test Cases to Bonfire Drop It`
`Correct typo in Waypoint Size Your Images`
1. In the body of your PR include a more detailed summary of the changes you made and why.
1. Indicate if you have tested on a local copy of the site or not.
1. If your PR is due to an issue, you can [reference and close that issue](https://help.github.com/articles/closing-issues-via-commit-messages/) automatically by adding a keyword like `Closes #xxxx`, where `xxxx` is the issue number.

# Next Steps
### If Changes are Requested
Don't worry, many PRs, especially first PRs, require correction or updating.  If you have used the GitHub interface to create your PR, you will need to close your PR, create a new branch, and re-submit.  This is because you cannot squash your commits via the GitHub interface.

If you have a local copy of the repo, you can make the requested changes and amend your commit with:  
`git commit --amend`  
This will update your existing commit.  When you push it to your fork you will need to do a force push to overwrite your old commit:  
`git push --force`

Be sure to post in the PR conversation that you have made the requested changes.

### If your PR is accepted
Once your PR is accpted, you may delete the branch you created to submit it.  This keeps your working fork clean.  You can do this with a press of a button on the GitHub PR interface.
You can delete the local copy of the branch with:
`git branch -D branch/to-delete-name`

### If your PR is rejected
Don't dispair!  You should recieve solid feedback from the Issue Moderators as to why it was rejected and what is needed.  Please, keep contributing.
