# Git Basics

## Getting a Git Repository
````bash
git init # initialize a git repository from a local directory.
git clone <url> # clone* an existing git repository from elsewhere.
git clone <url> <newname> # clone an existing git repository and rename it.
````
\* Pulls down all the data for that repository, and checks out a working copy of the latest version.

## Recording Changes to the Repository
![](./images/file-states.png)
Figure 1. File state in the working directory.

![](./images/lifecycle.png)
Figure 2. The lifecycle of the status of the files.

### status
````bash
git status # show the working tree status
````
### add
`git add` add precisely this content to the next commit.

````bash
git add <filename> # *add file contents to the index
````
\* The index is a binary file (generally kept in `.git/index`) containing a sorted list of path names, each with permissions and the SHA1 of a blob object; `git ls-files` can show you the contents of the index. Please note that words index, stage, and cache are the same thing in Git: they are used interchangeably.

## Reference
[Git: Understanding the Index File](https://mincong-h.github.io/2018/04/28/git-index/)

[Home](https://github.com/lolimay/Pro-Git-Reading-Notes) | [Previous](./1-Getting-Started.md)