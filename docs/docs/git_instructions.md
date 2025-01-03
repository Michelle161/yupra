---
layout: default
title: Git Instructions
nav_order: 2
---

# Git Instructions
{: .no_toc }

Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## General workflow

We will be using github to manage uploading our results for the project and sharing work

[![](../images/git_workflow.png)](https://dev.to/ambujsahu81/create-a-simple-github-actions-workflow-347n)

[Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)

## First time setup: how to install the project repository  

### Fork the repo

Navigate to [https://github.com/jbirky/yupra](https://github.com/jbirky/yupra) on your browser. In the upper right corner, select the `Fork` button:

![](../images/fork1.png)

Choose yourself as the owner for the forked repo and check "copy main branch only":

![](../images/fork2.png)

(Note: Step 1 only needs to be done once.)

### Clone repo to local computer

Now we want to `clone` our fork of the repository onto our local machine. We can put this in the same `research/` directory as our other files. 
To do this, change directories to your `research/` folder:
```bash
cd ~/research
```
Within the `research` directory, download the repo by using the `clone` command (and replacing `jbirky` in the url with your own github username):

```bash
git clone https://github.com/jbirky/yupra
```

If you type `ls`, you should now see all of the packages we've downloaded plus the yupra repo:
```bash
/research
	/alabi
	/vplanet
	/vplanet_inference
	/yupra
	...
```

Now we'll create a new folder within the yupra project to store our code and results. To do this, navigate to yupra directory and create a new folder with your name:
```bash
cd yupra
mkdir jbirky
```
This is the folder where you'll add all the code that you write (note: you only need to create this folder once).

## Commit and push changes results to your fork

Copy the tutorial files to your personal folder:
```bash
cp -r tutorials/ jbirky/tutorials 
```

Now if you type 
```bash
git status
```
you can check that git has tracked that new files have been added or modified, and the status command should show something like
```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	jbirky/

```

To take changes we've made on our local machine and upload them back to our repo fork, we need to `add` the new files, `commit` the changes with a commit message, and `push` them to upload:
```bash
git add jbirky/
git commit -m "copy tutorials"
git push
```
now if you go back to the webpage of your fork https://github.com/username/yupra, you should see that your new files have been uploaded.

## Pull requests: update the main repository with your code

Go to the webpage of your fork https://github.com/username/yupra, and in the upper right select `Contribute`:

![](../images/fork4.png)

This will now create a pull request, allowing your fork `username/yupra` to be merged with the main repo `jbirky/yupra`.


## Syncing: update your fork with changes from the main repo

Go to the webpage of your fork https://github.com/username/yupra, and in the upper right select `Sync fork`:

![](../images/fork4.png)

This will sync changes made by others from the main repo `jbirky/yupra` to your own fork fork `username/yupra`. Then to update the code on your local computer, go to your `research/yupra` directory and pull the latest version of your fork:

```bash
git pull
```


## For more instructions see here

- [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)

- [How to fork a repo](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)

- [How to update your fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)