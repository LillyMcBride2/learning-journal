# Git and git bash

Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version 
control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By 
utilizing a Version Control System (VCS), mistakes with files can easily be rectified. There have been several different kinds of version
control systems over the years. Originally all changes were saved on one local machine. Eventually we came up with centralized version 
control systems which saved projects to a centralized server so that multuple developers could work on the same code from different
machines. The only problem here was that if something happened to the centralized server, all work would be lost. Git is what we call a
distributed version control system. This means that each local machine has its own saved repository which is a clone of the repository 
living on the centralized server, GitHub. Each time you make a commit, Git creates a snapshot of the file and stores a reference to it.

Files in Git can reside in three main states: committed, modified and staged. Committed ata is securely stored in a local database. 
Modified files have been changed but not committed to the database. A staged file’s changed version has been flagged to be committed 
in the next snapshot. An inherent Git tool called git config allows the setting of configuration variables that control aspects of Git’s
operation and look. To check settings, use the git config --list command. There are three ways to get more information on a particular 
command, by accessing the manual: git help command OR git command --help OR man git-command.

To import an existing project or directory into Git, follow these steps using the Terminal or Command Line:

Switch to the target project’s directory
Example:
$ cd test (cd = change directory)
Use the git init command
$ git init
Note: At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.

To start tracking these repository files, perform an initial commit by typing the following:
$ git add *.c
$ git add LICENSE
$ git commit -m “any message here”
Now, your files are tracked and there’s an initial commit.

You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

$ git clone https://github.com/test
By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called
“test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The 
command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

To clone a repository into a directory with another name of your choosing, use the following command format:

$ git clone https://github.com/test mydirectory
The command above makes a copy of the target repository in a directory named “mydirectory.”

The local Git repository has three components:

Working Directory: The actual files reside here.
Index: The area used for staging
Head: Points to the most recent commit

All files in a checked out (or working) copy of a project file are either in a tracked or untracked state. Tracked files can be 
modified, unmodified, or staged; they were part of the most recent file snapshot. Untracked files were not in the last snapshot 
and do not currently reside in the staging area.

The Life Cycle of File Status:
1. After you edit a file, Git flags it as modified because of changes made after the previous commit.
2. You stage the modified file.
3. Then, you commit staged changes.

Track one file only by using the following format:
git add filename
Track all files in a repository by using the following command:
$ git add *

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.

After staging one or multiple files, you should commit the changes and record what you did within the commit message:
$ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.

Next, you would push changes to a remote repository. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ git push origin master
*This command pushes changes from the local “master” branch to the remote repository named “origin”.

*For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to 
your local repository. However, these names can be changed by the user.

When you are not ready to commit changes but do not want to lose them either, git stash is a great option. This command temporarily 
removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply 
use the git stash apply command to retrieve the hidden changes.

In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a 
network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote 
repositories to push information to and pull data from.

As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and
the name “master” to your local branch.

By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

$ cd example
$ git remote -v
remote1 https://github.com/remote1/example (fetch)
remote1 https://github.com/remote1/example (push)
remote2 https://github.com/remote2/example (fetch)
remote2 https://github.com/remote2/example (push)
remote3 https://github.com/remote3/example (fetch)
remote3 https://github.com/remote3/example (push)
