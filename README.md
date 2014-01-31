github_tutorial
===============

Mini tutorial enphasizing uses in multidisciplinary projects! Git/github is not just for coders!

*If you also love git and are trying to get your team to use it, feel free to contribute!

***

Installation
------------

###Windows
The *first* and most important thing you have to ask yourself is: why, why, why am I **still in windows**? 

The *second* thing to ask yourself is why do I keep **doing this to myself**?

If you choose not to heed this advice, [here's](http://msysgit.github.io/) what you gotta do to have git on windows.

###Linux

####Fedora 
```bash
$ yum install git-core
```

####Debian
```bash
$ apt-get install git
```

###Mac
Hahaha you spent a LOT of money! Don't be so *fresa*
Did you see how **easy** it was for linux users? There is two ways for you:

1. [Via the git installer](http://code.google.com/p/git-osx-installer)
2. With [MacPorts](http://www.macports.org) installed:

```bash
$ sudo port install git-core +svn +doc +bash_completion +gitweb
```
***
The basic global setup
----------------------

Git (or github) is in my opinion a pretty awesome way to work in teams bacuase it facilitates sharing and integrating work and it makes everyone accountable for the tasks they have assigned. 

For the second reason, you have to tell github who you are.

```git 
$ git config --global user.name "Your Name"
$ git config --global user.email "your_email@whatever.com"
```

Once you do this, everything that you upload/update/do will have attached your name in the history of your repo (accountability FTW!)

One last thing

If on a mac add also
```git
$ git config --global core.autocrlf input
$ git config --global core.safecrlf true
```
If on windows add also
```git
$ git config --global core.autocrlf true
$ git config --global core.safecrlf true
```
This will setup line ending preferences.

Pimping it up some mo'!
-----------------------
You can also tell git which editor you prefer (obviously, my example is with emacs but you plug in your favourite!)
```git
$ git config --global core.editor emacs
```
Lastly, for resolving merge conflicts, you can setup where you want to do it!
```git
$ git config --global merge.tool emerge
```

Lets check out our setup:
```git
$ git config --list
```

[More info on setup.](http://git-scm.com/book/en/Getting-Started-First-Time-Git-Setup)

***
Getting help
------------
No one (and I mean **no one** knows everything. Knowing how to access the documentation is always your best bet.

To access git's manpage just do
```git
$ git help <verb>
$ git <verb> --help
$ man git-<verb>
```
where <verb> refers to any command you want! (if you know not any command, ask google what you wanna do and start checking out all the possibilities to make your life easier!)


***
What is this weird (but awesome) .md file?
------------------------------------------
To write beautiful stuff (like this document), use markdown! It really is awesome.

For an [amazing cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet#wiki-hr)

Incidentally, your can export an md directly into a presentation! For those RStudio users, [checkout this one](http://www.rstudio.com/ide/docs/authoring/using_markdown)








