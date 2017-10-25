# GitWorkshops
Welcome to our GitHub workshop. Get ready to learn all about the basics of using GitHub. Below are list of useful links and commands that we'll be using throughout this workshop.

Set Up
======
Begin by 
1. [downloading git](https://git-scm.com/downloads "Git Downloads")
2. [creating your GitHub account](https://github.com "GitHub Homepage")

Basic Linux Commands
======
These are the Linux commands that you'll be using in Git Bash (which you've just downloaded)  

&nbsp;&nbsp;&nbsp;`ls` shows files and folders (aka directories)  
&nbsp;&nbsp;&nbsp;`mkdir <folder_name>` makes a new directory  
&nbsp;&nbsp;&nbsp;`cd <directory_path>` changes directory to the specified path  
&nbsp;&nbsp;&nbsp;`touch <file_name>` used to update access date of file/directory  
&nbsp;&nbsp;&nbsp;`cp <file_name> <new_file>` copies contents of `<file_name>` to `<new_file>`  
&nbsp;&nbsp;&nbsp;`mv <file_name> <new_file>` moves `<file_name>` and it's contents to another location/name  
&nbsp;&nbsp;&nbsp;`rm [-rf] <file_name>` removes file (`-rf` tag removes folders and their contents, recursively)

Basic Git
======

## Initializing

[Forking](https://guides.github.com/activities/forking/ "GitHub Guides: Forking")
------
Forking is a **GitHub** feature that creates a copy of a repository in your account.  
1. One person will fork to their personal account by clicking the **"Fork"** button in the upper right hand corner.
2. Invite your teammates to join your forked repository by going to the **"Settings"** page of the repository.

## [Cloning](https://git-scm.com/docs/git-clone "Git Clone")
Copy the **HTTPS** URL from the repository. Before you use this URL, be sure to change to the directory where you'd like for the repository to be saved on your local machine. The sequence of events 

```bash
cd git-repos/
git clone <url>
``` 
Now it is on your local machine. See for yourself by using the `ls` command!

## [Status](https://git-scm.com/docs/git-status "Git Status")

```bash
git status
``` 
Red changes are *not* staged for commit, whereas green changes are staged for commit.

## Uploading to Your Repository
In general, the basic flow of updating the repository based on your changes is to [add](https://git-scm.com/docs/git-add "Git Add"), [commit](https://git-scm.com/docs/git-commit "Git Commit"), and [push](https://git-scm.com/docs/git-push "Git Push").

```bash
git add .
git commit -m "A descriptive message"
git push
```

## [Reset](https://git-scm.com/docs/git-reset "Git Reset")
This is how you can **unstage** files that have been staged for a commit.

```bash
git reset .
```

## [Pull](https://git-scm.com/docs/git-pull "Git Pull")

```bash
git pull
```

## Merge Conflicts
If you are given an error when attempting to `git push`, often times the error is because your local repository is not up to date which can be solved by `git pull`. However, if you pull and run across a **CONFLICT** message you'll need to open the file with the conflict and resolve them.
