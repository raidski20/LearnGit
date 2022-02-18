# Demo Repo To Learn Git

# 1: ssh keys
To use github to commit your changes ...etc, first you must connect your machine with your account for that we can use ssh.

# 1-A: ssh keys generation
To generate ssh keys we use the commande: ssh-keygen -t rsa -b 4016 -C "your_github_email_@"
PS: whene your generate your ssh key by default it generates a public and private keys, located in: /home/raid/.ssh/ and the name of your file will be what you specify: for example "learning & learning.pub"

# 1-B: add your key in github
After generating it now you must put the public key in your github account under "SSH & GPG Keys" section in settings.

# 1-C: add ssh key to ssh-agent
Now you must let your local git command line knows about the key you just add it, for that just see the doc.

# 2: Git repo
You can create a new git repo on your github accout.

# 3: git init
After creating a new git repo, copy the given url and go to your project folder and initialize it using the command: git init 

# 4: git remote add origin link_of_your_repo
After initializing your project folder, no it's time to reference your project folder to your remote git repo on github, for that we use the command: git remote add origin link_of_your_repo, after that you can check the setup using: git remote -v

# 5: git add .
This command means you're telling git to track all the changed or created or deleted files.

# 6: git commit -m "message here"
This command used to commit your files/changes, and your have to leave a message or comment for this commit so we use -m parameter. This commit message explains what you've did in this commit, just a short brief.

# 7: git push origin master
Your code is saved locally on your local machine, it means your code or commit isn't live on github yet. To make it live we use this command: git push origin master.
Origin: option for the position of your git repository.
Master: the branch which you want to push to. 

# 8: git push
This command is just an abbriviation for "git push origin master" command.

# 9: git status
This command shows all the new or deleted or updated files but haven't been saved in a commit yet.

# #################### Git Branching ####################
In git repo by default there is only one branch which is the "master" branch where you push your commits, but you can create much branchs as you want.
Each branch works separatly from other branchs, if you push a commit to specific branch that commit want be available for other branchs. For example if you have a code of an app saved in the master branch, and you're going to add new features to that app and those features may break your code so, you can create new branch called features and push the code to it. 
When you finish developing those features and make sure they don't break you app no you can merge it to the master branch.

# 10: git branch
To see branchs that you have in your repo, the current branch that you're in is precceded by *

# 11: git checkout -b name_of_your_branch
To create new branch.

# 12: git checkout branch_name
To switch from the current branch to another branch.

# 13: git push origin branch_name
To push your changes to a specific branch.

# 14: git pull origin branch_name
To get the new updates into your project.

# 15: git merge branch_to_be_merged
To merge your current branch with the matser branch, first you go to the master branch then run the command above, for ex if you want to merge a banch called test-branch into master branch, first you go to the master branch then run: "git merge test-branch" then run "git push origin master" to merge them on remote.

# 16: git branch -d branch_name
To delete a specific branch locally on your machine.

# 17: git push origin -d new-branch
To delete a specific remote branch.

# #################### Undoing Stuff

# 18: git reset
This command allows you unstage commmits (means after you do git add . you can cancell it using the above command, if you want to unstage a specific file just pass it's name as argument).

# 19: git reset HEAD~1
This command allows you undo a commit, the "HEAD" points to the last commit, and "~1" means how many steps to go back.

# 20: git reset --hard
Remove completely the changes

# 21: git log
To see a log of all your commits, or you can use also "git log --oneline"