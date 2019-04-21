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
git stats --short # show the working tree status in a more compact way
````
### add
`git add` add precisely this content to the next commit.

````bash
git add <filename> # *add file contents to the index
git add -A # add all modified and untracked files to the index
````
\* The index is a binary file (generally kept in `.git/index`) containing a sorted list of path names, each with permissions and the SHA1 of a blob object; `git ls-files` can show you the contents of the index. Please note that words index, stage, and cache are the same thing in Git: they are used interchangeably.

## Ignoring Files
`.gitignore` ignore specific files that git will not try to track them.

> The rules for the patterns you can put in the .gitignore file are as follows:
> - Blank lines or lines starting with # are ignored.
> 
> - Standard glob patterns work, and will be applied recursively throughout the entire working tree.
> 
> - You can start patterns with a forward slash (/) to avoid recursivity.
> 
> - You can end patterns with a forward slash (/) to specify a directory.
> 
> - You can negate a pattern by starting it with an exclamation point (!).

### diff
`git diff` Show changes between commits, commit and working tree, etc.
````bash
git diff # to see what you've changed but not staged (compare working directory with staging area)
git diff --staged # *compare staged changes and the last commit
````
\* `git diff --staged` == `git diff --cached`

### commit
`git commit` Record changes to the repository.

````
git commit -m "commit message" # commit with single line commit message
git commit # call core.editor and input multi-lines commit message
````

## Reference
1. [Git: Understanding the Index File](https://mincong-h.github.io/2018/04/28/git-index/)
2. [Good .gitignore file examples](https://github.com/github/gitignore)

[Home](https://github.com/lolimay/Pro-Git-Reading-Notes) | [Previous](./1-Getting-Started.md)
