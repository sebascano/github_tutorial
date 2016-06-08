# Basic commands

Once you have a repo, you will make changes over time, you 
will share them with others and will track your
changes locally (that is the hard and easily editable copy
of the repo in your computer).

Git does not have to be connected to github. Github is just 
a very popular way to store and share repositories. It is 
a **GREAT** tool. 

# Transport commands

![](img/githuboverview.png)

Taken from [Oliver Steele's blog](http://blog.osteele.com/posts/2008/05/my-git-workflow/).

# Pushing and pulling

Your commits are local and repositories are just clones of each
other. Such is the nature of a distributed version control system.
You synchronize the changes via `git push` and `git pull`.

You can connect with several different copies of the same source code. 
Locally you will define *nicknames* for this *versions*. Each of 
this versions equates to an actual repo with its clonable url in 
github.
The url you use to clone a repo is by default nicknamed `origin`. 

We will soon talk more about this but for now, you should also understand 
that each of this *nicknamed versions* can have several **branches** which
is just another way of having different copies of the repo. By default,
you will work on branch `master` which is the one that any repo has.
The difference, for now, between the version and the branch is that the
branch will not have its own url on github but lives within the repo.

Everytime you do a `pull` or a `push` by default you connect to the
repository with nickname `origin` and to the branch `master`
so it is equivalent to do

```bash
git pull 
# or
git pull origin master
```

This will become relevant later. 

# Local vs. source


```git
git status
```
Status allows you to view what you have in your local machine, what is in the cloud, etc.

# Adding 

You will obviously want to add changes performed locally to the version control. That
is not the same thing as adding them to github. Again, git is not github.

Once you create some files or make changes on your computer you need to let *git*
know that you want it to pay attention to them (or **track** those files/changes).

Git add is the operation that allows you to quite obviously *add* the changes to 
the **index** (the way git has to keep track of all changes).

Several tips to using `git add`

- `git add .` adds all the *new* files in the corresponding subfolder
- `git add -u .` adds all *modified* files in the corresponding subfolder
- `git add -A` will add *everything* [tread carefully!]

Once you added some changes, it is said you have *staged* them. 
Still, you can easily change your mind by using `git reset HEAD <file>`

# commiting

You can **commit** the staged changes. Commits are the way in which git will
really handle the *versioning* part of the deal. They are basically
**snapshots** of all the files you have staged for commit.

Everytime you commit, you are forced to provide an accompanying message
that summarizes the changes performed. At least, that is the idea.
It would be lovely on your part to actually give informative messages...

![](img/git_commit.png)

All you do is...

```bash
git commit -m "nice simple message here"
```

# pushing

Once commited (you can do it several times) you can syncronise the web
version of da thing to incorporate local changes by using the command
`git push`. That simply updates the remote repo.

