## Where does Git store information?

Each of your Git projects has two parts: the files and directories that you create and edit directly, 
and the extra information that Git records about the project's history. The combination of these two things is called a **repository**.  

Git stores all of its extra information in a directory called `.git` located in the root directory of the repository. Git expects this 
information to be laid out in a very precise way, so you should never edit or delete anything in `.git`.  

Suppose your home directory `/home/repl` contains a repository called dental, which has a sub-directory called data. Where is information about the history of the files in `/home/repl/dental/data` stored?

Answer: /home/repl/dental/.git

## How can I check the state of a repository?

When you are using Git, you will frequently want to check the status of your repository. To do this, run the command `git status`, 
which displays a list of the files that have been modified since the last time changes were saved.

How can I tell what I have changed?

Git has a **staging area** in which it stores files with changes you want to save that haven't been saved yet. 
Putting files in the staging area is like putting things in a box, while **committing** those changes is like putting that box in the mail: 
you can add more things to the box or take things out as often as you want, but once you put it in the mail, you can't make further changes.  

`git status` shows you which files are in this staging area, and which files have changes that haven't yet been put there. In order to compare 
the file as it currently is to what you last saved, you can use `git diff filename`. `git diff` without any filenames will show you all the 
changes in your repository, while `git diff directory` will show you the changes to the files in some directory.
