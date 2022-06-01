---
description: You can never know enough about git. 
---

# Git

## Understanding git

Git stupidly tracks files and directories. When git stores a new project it stores an entire tree. ie. a whole bunch of blobs of contect and pointers pointing to that content that can be expanded out to form a complete directory.
  
### Git object types
These are the actual data stored within git. They are all stored in the git object database within the `.git` directory.

**The Blob**  
The content of a file is stored in a blob. So in the .git directory, there with be a blob that corresponds to each file. Importantly, it is only the *content* of the file stores in the blob, the name or location of the file is not. So, if you have 2 identical files is two places in your repo, they will only be stored once. 

**The Tree**  
This is the directory structure. The tree is just a list of other tree (subdirectories) and blobs (files).

**The Commit**  
A commit is very simple, it just points to a tree and keeps track of the the author, committer, messsage and the parent commit that directly preceded it.




## Undoing thing
Okay, so git gives you this amazing history of commit messages to help you keep track of everything that has happened in your project. Now, how do we undo mistakes we may havve made. 
One of the most common is adding more changes to a commit youve already made. ```git commit --amend``` overwrides your previous commit and adds the files in your staging area to it. Might look like this.
```
$ git commit -m 'Initial commit'
$ git add forgotten_file
$ git commit --amend
```

if you want to just change the last commit message you made try
`git commit --amend -m"updated comit message"`

see more about undoing things [here](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

How to unstage things from your staging area (things added to git add).
There are lots of different things you may want to do. Suppose you have added something to the staging area and you want to take it out of staging but not actually make any changes to the fil. This may be because you dont want to include it in a commit you wish to make. ```git reset HEAD <file>``` will do that for you.

What if you made changes to a file and actually just want to get rid of all of the changes, and make it look like it did at the last commit (or any other). ```git checkout -- <file>``` will do that for you

[Revent, Restore, Reset](https://stephencharlesweiss.com/git-restore-reset-revert)
## Branching

checkout a remote branch simply by writing ```git checkout remote_branch_name``` even though it doesnt show up in a git branch command, it is still there. A `git branch -a` will show you all branches.

Delete a local branch once it has been used by `git branch -d feature` and you can delete on the remote repository using `git push -d origin feature`

### Notes

Head, Tags, Branches and remotes all just point to a commit, which are directories of blobs (the data stored in git). Commits are just snapshots of your directory at a given point in time. 

You can pipe a diff into a file to see the difference  
```git diff file1.csv file2.csv > the_diff.diff```


To reset the remote path use  
``` git remote set-url origin```


If you are in the middle of a merge conflict and just want to go back to how it was before run a 
`git reset --hard HEAD` - THIS IS A DANGEROUS COMMAND
### Commands

`git restore` - The either helps you to unstage things. Or the restore command can discard local changing, restoring the last commited state. 
`git restore .` - will restore all uncommited files back the state they were in at the previous commit. **This is a dangerous operation** 
`git restore --staged main.py` removes the file from the staged area but keeps the modifications untouched. 

`git fetch -p` - This removes any remote tracking references no that no longer exist of the remote. 

* `git gui` or  `gitk`- for getting up a graphical interface

[Addings SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Links

* [Advanced git for developers](https://www.youtube.com/watch?v=duqBHik7nRo) - youtube video of a conference talk. Very informative. 
* [visual cheatsheet](https://ndpsoftware.com/git-cheatsheet.html#loc=index;) - this is a nice visual website
* [git internals PDF](https://github.com/pluralsight/git-internals-pdf) - look at git object types and git data model. Page 13 onwards
* [Git Pro](http://git-scm.com/book/en/v2)
* [Git documentation](https://git-scm.com/doc)
* [Interactive Visualisation of how git works](https://git-school.github.io/visualizing-git/)
* [git for professionals ](https://www.youtube.com/watch?v=Uszj_k0DGsg\&t=18s\&ab_channel=freeCodeCamp.org)freecodecamp video
* [practicaldatascience](https://www.practicaldatascience.org/html/git_and_github.html) give a short intro to git in thier DS course. Nice beginer intro.
* [Setting up multiple SSH keys for different github account](https://gist.github.com/jexchan/2351996). This was used to be able to read and write to the same EIK repo on both my work and personal laptop. The idea is, that you need to generate a ssh key pair on your work laptop, and then all the public key to citrez account. Then on you work laptop, add to the ssh config, that you should use the (new) private ssh key, when the citrez account is asking for requests. You will also need to add you work account as a collaberator on the project.
[SSH Keys for github](https://jdblischak.github.io/2014-09-18-chicago/novice/git/05-sshkeys.html) - checkout githubs own docs as well
* [The git parable](https://tom.preston-werner.com/2009/05/19/the-git-parable.html) - written by the founder of github. 
