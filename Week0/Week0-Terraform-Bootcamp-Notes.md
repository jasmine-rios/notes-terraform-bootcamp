# Week 0 Notes

## "Branching Tagging PR" video

Note PR means Pull Request
### Steps to create branch 

1. Go to "github terraform-beginner-bootcamp-2023" repo and click Issues

2. Create an issue and name the Issue (Add Semantic Versioning Documentation to Project.) with a description (We just want to document in the project semantic versioning.)

3. Click Submit New Issue. Once Issue is created there should be a number next to the name and that is what we will use in naming the branch.

4. Go to code and click gitpod. On terminal, enter 

`git checkout -b 1_sematic_versioning`

5. Branch will be created and gitpod will be switched to that branch.

6. Now you need to push the branch:

`git push`

7. You will get a fatal error saying that there is no upstream branch and to push the current branch you need to set the remote as upstream using

`git push --set-upstream origin 1_semantic_versioning`

use that command and allow if a popup asks if you want to do that.

8. Go to github to the repo and click the main branch drop-down and see that the new branch was created.

### Change Read-me on Gitpod

1. On gitpod edit the readme and paste this:

`## Semantic Versioning`

2. Go to semantic Versioning 2.0 webpage @https://semver.org and copy and paste the summary (Make into list and bold certain words.)`

`Given a version number **MAJOR.MINOR.PATCH**, increment the:`

` - **MAJOR** version when you make incompatible API changes`

`- **MINOR** version when you add functionality in a backward compatible manner`

`- **PATCH** version when you make backward compatible bug fixes`

3. Above what you posted add this

`This project is going utilize semantic versioning for its tagging.`

`[Semantic Versioning](https://semver.org)`

4. Before "**MAJOR.MINOR.PATCH**" put 

`The general format:`

5. To the left and right of "**MAJOR.MINOR.PATCH**," remove the other words so it looks like this

`**MAJOR.MINOR.PATCH**, eg. '1.0.1'`

### Preview your code 

1. Press the icon with the "book and magnifying glass" to preview your markdown.

### Git Graph

1. While in Gitpod and in the Git tab, place your mouse next to "Source Control" and select the button with three filled in dots on two lines. That is the Gitgraph button

### Push your changes

1. In the Git tab, press the plus button next to README.md to stage the changes.

2. Enter in a message under source control
> Add documentation for the sematic versioning.

3. Commit your changes by pressing commit. 

4. Click "Sync Changes" to push the commit. If that doesn't work then in terminal use this command

`git push`

### Tag your Branch

1. In terminal, use this command to tag

`git tag 0.1.0`

2. Use this command to push the tags

`git push --tags`

### Check your tags in Github

1. Go to Github and click main to dropdown. Click the tags tab and see the new tag.

### Bring tag into Main by doing a PR

1. When in Gitgraph we notice that the tag is on the 1_semantic_versioning branch but not on the main branch. We want it on the main branch

2. Go to Github and click the Pull requests tab (Note: the Compare & Pull request button is not always reliable)

### Tag the issue

NOTE: We actually wanted to tag the issue instead

1. In gitpod README.md, Next to "## Semantic Versioning" add

`:mage:`

2. Go to Git tab and add the message 
> #1 add mage to sematic versioning

3. Click commit and sync changes.

4. In Github, go to issues and the issue we opened and we should see the message referenced for the issue.

### Fix to make workflow more convient

1. Copy code for README.md and paste it in a notepad or notes

2. In github go to the issue we created, under Development click "Create a Branch", click create with ratio of locally

3. Copy the second line of code and paste it into Gitpod terminal

`git checkout 1-add-semantic-versioning-documentation-to-project`

4. Go to Gitgraph and see that the branch we created is off of main but we want into the branch "1_semantic_versioning" so we will have to merge it

5. To merge the new branch we just created, in terminal use

`git merge 1_semantic_versioning`

`git push`

Note: Personally when running the merge command, it says "merge: 1_semantic_versioning - not something we can merge"

I had the branch named wrong so I had to rename the branch

6. Go to issue in Github and under development, we see that the branch "1-add-semantic-versioning-documentation.." is there. This is important so that others know that the branch is apart of this feature or issue and is isolate

7. In Github, go to the Code tab and click main. Click "View all branches". Delete the old branch named "1_semantic_versioning

### Tag the :mage:

1. In terminal, use

`git tag 0.1.1`

2. In gitgraph we see that the tag is now added to the branch "1-add-semantic-versioning-documentation-to-project"

3. We don't see the tag in GitHub so in terminal do

`git push --tags`

4. You should now see the tag in GitHub

### Create a new Pull Request

1. In Github the README.md of main, the readme is blank so we will have to do a pull request. Go to the "Pull requests" tab and click "Create pull request".

2. In the compare branch, choose "1-add-semantic-versioning-documentation-to-project" and click "create pull request" button.

3. Describe what we did in the "Leave a comment" box
> We added documentation for semantic versioning.

4. Click "Create pull request".

5. Scroll down and click the drop-down arrow next to "Create a merge commit" and choose "squash and merge" then click it. Click "Confirm squash and merge".

### Do not delete branch

In normal work, you would merge and then delete the branch but in this bootcamp, we are keeping all of our branches for validation. 

**DO NOT DELETE BRANCHES**

### See merge in Git Graph

1. In Gitpod, go to Gitgraph and see that there is a merge but we still have the branches.

### See commit messages

1. In GitHub code tab, click commits.

### Stop our Gitpod environment

If using Gitpod in browser, click the hamburger on the upper left and stop the Gitpod

If using Gitpod in VSCode, Go to the browser you opened Gitpod and click More Actions>Stop Workspace

## "Terraform CLI Refactor" video

Fix Terraform CLI Installation, understand the file ".gitpod.yml", and do some bash scripting. Code trap is introduced.

### Launch Gitpod in Github for Project Repo

### Determine what linux flavor we are using

1. In Gitpod, go to terminal and use

`cat /etc/os-release`

### Code Trap

In the terminal there is a window named terraform:bash that would have to press enter to continue, it is not automated.

### Stop Gitpod and Create feature branch

1. Stop Gitpod. In GitHub, create a new issue. Name the issue 
> Refactor Terraform CLI

2. Leave a comment 
> There is an issue with installing the Terraform CLI.
> We need to go and make sure it automates without user input.

3. Label the issue with the "bug" label.

4. "Submit new issue"

5. Label last issue as "Documentation

6. Go to Refactor Terraform CLI issue and edit the comment to say
> There is an issue with installing the Terraform CLI.
> We need to go and make sure it automatically installs to completion without user input.

7. From the new issue, click create a branch and click "create branch" from popup.

8. Go to the code tab and choose the new branch from the branch dropdown. Click Gitpod and start the Gitpod for the new branch.

### Fix the .gitpod.yml terraform

1. In Gitpod, go to the explorer tab and open the .gitpod.yml file.

2. Run each code in the init for terraform in the terminal line by line.

3. In running the curl command to get the package, the error occurs

```bash
$ curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -

Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
OK
```
But maybe it's not the issue

4. In running the sudo apt-add-repo command, It asks to hit enter. Add -y at the end of the command to assume yes to all queries and run it again in termninal. 
It works but says

```bash
https://apt.releases.hashicorp.com/dists/jammy/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
```

5. Since things are looking deprecated, check the Terraform Installation Guide to see if things changed in a browser.
[Terraform Install Linux] (https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
Navigate to the linux tab as it will have the most up to date.

6. In Gitpod, create a folder named "bin" in the repo and create a new file called install_terraform_cli. In that file, copy and paste the instructions to install Teraform on Ubuntu/Debian

> sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
>
> wget -O- https://apt.releases.hashicorp.com/gpg | \
> gpg --dearmor | \
> sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
>
> gpg --no-default-keyring \
> --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
> --fingerprint
>
> echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
> https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
> sudo tee /etc/apt/sources.list.d/hashicorp.list
>
> sudo apt update
>
> sudo apt-get install terraform

7. Run the install_terraform_cli line by line in the terminal to what kind of output we are looking for.

8. Run the sudo apt-get command, you can add curl at the end. Everything is good.

9. When running the wget command the backslashes that mean it's a line don't paste that easy. You can remove them. 
You will get a bunch of nonsense that's okay because it just puts it in a file called /usr/share/keyrings/hashicorp-archive-keyring.gpg

10. When running the gpg command, it has --no-default-keyring and that might fix our depricated issue and it does. 

11. Running the echo command and sudo apt update works.

12. Before running the last command you can add "-y" to automate 
apt-get, then run it. It turns out good.

NOTE: You can rename "install_terraform_cli" to have ".sh" at the end to make it a bash script and run that but we are going to make this an executable with a shebang.

13. At the top of the script, put a shebang for ubuntu.
> #!/usr/bin/env bash 

14. Now you can run the script, go to terminal and use
> source ./bin/install_terraform_cli
Running the command above without source is not allowed, because it's not an executable.
In order to make executable, you will have to change the linux file permissions

15. Edit the readme to have the resources we used.
> https://www.cyberciti.biz/faq/how-to-check-os-version-in-linux-command-line/
> https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli
> https://en.wikipedia.org/wiki/Shebang_(Unix)
> https://en.wikipedia.org/wiki/Chmod

16. Go to terminal and run this to see our permissions for the install_terraform_cli file
> ls -al ./bin
she that there is no x in the permisions so we need to change the user portion to have that.

17. Use the chmod to change the file to be executable for user
> chmod u+x ./bin/install_terraform_cli
check if permisions took with ls -al

18. Run the file without source and it should run now.

### Use the executable for .gitpod.yml

1. In .gitpod.yml, erase the lines for terraform init and add 
> source ./bin/install_terraform_cli

2. According to the Gitpod documentation on tasks, the init only runs when a new workspace is created. So we would have to change the init to before. (add that resource to the README.md)
> https://www.gitpod.io/docs/configure/workspaces/tasks#tasks

### Make sure it's fixed.

1. Edit the README.md to show what the links we pasted are about and document the changes we made so later we know when explaining why we did it.
> ### Install the Terraform CLI
> ### Considerations with the Terraform CLI changes
>The Terraform CLI instructions have changed due to gpg keyring changes. So we needed to refer to the latest install CLI instructions via Terraform Documentation and change the scripting for install
>
>[Install Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) 
>
> ### Considerations for Linux Distribution
>
> This project is build against Ubuntu.
> Please consider checking your Linux Distribution and change accordingly to distribution needs.
> 
> [How to Check OS Version in Linux](https://www.cyberciti.biz/faq/> how-to-check-os-version-in-linux-command-line/)
> 
> Example of checking OS Version:
> 
> ```
> $ cat /etc/os-release
>
> PRETTY_NAME="Ubuntu 22.04.3 LTS"
> NAME="Ubuntu"
> VERSION_ID="22.04"
> VERSION="22.04.3 LTS (Jammy Jellyfish)"
> VERSION_CODENAME=jammy
> ID=ubuntu
> ID_LIKE=debian
> HOME_URL="https://www.ubuntu.com/"
> SUPPORT_URL="https://help.ubuntu.com/"
> BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
> PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
> UBUNTU_CODENAME=jammy
> ```
>
> ### Refactoring into Bash Scripts
>
> While fixing the Terraform CLI gpg depreciation issues we noticed that the bash scripts steps were a considerable amount more code. So we decided to create a bash script to install the Terraform CLI.
>
> This bash script is located here: [./bin/install_terraform_cli](./bin/install_terraform_cli)
>
> - This will keep the Gitpod Task File ([.gitpod.yml](.gitpod.yml)) tidy.
> - This allows us an easier to debug and execute manually Terraform CLI install
> - This will allow better portablity for other projects that need to install Terraform CLI
>
> #### Shebang Considerations
>
> A Shebang (prounced Sha-bang) tells the bash script what program that will interpret the script. eg. `#!/bin/bash`
>
> ChatGPT recommends this format for bash: `#!/usr/bin/env bash`
>
> - For portabillity for different OS distributions 
> - Will search the user's PATH fpr the bash executable
>
> [Shebang for Unix](https://en.wikipedia.org/wiki/Shebang_(Unix))
>
> #### Execution Considerations
>
> When executing the bash script we can use the `./` shorthand notation to execute the bash script.
>
> eg. `./bin/install_terraform_cli`
>
> If we are using a script in .gitpod.yml we need to point the script to a program to interpret it.
>
> eg. `source ./bin/install_terraform_cli`
> #### Linux Permisions Considerations
>
> In order to make our bash scripts executable we need to change linux permission to fix to be executable at the user mode.
>
> ```sh
> chmod u+x ./bin/install_terraform_cli
> ```
>
> alternatively:
> ```sh
> chmod 744 ./bin/install_terraform_cli
> ```
>
> [How to Use chmod to Change Permissions](https://en.wikipedia.org/wiki/Chmod)
>
> ### GitHub Lifecyle (Before, Init, Commmand)
> 
> We need to be careful when using the Init because it will not rerun if we restart an existing workspace.
> 
> [Gitpod Tasks Process](https://www.gitpod.io/docs/configure/workspaces/tasks#tasks)

2. Commit changes you made with message
> #3 refactor terraform cli into a bash script for gitpod.yml 

3. Make sure branch is still in Github

4. Make a new pull request with the comment of
> We refactored the Terraform CLI to be a bash script which is executed in the Gitpod.yml file

5. Do a squash and merge.

6. Go to Gitpod and do

`git fetch`

7. Check the Gitgraph and it is merged in. We want to make sure the orgin is the one that has the tag. Go to terminal and run the following

`git checkout main`
`git pull`
`git tag 0.2.0`
`git push --tags`

## "Project Root Env Var" video

### Create a issue and Open New Branch in Gitpod

1. Create an new issue in GitHub and name it 

> Project Root Env Var

Give it a description of

> We are going to set an environment variable for PROJECT_ROOT that we can reference in our bash scripts.

Create the issue.

2. Once created go to the right side and click create a branch. Use the second line to get into that branch

3. Go to the project repo, click GitPod and start it.

### Env Command

1. In Gitpod terminal, use this to see all the environment variables that are set

`env`

NOTE: The project will require variables in all caps and `_` to be used as a space

2. To filter out specific variables use something like these

`env | grep GITPOD`
`env | grep HOSTS`
`env | grep terraform-beginner-bootcamp`

3. When running scripts in Gitpod, it usually uses the directory you are in. Which can suck because if you don't pay attention, you might have installed something in a repo you didn't want

To mitigate that, in the scripts you put cd /workspace and at the end cd back to where it was before. This is something you would want to use enironment variables to make more portable and others can use.

In install_terraform_cli, before the first command put

`cd /workspace`

e.g `cd $THERIA_WORKSPACE_ROOT`

4. To print out a variable you can use echo to print it.
e.g `echo $THERIA_WORKSPACE_ROOT`

5. You can set an env var in a script by doing something like this

e.g `PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023'`

Or put it in the environment using terminal

e.g `PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023' ./bin/install_terraform_cli`

Or you could export it in terminal

`export PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023'`
6. To unset an variable 
e.g `unset PROJECT_ROOT`

### Add "Working with Env Vars" section to README.md

1. At the end of README.md, type out
> ### Working with Env Vars
>
> We can list out all Environment Variables (Env Vars) using the `env` command
>
>We can filter specific env vars using grep eg. `env | grep AWS_`
>
> #### Setting and Unsetting Env Vars
>
> In the terminal we can set using `export HELLO='world'`
>
> In the terminal we can unset using `unset HELLO`
>
> We can set an env var temporarily when just running a command
>
> ```sh
> HELLO='world' ./bin/print_message
> ```
>
> Within a bash script we can set env without writing export. eg.
> ```sh
> #!/usr/bin/env bash 
>
> HELLO='world'
>
> echo $HELLO
> ```
>
> #### Printing Vars
>
> We can print an env var using echo eg. `echo $HELLO`

2. If you define a env var in terminal, it is local to terminal and will not be able to be used in the terraform: bash and aws-cli: bash in terminals.

To have them everywhere, you would have to set env var globally

Add this to the end of README.md
> #### Scoping for Env Vars
>
> When you open up new bash terminals in VSCode, it will not be aware of env vars you set in another window
>
> If you want Env Vars to persist across all future bash terminals that are open, you need to set env vars in your bash profile. eg. `bash_profile`
>
> #### Persisting Env Vars in Gitpod
>
> We can persist env vars into Gitpod by storing them in Gitpod Secrets Storage.
>
> ```
> gp env HELLO='world'
> ```
>
> All future workspaces launched will set the env vars for all bash terminals opened in those workspaces.
>
> You can also set env vars in the `.gitpod.yml` but this can only contain non-sensitive env vars

### Set Env Var for PROJECT_ROOT the Gitpod way

1. Make a new file under /bin and name it:

> .env.example

2. In .env.example put 
`PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023'`

We are never going to need to set .env.example file but this would be important because if someone doesn't use Gitpod, it's a way to show what env var this project needs.

3. We are going to set this variable so that it always persists. In terminal, set the env var the gitpod way

`gp env PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023'`

If you do an echo on that env var, nothing will come as it was sent to Gitpod secrets.

### Make sure install_terraform_cli is good and restart to see changes

1. In install_terraform_cli, make sure that `cd /workspace` is at the top.

Put this at the bottom on the file

`cd $PROJECT_ROOT`

2. In the source tab, stage the changes and provide this commit message
> #5 provide example env for env var project root, provide good documentation about env vars

3. Restart the Gitpod and launch it again

4. Once launched, go to gitpod terminal and click the terraform terminal. Check if the variable is still there
`echo $PROJECT_ROOT`

### Do a PR

1. In GitHub create a pull request. Leave a comment:
> Adding documentation for env vars and env.examples

2. Create pull request

3. Add the "documentation" label to the issue we just closed

4. Reopen branch 5 in Gitpod. Do the following in terminal:
`git checkout main`
`git pull`

5. Go over to source control and find out where we are in GitGraph. We see the merge but now we need to tag it. 
`git tag 0.3.0`
`git push --tags`

## "AWS CLI Refactor" video

### Create a New Issue and Launch New Branch in Gitpod

1. Go to GitHub and click the issues tab, create a new issue and name it
> Refactor AWS CLI Script

For the description put
> - [ ] Refactor AWS CLI into bash script
> - [ ] Provide env var examples for AWS CLI requirements
> - [ ] Set our env vars for AWS using gp env

2. Change label of the issue to enhancement and then create the issue

3. Go to the right pane of the issue and click create new branch

4. Go to the code tab and go into the newly created branch and launch Gitpod 

### Create install_aws_cli and edit README.md

1. In Gitpod, go to the bin directory and click create new file and name the file
> install_aws_cli

2. Go to install_terraform_cli and copy and paste this code into install_aws_cli
`#!/usr/bin/env bash `

3. Go to .gitpod.yml and copy and paste the aws before command to install_aws_cli
`cd /workspace`
`curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`
`unzip awscliv2.zip`
`sudo ./aws/install`
`cd $THEIA_WORKSPACE_ROOT`

4. In install_aws_cli change the last command to this
`cd $PROJECT_ROOT`

5. In a browser find the install aws cli page and copy the link.
> https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

6. Go to README.md and add 
`### AWS CLI Installation`

`AWS CLI is installed for the project via the bash script [`./bin/install_aws_cli`](./bin/install_aws_cli)`

`[Getting Started Install (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)`

7. Go to gitpod.yml and replace the before message to launch the install_aws_cli
`source ./bin/install_aws_cli`

8. Go to the AWS terminal and type in aws for bring the prompt box forward
`aws`

9. Do this to create a hello world
`aws sts get-caller-identity`

You should get an error because you haven't set any env var
You don't want to use `aws configure` but use the env vars instead

10. Go to README.md and add
> We can check if our AWS credentials is configured correctly by running the following AWS CLI command:`
> ```sh
> aws sts get-caller-identity
> ```

### Add AWS Env Vars and Create AWS user
1. Go to a browser and find the AWS env var documentation
> https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html

2. Go to README.md and add this after the link for Getting Started (AWS CLI)
`[AWS CLI Env Vars](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html)`

3. On the AWS env vars link, go down to Linux or MacOS and copy the code. Paste it in .env.examples and remove the export commands in front of it and add single quotes to values, like this

`AWS_ACCESS_KEY_ID='AKIAIOSFODNN7EXAMPLE'`
`AWS_SECRET_ACCESS_'KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY'`
`AWS_DEFAULT_REGION='us-west-2'`

The values for these variables are fake but you would **NEVER WANT TO PUT YOUR REAL CREDENTIALS IN THIS FILE**

**DON'T PUT YOUR REAL AWS CREDENTIALS INTO YOUR REPO!!!**

4. Log into your AWS account you are going to use for the project and go to IAM>users and create new user
> terraform_beginner_bootcamp

5. Add that user to an admin group with permissions of AdministratorAccess and create the user

6. Go to the user and go to the security credentials and create the access key

7. Choose Command Line as the use case

### Use AWS Credentials

**DON'T COMMIT THE CHANGES TO THE REPO WHEN DOING THIS**

1. In Gitpod, go to the .env.example file and copy the AWS credentials variable and paste them below. Add export to the beginning of the AWS credentials variables then add the variable values with the terraform beginner secret key then copy it.

2. In the AWS terminal paste and enter the credential values. Confirm they are there.
`env | grep AWS_`

3. In .env.example change the credentials with 'export' to 'gp env'. Copy the lines and paste them in the AWS terminal and enter.

4. **DELETE THE LINES FROM .env.example** and save

5. In AWS terminal, check if the credentials work
`aws sts get-caller-identity`

6. In README.md, add this

> If it is successful you should a json payload return that looks like this
> ```json
> {
>     "UserId": "AIAA75AN7YUW56Y6DGWY5",
>     "Account": "123456789012",
>     "Arn": "arn:aws:iam::123456789012:user/terraform_beginner_bootcamp"
> }
> ```
>
> We'll need to generate AWS CLI credits from IAM user in order to use the AWS CLI.
NOTE: We fudged some numbers in the JSON to not expose stuff

7. In install_aws_cli, paste this command before cd $PROJECT_ROOT

`aws sts get-caller-identity`

8. In aws terminal test script locally and it should prompt you to write over
`chmod u+x ./bin/install_aws_cli`
`./bin/install_aws_cli`

9. We don't want it to prompt us so go to install_aws_cli and add this after cd /workspace

`rm -f '/workspace/awscliv2.zip'`
`rm -rf '/workspace/aws'`

10. In AWS terminal run the install file again to see if it works
`./bin/install_aws_cli`

8. In the source control tab, stage the changes and commit with
> #7 refactor AWS CLI into a bash script

9. Stop the Gitpod workspace and check GitHub that changes were commited to the branch. Open Gitpod for the branch.

10. In Gitpod, the AWS terminal should show the credentials in json. AWS is logged in. Stop the Gitpod

11. In Github, check off the issues we did. Copy the comments of the issue

12. In GitHub, make the pull request. In the comments paste the issues and readd the "-[x]" in front of the issues.
> - [x] Refactor AWS CLI into bash script
> - [x] Provide env var examples for AWS CLI requirements
> - [x] Set our env vars for AWS using gp env

### Check Git Graph and add tags

1. In Github, go to the branch and launch Gitpod.

2. In source control tab, open up Git Graph and see that we see that merge

3. In terminal, tag the branch
`git tag 0.4.0`
`git push --tags`
`git fetch`

4. Stop the gitpod and go back to GitHub, and check the tag.

## "Random Terraform Provider Init Plan Apply"

# Create an issue

1. 

