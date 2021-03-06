
* This chapter is for people who have no experience with git *

#### 1. Initialize a repo

Once you have git installed, the first thing you want to do maight be initializing a repo. Either make your own repo or clone others' repo.

init a repo of your own.
```bash
mkdir learn-git && cd $_
git init
Initialized empty Git repository in /somepath/learn-git/.git/
```
There should be a `.git` folder inside. You can just simply remove this folder if you no longer want the files under git version control.

You can also initialize a repo by cloning others.

```bash
git clone https://github.com/twbs/bootstrap.git
```
this will automatically create a folder named `bootstrap` in the current path. You can also specify another path, for example:
```bash
# this will clone the repo in my-bootstrap folder
git clone https://github.com/twbs/bootstrap.git my-bootstrap

# this will clone the repo in current folder and current paht will be the root
git clone https://github.com/twbs/bootstrap.git .
```

#### 2. Make a first commit

In the new repo you just initialized, let's create a new file and add some random text. Now let's version-control it!

```bash
#try to run this and see the output
git status
#>>output:
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

nothing added to commit but untracked files present (use "git add" to track)

#or run this to see one-line output
git status -s
#>>output:
?? README.md
```
It means that the file `README.md` is not under version control. Now if you run `git add README.md` and `git status` again then see the output.

```bash
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   README.md
```
But you are not done, the file only `staged`(will talk this later) and you still need to `commit` it to repo.

```bash
git commit -m"init"
```

`git commit` will commit all the `staged` changes to your repo. `-m` flag follows with the commit message, this should be a short description to the changes you made.

Now, your file is controlled by git and you shoule see the log of the commit

```bash
git log
#output:
commit 93343c6ce83846a7d217cf04cfd288ed0febb7ab
Author: ruanyl <ruanyu1@gmail.com>
Date:   Sat Aug 1 16:08:19 2015 +0300

    init
```
