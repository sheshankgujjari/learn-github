# learn-github


# Setup GitHub

## Prerequisites
1. These steps assume that you have a Git client with git-bash installed. if not, go download/install Git - https://git-for-windows.github.io/
2. These steps assume you have a GitHub account at https://github.com/, if not create a new account https://github.com/


## Prerequisite on configuring Your Key
1. On your own machine, run the application 'Git-bash'
2. In the bash shell, type the command (replacing with your own email address:)
   ``ssh-keygen -t rsa -b 4096 -C "your_email"``
3. When prompted for "Enter file in which to save the key:" <hit enter to accept default of 'id_rsa'>
4. when prompted for "Enter passphrase:" <leave empty for no passphrase - just hit 'enter' to continue>
5. With Notepad or similar tool, open the newly-generated ~/.ssh/id_rsa.pub file in order to copy/paste the entire keygen into your GitHub account as described below


# Configuring Your Github account with the Public SSH Key
1. Browse to https://github.com/ and sign in with your account
2. Click on your account icon drop-down menu and select "Settings"
3. On the left-side menu, click the "SSH and GPG Keys" item
4. Click the "New SSH Key" button and configure as follows:
5. Title: Type in a descriptive name for this key - e.g. 'key_2018_Aug08' or something that makes sense to you
6. Key: <This is where you copy/paste the entirety of the id_rsa.pub file into this field>
7. Click the "Add SSH Key" button to save this configured key

# Setup github credentials on your local machine
1. Open https://github.com/username
2. Click on your profile and Settings tab
3. On your left you will see Developer Setting tab, please click on it
4. Click on personal access token
5. Click on Generate Token and choose all the options provided
6. COPY THE ACCESS TOKEN AND YOU CANNOT RE-COPY IF YOU MISS IT

# Adding new repository to GitHub
1. Login to GitHub at https://github.com/ using your credentials
2. Click on the button 'New Repository' on the screen.
3. Create a new repository with any name and copy the url of the new repo
4. Open 'Collaborators' page and grant access to your repository to the team members

# Clone the repository into your local workspace
1. Open git bash client for windows and for mac users open terminal
2. In your github repository you will see a button with clone or download copy the url and in the command prompt, go to the directory where you want to clone the repo and type ``git clone URL which you copied``
3. ``git checkout master`` (By default you will be in master branch, if you are not use the command for checking out master branch from the clone repo)

# How to commit after making changes
1. Make changes in the code or create a new file in the directory
2. ``git status`` (Shows all the changes you made to the repo)
3. ``git add .`` (Add to your local git repo)
4. ``git commit –m “Some meaningful message”`` (Commiting to your local git repo)
5. ``git push origin branch_name`` (Pushing it to remote branch)
6. please enter your email address as username and personal access token added from the above steps

# Creating new branch from any branch
1. ``git status`` (This will provide information on which branch you are on)
2. ``git checkout –b branch_name``
3. ``git push --set-upstream origin branch_name``
4. Make changes and use the same How to commit after making changes instructions to commit and push to the new branch which you created.

# Fetch all remote branches
1. ``git fetch --all``

# List all remote branches after fetch
1. ``git branch -r``

# Delete branch from local and remote
1. ``git branch -d branch_name`` (To force delete use git branch -D branch_name)
2. ``git push --delete origin branch_name``

# Cloning remote branch from github
1. ``git checkout origin/develop`` or ``git checkout develop``
2. ``git pull``

# Create pull request
1. Login to GitHub at https://github.com/ using your credentials
2. Navigate the project you want to contribute
3. Click on Pull Request tab
4. New Pull Request
5. Choose base and master
6. Assign a user to review the changes

# Other way is to use Merge or Rebase (Always use pull request to merge your changes)
1. Merge: Let's say you have created a branch for the purpose of developing a single feature. When you want to bring those changes back to master, you probably want merge (you don't care about maintaining all of the interim commits).
2. Rebase: if you started doing some development and then another developer made an unrelated change. You probably want to pull and then rebase to base your changes from the current version from the repo.

# Fork the existing repo
1. Browse to https://github.com/sheshankgujjari/learn-github
2. On the top right corner click on the fork button
3. A pop up window will show to choose the account where you want to fork
4. Once you click on the account, the repository should appear in your account.
