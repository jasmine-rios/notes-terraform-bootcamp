# Week 0 Notes

## "Branching Tagging PR" video

Note PR means Pull Request
### Steps to create branch 

1. Go to github terraform-beginner-bootcamp-2023 repo and click Issues
2. Create an issue and name the Issue (Add Semantic Versioning Documentation to Project.) with a description (We just want to document in the project semantic versioning.)
3. Click Submit New Issue. Once Issue is created there should be a number next to the name and that is what we will use in naming the branch.
4. Go to code and click gitpod. On terminal, enter 
> git checkout -b 1_sematic_versioning
5. Branch will be created and gitpod will be switched to that branch.
6. Now you need to push the branch:
> git push
7. You will get a fatal error saying that there is no upstream branch and to push the current branch you need to set the remote as upstream using
> git push --set-upstream origin 1_semantic_versioning
use that command and allow if a popup asks if you want to do that.
8. Go to github to the repo and click the main branch drop-down and see that the new branch was created.

### Change Read-me on Gitpod
1. On gitpod edit the readme and paste this:
> ## Semantic Versioning
2. Go to semantic Versioning 2.0 webpage @https://semver.organd copy and paste the summary (Make into list and bold certain words.)
> Given a version number **MAJOR.MINOR.PATCH**, increment the:
>
> - **MAJOR** version when you make incompatible API changes
> - **MINOR** version when you add functionality in a backward compatible manner
> - **PATCH** version when you make backward compatible bug fixes
3. Above what you posted add this
> This project is going utilize semantic versioning for its tagging.
> [Semantic Versioning](https://semver.org)
4. Before "**MAJOR.MINOR.PATCH**" put 
> The general format:
5. To the left and right of "**MAJOR.MINOR.PATCH**," remove the other words so it looks like this
> **MAJOR.MINOR.PATCH**, eg. '1.0.1'

## Preview your code 

1. Press the icon with the "book and magnifying glass" to preview your markdown.

## Git Graph

1. While in Gitpod and in the Git tab, place your mouse next to "Source Control" and select the button with three filled in dots on two lines. That is the Gitgraph button

## Push your changes

1. In the Git tab, press the plus button next to README.md to stage the changes.
2. Enter in a message under source control
> Add documentation for the sematic versioning.
3. Commit your changes by pressing commit. 
4. Click "Sync Changes" to push the commit. If that doesn't work then in terminal use this command
> git push

## Tag your Branch

1. In terminal, use this command to tag
> git tag 0.1.0
2. Use this command to push the tags
> git push --tags

## Check your tags in Github

1. Go to Github and click main to dropdown. Click the tags tab and see the new tag.

## Bring tag into Main by doing a PR

1. When in Gitgraph we notice that the tag is on the 1_semantic_versioning branch but not on the main branch. We want it on the main branch
2. Go to Github and click the Pull requests tab (Note: the Compare & Pull request button is not always reliable)

## Tag the issue

NOTE: We actually wanted to tag the issue instead

1. In gitpod README.md, Next to "## Semantic Versioning" add
> :mage:
2. Go to Git tab and add the message 
> #1 add mage to sematic versioning
3. Click commit and sync changes.
4. In Github, go to issues and the issue we opened and we should see the message referenced for the issue.

## Fix to make workflow more convient
1. Copy code for README.md and paste it in a notepad or notes
2. In github go to the issue we created, under Development click "Create a Branch", click create with ratio of locally
3. Copy the second line of code and paste it into Gitpod terminal
> git checkout 1-add-semantic-versioning-documentation-to-project
4. Go to Gitgraph and see that the branch we created is off of main but we want into the branch "1_semantic_versioning" so we will have to merge it
5. To merge the new branch we just created, in terminal use
> git merge 1_semantic_versioning
> git push

Note: Personally when running the merge command, it says "merge: 1_semantic_versioning - not something we can merge"
I had the branch named wrong so I had to rename the branch

6. Go to issue in Github and under development, we see that the branch "1-add-semantic-versioning-documentation.." is there. This is important so that others know that the branch is apart of this feature or issue and is isolate

7. In Github, go to the Code tab and click main. Click "View all branches". Delete the old branch named "1_semantic_versioning

## Tag the :mage:

1. In terminal, use
> git tag 0.1.1
2. In gitgraph we see that the tag is now added to the branch "1-add-semantic-versioning-documentation-to-project"
3. We don't see the tag in GitHub so in terminal do
> git push --tags
4. You should now see the tag in GitHub

## Create a new Pull Request

1. In Github the README.md of main, the readme is blank so we will have to do a pull request. Go to the "Pull requests" tab and click "Create pull request".
2. In the compare branch, choose "1-add-semantic-versioning-documentation-to-project" and click "create pull request" button.
3. Describe what we did in the "Leave a comment" box
> We added documentation for semantic versioning.
4. Click "Create pull request".
5. Scroll down and click the drop-down arrow next to "Create a merge commit" and choose "squash and merge" then click it. Click "Confirm squash and merge".

## Do not delete branch

In normal work, you would merge and then delete the branch but in this bootcamp, we are keeping all of our branches for validation. 
**DO NOT DELETE BRANCHES**

## See merge in Git Graph
1. In Gitpod, go to Gitgraph and see that there is a merge but we still have the branches.

## See commit messages
1. In GitHub code tab, click commits.

## Stop our Gitpod environment
If using Gitpod in browser, click the hamburger on the upper left and stop the Gitpod

If using Gitpod in VSCode, Go to the browser you opened Gitpod and click More Actions>Stop Workspace

# "Terraform CLI Refactor" video

Fix Terraform CLI Installation, understand the file ".gitpod.yml", and do some bash scripting. Code trap is introduced.

## Launch Gitpod in Github for Project Repo

## Determine what linux flavor we are using

1. In Gitpod, go to terminal and use
> cat /etc/os-release

## Code Trap
1. In the terminal there is a window named terraform:bash that would have to 

