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
> ```bash
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
> ```bash
> chmod u+x ./bin/install_terraform_cli
> ```
>
> alternatively:
> ```bash
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
> ```bash
> HELLO='world' ./bin/print_message
> ```
>
> Within a bash script we can set env without writing export. eg.
> ```bash
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
> ```bash
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
> ```bash
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

1. In Github go to issues and create a new issue. Name the issue
> Terraform Random Bucket Name

Give a description of
> - [ ] explore the terraform registry
> - [ ] install the terraform random provider
> - [ ] run the terraform init
> - [ ] generate out a random bucket name
> - [ ] output the random bucket name to outputs

Create the issue.

2. Create the branch of of the issue.

3. Go to the code tab and select the newly created branch and launch Gitpod.

# Check the branch is working 

1. Go to the AWS terminal and Terraform terminal to make sure it is working

2. In a browser, navigate to the terraform registry
> https://registry.terraform.io

This is where we will get providers and modules

Providers is what you use to integrate third-party api to make it powered by terraform

modules is a way to provide a template to utilize commly used actions

3. In the search bar of the website search for random. Click use this provider. Copy the code it gives you
`terraform {`
`  required_providers {`
`    random = {`
`      source = "hashicorp/random"`
`      version = "3.5.1"`
`    }`
`  }`
`}`

`provider "random" {`
`  # Configuration options`
`}`

4. In Gitpod, go to main.tf and paste in the code.
main.tf is a top-level module.

We additionally need to provide a resource.
Go to the documentation for the terraform random provider.
Copy the first provider

```go
resource "random_id" "server" {
  keepers = {
    # Generate a new id each time we switch to a new AMI id
    ami_id = var.ami_id
  }

  byte_length = 8
}
```
5. In main.tf paste the resource into provider "random.
change "server" to "bucket_name"

6. Go to the random documentation and expaand resources on the left. Go to random_string.
Copy the example usage.

```go
resource "random_string" "random" {
  length           = 16
  special          = true
  override_special = "/@£$"
}
```
7. Go to main.tf, paste it over the resource we gave. Chang the second line "random" to "bucket_name".

`resource "random_string" "bucket_name" {`

8. Take out the value of override_special

`  override_special = ""`

9. Go to a broswer and search for terraform output.
> https://developer.hashicorp.com/terraform/language/values/outputs

Copy the code under declaring an output value and paste it at the end of main.tf.

output "instance_ip_addr" {
  value = aws_instance.server.private_ip
}

10. Edit the string for output to say "random_bucket_name_id"
Remove aws_instance.server.private_ip and change it to random_string.bucket_name.id
```go
output "random_bucket_name_id" {
  value = random_string.bucket_name.id
}
```

11. Copy the output code and paste it below it. Change .id to .result
```go
output "random_bucket_name_result" {
  value = random_string.bucket_name.result
}
```

12. Change resource values of special to false. Remove override_special.
```go
provider "random" {
resource "random_string" "bucket_name" {
  length           = 16
  special          = false
}
}
```

### Run a terraform init

1. In Gitpod, go to the terraform terminal. Use the following
`terraform`
`terraform init`

It created the terraform.lock.hcl and the .terraform folder.

The .terraform folder contains a file that is binary. We do not want to commit with this file as it will make it everytime we run init

2.  Go to .gitignore and make sure that file is ignored. The command should be 
```bash
# Local .terraform directories
**/.terraform/*
```

### Run a terraform plan and terraform apply

1. In the terraform terminal use this to do a terraform plan
`terraform plan`

2. If successful, run a terraform apply
`terraform apply`

3. When it asks you for a value type yes to apply it

#### Problem: When I ran terraform plan, I got an error.

```bash
$ terraform plan
╷
│ Error: Reference to undeclared resource
│ 
│   on main.tf line 18, in output "random_bucket_name_id":
│   18:   value = random_string.bucket_name.id
│ 
│ A managed resource "random_string" "bucket_name" has not been declared in the
│ root module.
╵
╷
│ Error: Reference to undeclared resource
│ 
│   on main.tf line 22, in output "random_bucket_name_result":
│   22:   value = random_string.bucket_name.result
│ 
│ A managed resource "random_string" "bucket_name" has not been declared in the
│ root module.
```

I chatgpt it, and it said to use this instead to fix the issue
```go
terraform {
  required_providers {
    random = {
      source = "hashicorp/random"
      version = "3.5.1"
    }
  }
}

provider "random" {}

resource "random_string" "bucket_name" {
  length = 16
  special = false
}

output "random_bucket_name_id" {
  value = random_string.bucket_name.id
}

output "random_bucket_name_result" {
  value = random_string.bucket_name.result
}

```

When I ran terraform plan, it works now.

### Change main.tf outputs and test it works

1. In main.tf, remove .id from the first output and change the value .id to .result

2. Remove the secound output
It should look like this when done

```go
output "random_bucket_name" {
  value = random_string.bucket_name.id
}

output "random_bucket_name_result" {
  value = random_string.bucket_name.result
}
```

3. In terraform terminal, run terraform plan
The changes to output will say _id and _result where changed

4. Run this to run teraform apply but not be prompted yes to apply
`terrafrom apply --auto-approve`

5. It will return the bucket name and create state files.
If you need the bucket name again, you can run
`terraform output`

### Add documentation

1. In README.md, add the following

```md
## Terraform Basics

### Terraform Registry

Terraform sources their providers and modules from the terraform registry which is located at [registry.terraform.io](https://registry.terraform.io)

- **Providers** is an interface to APIs that will allow you to create resources in terraform.

- **Modules** are a way to refactor or to make large amounts of terraform modular, portable, and sharable.

[Random Terraform Provider](https://registry.terraform.io/providers/hashicorp/random/)
### Terraform Console

We can see a list of all the terraform commands by simply typing `terraform`.


#### Terrafrom init

At the start of a new terraform project we will run `terraform init` to download the binaries for the terraform providers we will use in this project.

#### Terraform Plan

`terraform plan`

This will generate out a changeset, about the state of our infrastructure and what will be changed.

We can output this changeset ie. "plan to be passed to an apply, but often you can ignore the outputing

#### Terraform Apply

`terraform apply`

This will run a plan and pass the changeset to be executed by terraform. Apply should prompt yes or no.

If we want to automatically approve an apply we can provide the auto approve flag eg. `terraform apply --auto-approve`

### Terraform Lock files

`.terraform.lock.hcl` contains the locked versioning for the providers or modules that should be used with this project.

The Terraform Lock File **should be commited** to your Version Control System (VCS) eg. GitHub

### Terraform State files

`terraform.tfstate` contains information about the current state of your infrastructure. 

This file **should not be committed** to your VCS.

This file can contain senstitive data.

If you loose this file you loose knowing the state of the infrastructure.

`terraform.tfstate.backup` is the previous state file state.

### Terraform Directory

`.terraform` directory contains binaries of terraform providers.
```

## Make sure you're committing the correct things and PR

1. Go to to source control tab and make sure the state files are not in there.

2. Go to Github issues and checkoff what we have done.

3. In Gitpod, stage the changes and commit with this message
> #9 add random terraform provider

4. Do a pull request with the message 

> - [x] explore the terraform registry
> - [x] install the terraform random provider
> - [x] run the terraform init
> - [x] generate out a random bucket name
> - [x] output the random bucket name to outputs

## Git Graph and Add tags

1. In Gitpod terminal, 
`git checkout main`
`git pull`

2. Check Git Graph tree to see merge

3. Tag the branch
`git tag 0.5.0`
`git push --tags`
`git fetch`

4. Make sure the tag is in Git Graph and GitHub then stop the workspace.

## "Terraform Provider S3 Bucket, Terraform Destroy" video

### Create a New Issue

1. In GitHub Issues, create a new issue. Name it:

> Simple S3 Bucket

Add description

- [ ] Define an S3 Bucket in Terraform
- [ ] We are going to use the random resource for the name
- [ ] Install the AWS Terraform Provider
- [ ] Configure AWS Provider
- [ ] Terraform apply and terraform destroy

2. In the issue, create the branch.

3. In code tab, go to the newly created branch and click Gitpod

### S3 buckets

1. In Gitpod AWS terminal list the AWS S3 buckets
`aws`
`aws s3 ls`

You should have no buckets

2. See what user you are
`aws get-caller-identity`

3. In Terraform Registry webpapage> Providers>AWS>Documentation>S3>aws_S3_bucket
> https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket

Copy the example usage of a Private Bucket with Tags

```Go
resource "aws_s3_bucket" "example" {
  bucket = "my-tf-test-bucket"

  tags = {
    Name        = "My bucket"
    Environment = "Dev"
  }
}
```
4. In Gitpod main.tf, paste the example in front of output. Commit it out for the moment. 
Hint: Highlight it and use cmd+/

5. In Terraform terminal, do a terraform init because we don't have `.terraform` directory yet
`terraform init`

6. Apply the terraform
`terraform apply --auto-approve`

### Show an Error When Naming a Bucket

1. In main.tf, uncomment aws_s3_bucket and remove the tags portion. Chane the bucket value to be a random_string.bucket_name.result
```go
resource "aws_s3_bucket" "example" {
  bucket = random_string.bucket_name.result
}
```

2. In terraform terminal, run terraform plan
`terraform plan`

We should get an error because we have not specified a provider

```bash
$ terraform plan
╷
│ Error: Inconsistent dependency lock file
│ 
│ The following dependency selections recorded in the lock file are inconsistent with the current configuration:
│   - provider registry.terraform.io/hashicorp/aws: required by this configuration but no version is selected
│ 
│ To update the locked dependency selections to match a changed configuration, run:
│   terraform init -upgrade
```
3. Go to Terraform Registry webpage>Browse Providers>aws>use provider and copy the code given
```go
terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "5.17.0"
    }
  }
}

provider "aws" {
  # Configuration options
}
```

4. In main.tf paste it after the first required provider.

5. In terminal, run `terraform plan` and we should get an error because we can't have more than one provider for a module.

```bash
$ terraform plan
╷
│ Error: Duplicate required providers configuration
│ 
│   on main.tf line 10, in terraform:
│   10:   required_providers {
│ 
│ A module may have only one required providers configuration. The required providers were previously configured at
│ main.tf:2,3-21.
╵
```

6. Copy the aws provider without terraform and required providers (delete the leftover)
It should like this

```go
terraform {
  required_providers {
    random = {
      source = "hashicorp/random"
      version = "3.5.1"
    }
    aws = {
      source = "hashicorp/aws"
      version = "5.17.0"
    }
  }
}
```

7. In terminal, do `terraform plan`

You should get an error because it doesn't have the binary file for the provider, aws. It also doesn't have the provider hashes in the .terraform.lock.hcl

```bash
$ terraform plan
╷
│ Error: Inconsistent dependency lock file
│ 
│ The following dependency selections recorded in the lock file are inconsistent with the current configuration:
│   - provider registry.terraform.io/hashicorp/aws: required by this configuration but no version is selected
│ 
│ To update the locked dependency selections to match a changed configuration, run:
│   terraform init -upgrade
```

8. In order to fix this you have to run `terraform init` in terminal

9. Run `terraform plan`. It should work but will fail when applyingit will have uppercase for the bucket name which won't let you create the bucket

10. Run `terraform apply` and give a yes when prompted. It will fail because of invalid bucket name.

### Fix Random Bucket Name 

1. In a browser navigate to S3 Bucket Naming Rules documentation and copy the url
> https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html

2. In Gitpod main.tf paste the url into resource "aws_s3_bucket. Comment it out and add another comment above with Bucket Naming Rules

```go
resource "aws_s3_bucket" "example" {
  # Bucket Naming Rules
  # https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html
  bucket = random_string.bucket_name.result
}
```
3. Go to Terraform Registry documenation for aws_s3_bucket and copy/paste in main.tf above the resource "aws_s3_bucket". Comment it out

```go
# https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket
resource "aws_s3_bucket" "example" {
  # Bucket Naming Rules
  # https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html
  bucket = random_string.bucket_name.result
}
```

4. In Terraform Registry search for random. In documentation, go to random-string and copy the url
> https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string

Paste this in main.tf above the resource for random_string and comment it out

```go
# https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string
resource "random_string" "bucket_name" {
  length = 16
  special = false
}

```
5. In the resource parameters for "random_string" "bucket_name" put lower as true and upper as false so we don't have a bucket name created with uppercase. Also change length to 32 characters

```go
# https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string
resource "random_string" "bucket_name" {
  lower=true
  upper=false
  length = 32
  special = false
}
```

6. In terminal run `terraform plan`
Hint: `terraform validate` will allow you to validate your code

7. Run `terraform apply`. Type yes and hit enter

### Verify in AWS That Bucket was created and Destroy Bucket

1. Go to AWS console and see that bucket was created.

2. In Gitpod terminal destroy the terraform to delete that bucket. Type/enter yes when prompted.
`terraform destroy`

3. Go to AWS console and see that the bucket is gone now.

### Edit README.md to Add Documentation and Commit

1. In Gitpod README.md before "#### Terraform Lock Files" add this

```md
#### Terraform Destroy

`terraform destroy`
This will destroy resources.

You can also use the auto-approve flag to skip the approve prompt eg. `terraform destroy --auto-approve`
```

2. In source control tab, go through your files and make sure there are no secrets. Stage the changes and commit with a message:

> #11 Install terraform provider, create s3 bucket

3. In GitHub, check tasks in issue.

### Homework: Create a Section in README.md about Bucket Naming issue

1. In Gitpod, add a section about the S3 bucket naming problem we encountered. For example, mine is

```md
##### Problems Applying S3 Bucket

When applying bucket with main.tf, we needed to make sure that the parameters for resource "aws_s3_bucket" "bucket name" had upper as false and lower as true

If you don't have these set then the terraform plan will try to name bucket with uppercase which is not allowed for an S3 bucket. `terraform plan` will say it's good but when using `terraform apply`, it will fail with invalid bucket name

[S3 Bucket Naming Rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html)
```
2. Commit with the message explaining what you did like
> #11 Added S3 bucket naming problem to README.md

### Pull request and tags

1. In GitHub pull request, create a new pull request. In the comments put the issues we checked off

> - [x] Define an S3 Bucket in Terraform
> - [x] We are going to use the random resource for the name
> - [x] Install the AWS Terraform Provider
> - [x] Configure AWS Provider
> - [x] Terraform apply and terraform destroy

2. Click "create pull request" and then "squash and merge"

3. In Gitpod, look at the Git Graph to see the merge. 

4. In terminal do the following to tag the main branch:
`git checkout main`
`git pull`
`git tag 0.6.0`
`git push --tags`

5. In Github code tab, check if the tag is there. Stop Gitpod.

## "Terraform Cloud and Terraform Login" video

# Remotely Manage Our State

We don't want to locally manage our state because we are responsible for the state file.
Instead we want to remotely manage our state using a provider like Terraform Cloud

1. In Github main branch, launch Gitpod. Make sure in the terminals that everything launched okay

2. In browser go to terraform cloud and login.

3. Click New>Project. 

In terraform cloud a workspace and project are diffrent:
- Workspace: A container in Terraform Cloud for infrastructure state, configurations, and settings.
- Project: (conceptual) An overarching effort or goal, potentially consisting of multiple Terraform Cloud workspaces.

4. Name the project and create.
> terraform-beginner-bootcamp-2023

5. In the new project box click "create new workspace"

6. In Gitpod terraform terminal do `terraform init` then `terraform apply --auto-approve`

## Move terraform.tfstate to Terraform Cloud

1. Go back to Terraform Cloud to create a workspace in our project. Choose cli-driven workflow. 
Name the workspace terra-house-<whatyou want your house to be>
> terra-house-hello-kitty-island-adventure

Give a description of
> This will be our Terrahouse infrastructure that will connect to TerraTowns.

Create the workspace.

2. Copy the example code given to you. Go to Gitpod main.tf and paste it after "terraform {"
It should look like this

```go
terraform {
    cloud {
    organization = "example-org-0dcec0"

    workspaces {
      name = "terra-house-hello-kitty-island-adventure"
    }
  }
  required_providers {
    random = {
      source = "hashicorp/random"
      version = "3.5.1"
    }
    aws = {
      source = "hashicorp/aws"
      version = "5.17.0"
    }
  }
}

```
3. In terraform terminal run `terraform init`. You should get an error as we don't have a token.
We have to login first.

4. Run `terraform login` and type/enter yes in the prompt.

5. In the Terraform Cloud box, enter captial P.
Click the link in document with cmd+click.

6. Create a user token. Andrew used one day but I am going to use 30 days.
Copy the token it gives you.

7. In Terraform box enter q to quit and then y. Paste that token.

8. In terraform terminal run `terraform init` and enter yes when prompted

9. In Terraform Cloud, go to your terra-house in the project. We should see the resources and an output.

### Add documentation to README.md and commit

1. In Gitpod README.md

```md
## Issues with Terraform Cloud Login and Gitpod Workspace

When attempting to run `terraform login` it will launch bash a wiswig view to generate a token.
However, it does not work as expected in Gitpod VSCode in the browser. It works in Gitpod VSCode locally.

The workaround if you are using the Gitpod VSCode in the browser is to manually generate a token in Terraform Cloud.

```
https://app.terraform.io/app/settings/tokens
```

Then create the file manually here:

```bash
touch /home/gitpod/.terraform.d/credentials.tfrc.json
open /home/gitpod/.terraform.d/credentials.tfrc.json
```

Provide the following code (replace the token in the file):

```json
{
  "credentials": {
    "app.terraform.io": {
      "token": "YOUR-TERRAFORM-CLOUD TOKEN"
    },
  }
}
```
2. Backtrack and create a issue in GitHub with name:
> Terraform Cloud Backend

Give description of: 

> - [ ] Configure Terraform Cloud Backend
> - [ ] Workaround for Terraform Login
> - [ ] Migrate our local state to remote state
> - [ ] Create a new Project and Workspace in Terraform Cloud

3. Check off issues. Create the branch off of the issue.

4. In Gitpod terminal do
`git fetch`
`git add .`
`git stash save`

5. Go back to GitHub and copy the new branch name. Go back to Gitpod
`git checkout 13-terraform-cloud-backend`
`git stash apply `

6. Review changes, stage changes, and commit with message:
> #13 migrate local state to terraform cloud using terraform cloud block

7. Make sure issue is closed. Go to pull request with issues as comment. Create pull then merge and squash

### Add tags 

1. In Gitpod do
`git checkout main`
`git pull`
`git tag 0.7.0`
`git push --tags`

2. Check Git Graph and GitHub

3. Stop Gitpod

## "Terraform Login Workaround" video

### Create an issue
1. In GitHub create an issue with the name
> Generate TFRC 

With the description of
> - [ ] Create a bash script using ChatGPT to create tfrc file.
> - [ ] Create new token for 30 days in Terraform Cloud.

2. Open a branch off of the issue.

3. Go to the code tab and choose the newly created branch. Launch Gitpod.

### 

1. Go to chatGPT and ask
> Write a bash script that will generate out the json file crendentials.tfrc.json with the json structure you generated out and it should use the env var TERRAFORM_CLOUD_TOKEN
It should return something similar to this although mine went off the rails and didn't have anything close to this.
```bash
#!/user/bin/env bash

# Check if TERRAFORM_CLOUD_TOKEN is set
if [ -z "$TERRAFORM_CLOUD_TOKEN" ]; then
    echo "Error: TERRAFORM_CLOUD_TOKEN environment variable is not set"
    exit 1
fi

# Generate credentials.tfrc.json with the token
cat > credentials.tfrc.json << EOF
{
    "credentials": {
        "app.terraform.io": {
            "token": "$TERRAFORM_CLOUD_TOKEN"
        }
    }
}
EOF

echo "credentials.tfrc.json has been generated."

```
Copy that code or this code.

2. In gitpod create a new file under bin directory and name it
> generate_tfrc_credentials

Paste the copied code into there

3. Set the TERRAFORM_CLOUD_TOKEN variable in terminal with
`gp env TERRAFORM_CLOUD_TOKEN='<Your-token>'`
`export TERRAFORM_CLOUD_TOKEN='<Your-token>'`

I already set my 30-day token in the last video so I am not doing that.
You can do a `terraform login status` to make sure the credentials are still good.
Mine gives an error of 
```bash
$ terraform login status
╷
│ Error: Service discovery failed for status
│ 
│ failed to request discovery document: Get
│ "https://status/.well-known/terraform.json": dial tcp: lookup status on
│ 1.1.1.1:53: no such host.
╵
```
So if I need to create a new token later I will. ChatGPT said it's a DNS issue.
I will do a `gp env TERRAFORM_CLOUD_TOKEN='<Your-token>'` 
and `export TERRAFORM_CLOUD_TOKEN='<Your-token>'` if it doesn't work.

4. Make the new file able to execute
`chmod u+x ./bin/generate_tfrc_credentials`

5. Execute the file
`./bin/generate_tfrc_credentials`

I get an error of 
```bash
Error: TERRAFORM_CLOUD_TOKEN environment variable is not set
```
So I will create a new token and redo the steps. It works.

6. Confirm the token is there
`env | grep TERRAFORM_`

7. The code we got from ChatGPT or from the video is not writing to right location
I couldn't find the repo that he was saying to copy so I wrote it out from video.
Then I ran it though ChatGPT and fixed any typos.

```bash
#!/usr/bin/env bash

# Define target directory and file
TARGET_DIR="/home/gitpod/.terraform.d"
TARGET_FILE="${TARGET_DIR}/credentials.tfrc.json"

# Check if TERRAFORM_CLOUD_TOKEN is set
if [ -z "$TERRAFORM_CLOUD_TOKEN" ]; then
    echo "Error: TERRAFORM_CLOUD_TOKEN environment variable is not set"
    exit 1
fi

# Check if directory exists, if not, create it
if [ ! -d "$TARGET_DIR" ]; then
    mkdir "$TARGET_DIR"
fi

# Generate credentials.tfrc.json with the token
cat > "$TARGET_FILE" << EOF
{
    "credentials": {
        "app.terraform.io": {
            "token": "$TERRAFORM_CLOUD_TOKEN"
        }
    }
}
EOF

echo "${TARGET_FILE} has been generated."
```
8. Delete the credentials.tfrc.json because we do not want to have that as it has our credentials

9. Run the file to make sure it generates where we want
`./bin/generate_tfrc_credentials`

10. cat the output file to see the contents
`cat /home/gitpod/.terraform.d/credentials.tfrc.json`

11. Run `terrafrom init` to make sure it's okay

### Make edits to .gitpod.yml, README.md, and .env.examples

1. Go to .gitpod.yml and add to terrafrom before sources
`source ./bin/generate_tfrc_credentials`

2. Go to README.md and add documentation
```md
We have automated this workaround process using the following bash script [./bin/generate_tfrc_credentials](./bin/generate_tfrc_credentials)
```

3. Go to .env.examples and add the TERRAFORM_CLOUD_TOKEN
`TERRAFORM_CLOUD_TOKEN='YOUR SECRET TERRAFROM CLOUD TOKEN`

### Commmit, update issues, and pull request

1. Stage changes and commit with
> #15 generate workaround for terraform login with gitpod

2. In GitHub go to issues tab and check off issues. Edit then copy the issue description.

3. In pull request and paste the issues with pull request comment
> - [x] Create a bash script using ChatGPT to create tfrc file.
> - [x] Create new token for 30 days in Terraform Cloud.

squash and merge

### Add tags

1. In Gitpod check Git Graph to see if the merge is good

2. Run the following
`git checkout main`
`git pull`
`git tag 0.8.0`
`git push --tags`
`git fetch`

3. In GitHub, make sure the tag is there.

4. Stop gitpod

## "TF_Alias" video

### Make an issue

1. In GitHub create an issue. Name it
> TF alias for Terraform
Give it a description of
> - [ ] Set an alias for terraform to be tf in our bash file.

2. Create a branch for the issue

3. In code tab use the new branch and click Gitpod

### Make an alias of tf to run terraform

1. In Gitpod terraform terminal open the bash file for our bash profile 
`open ~/.bash_profile`

2. Go to browser and look up alias in bash
> https://linuxize.com/post/how-to-create-bash-aliases/#google_vignette

3. In Gitpod ~./bash_profile use the alias to map tf to terraform
`alias tf="terraform"`

4. Run tf in terminal.
It won't work because when we update ~/.bash_profile we have to reload it
`source ~./bash_profile`

5. Run `tf` and it should work.

### Make bash script for alias to be permanent

1. Gitpod is not going to set this up every single time unless we make a script for it.
Go to chatGPT and ask it
> write a bash script that will add the following alias to our ./bash_profile
> alias tf="terraform"

Copy the script

```bash
#!/usr/bin/env bash

# Check if the alias already exists in the .bash_profile
grep -q 'alias tf="terraform" ~/.bash_profile'

# $? is a special variable in bash that golds the exit status of the 
if [ $? -ne 0 ]; then
    # If the alias does not exist, append it
    echo 'Alias tf="terraform"' >> ~/.bash_profile
    echo "Alias added successfully."
else
    # Inform the user if the alias already exists
    echo "Alias 'tf' already exists in ~/.bash_profile."
fi 
```

2. In Gitpod create a new file in ./bin named
> set_tf_alias

3. Paste the code into set_tf_alias and add this at the end
`source ./bin/set_tf_alias`


4. Change the permissions of set_tf_alias to be executable
`chmod u+x ./bin/set_tf_alias`

5. In gitpod.yml add the file as source for terraform and aws-cli before in as the first source
`source ./bin/set_tf_alias`

6. Stage and commit the changes with
> #17 add a script to add tf alias

7. Stop the gitpod

### Test the code

1. In GitHub choose the latest branch and launch Gitpod

2. And it broke
```bash 
 HISTFILE=/workspace/.gitpod/cmd-0 history -r; {
source ./bin/set_tf_alias
source ./bin/install_terraform_cli
source ./bin/generate_tfrc_credentials

}
gitpod /workspace/terraform-beginner-bootcamp-2023 (17-tf-alias-for-terraform) $  HISTFILE=/workspace/.gitpod/cmd-0 history -r; {
> source ./bin/set_tf_alias
> source ./bin/install_terraform_cli
> source ./bin/generate_tfrc_credentials
> 
> }

```
Will try tomorrow