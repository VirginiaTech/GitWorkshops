# GitWorkshops
Welcome to our GitHub workshop. Get ready to learn all about the basics of using GitHub. Below are list of useful links and commands that we'll be using throughout this workshop. If you'd like to see our full presentation [click here](https://docs.google.com/presentation/d/e/2PACX-1vSJ3RUco-cA7sxMaIPcdS86nhlFSYUD4YOYhlSQD5I2RuCsCpAbUHk2ziOIeqBZy34ISkOd5ozTpcPX/pub?start=true&loop=false&delayms=5000 "Workshop Presentation")

# Set Up
Begin by 
1. [downloading git](https://git-scm.com/downloads "Git Downloads")
2. [creating your GitHub account](https://github.com "GitHub Homepage")

# Basic Linux Commands
These are the Linux commands that you'll be using in Git Bash (which you've just downloaded)  

&nbsp;&nbsp;&nbsp;`ls` shows files and folders (aka directories)  
&nbsp;&nbsp;&nbsp;`mkdir <folder_name>` makes a new directory  
&nbsp;&nbsp;&nbsp;`cd <directory_path>` changes directory to the specified path  
&nbsp;&nbsp;&nbsp;`touch <file_name>` used to update access date of file/directory  
&nbsp;&nbsp;&nbsp;`cp <file_name> <new_file>` copies contents of `<file_name>` to `<new_file>`  
&nbsp;&nbsp;&nbsp;`mv <file_name> <new_file>` moves `<file_name>` and it's contents to another location/name  
&nbsp;&nbsp;&nbsp;`rm [-rf] <file_name>` removes file (`-rf` tag removes folders and their contents, recursively)

# Basic Git

## [Forking](https://guides.github.com/activities/forking/ "GitHub Guides: Forking")
Forking is a **GitHub** feature that creates a copy of a repository in your account. Begin by going the repository's web page.
1. Fork to your personal account by clicking the **"Fork"** button in the upper right hand corner.
2. Invite your teammates to join your forked repository by going to the **"Settings"** page of the repository.
3. Select the **"Collaborators"** tab from the sidebar on the left and enter your teammates' usernames.

## [Cloning](https://git-scm.com/docs/git-clone "Git Clone")
Copy the **HTTPS** URL from the repository. Before you use this URL, be sure to change to the directory where you'd like for the repository to be saved on your local machine. The sequence of events 

```
cd git-repos/
git clone <url>
``` 
Now it is on your local machine. See for yourself by using the `ls` command!

## [Status](https://git-scm.com/docs/git-status "Git Status")
Displays the working tree's status.
```
git status
``` 
Red changes are *not* staged for commit, whereas green changes are staged for commit.

## Uploading to Your Repository
In general, the basic flow of updating the repository based on your changes is to [add](https://git-scm.com/docs/git-add "Git Add"), [commit](https://git-scm.com/docs/git-commit "Git Commit"), and [push](https://git-scm.com/docs/git-push "Git Push").

```
git add .
git commit -m "A descriptive message"
git push
```

## [Reset](https://git-scm.com/docs/git-reset "Git Reset")
This is how you can **unstage** files that have been staged for a commit.

```
git reset .
```

## [Pull](https://git-scm.com/docs/git-pull "Git Pull")
Pulling updates your local machine with the latest changes made to the remote repository.

```
git pull
```

## [Merge Conflicts](https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/ "Resolving Merge Conflicts")
If you are given an error when attempting to `git push`, often times the error is because your local repository is not up to date which can be solved by `git pull`. However, if you pull and run across a **CONFLICT** message you'll need to open the file with the conflict and resolve them.

Code that is between the `<<<<<<< HEAD` and `=======` are changes that you've made.  
Code between the `=======` and `>>>>>>> <commit_id>` is what is located in the remote repository.

Simply delete the conflict markers and the line you don't need (or don't delete either line if you'd like to keep both).


## [Initializing](https://git-scm.com/docs/git-init "Git Init")
Initializes a non-git directory into a git repository.  
It does **NOT** automatically put itself onto GitHub.  

First, create a directory that you'd like to turn into a git repository. Change to that directory and make some files. Finally, initalize the directory into a git repository!
```
mkdir <folder_name>
cd <folder_name>
touch <file_name>
git init
```

For your local Git repository to exist on GitHub you have to go the GitHub's website and create a new repository. On the [GitHub homepage](https://github.com/ "GitHub HomePage"), click the **"New repository"** button on the lower right hand corner. Copy the URL from this new repository to use in the following commands:
```
git remote add origin <url>
git remote --set-upstream origin master
```
