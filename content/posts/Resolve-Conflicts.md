---
title: "Resolving GitHub Merge Conflicts"
date: 2021-03-15T18:44:37Z
draft: true
---

# How to Resolve GitHub Merge Conflicts?

Here I'll mention how I resolve GitHub Conflicts. I'm sure there are much easier and better methods to do so, but this is just for me to remember how I have done it for future reference.

## Step 1

A Pull Request that you have created might have conflicts or someone has made a Pull Request to your repository that has conflicts. To resolve these conflicts you can either use the web GitHub UI and resolve those Conflicts or use the command line. In some cases when the web UI is not an option and you are compelled to use the command. 

If you have to use your command line to resolve these merge conflicts you'll need a terminal. This terminal must be connected to your relevant GitHub repository. 

If you don't know how to do so on your on local terminal, you can simply use gitpod or another online extension like gitpod. The link to your gitpod terminal will be `https://gitpod.io/#<github repo link>`. Over here you have to replace `<github repo link>` with the **complete link of your GitHub repository (including the `https://` and everything else in the link)**.

## Step 2

Now that you have your terminal open, you set your branch to the branch from with the PR is coming. To do so you must type `git checkout <branch name>`, where you replace `<branch name>` with the relevant branch in relation to your PR.

## Step 3

Now in your terminal you are at your branch relevant to your PR. Now you'll have to get your PR from GitHub onto your terminal. 

To do so, type `git pull <repo link>.git <branch name>`. Here in the place of `<repo link>` add the link to your repository in relation to your PR (Make sure to add the `.git` at the end of the link without a space after the link) and in the place of `branch name` add the branch from which you are pulling/pushing changes.

## Step 4

Now that you have your PR in your terminal you'll have to resolve conflicts. This is the most important and critical step.

Understanding how to resolve conflicts might be difficult, so I'll try to explain it the best way I can over here.

Once you have got your PR in your terminal it will mrntion that files `x, y, z, etc...` have merge conflicts. You have to keep all these files in mind because your PR will never get pushed to your repository unless you manually resolve all merge conflicts in all files that have them. 

If you are using gitpod, as soon as you get your PR from your repository, a bunch of files will have symbols on them (like `C or M or U`). The files that have conflicts are the files with the symbol `C`. Only the files with this label are relevant here as these are the file that have merge conflicts. (`M` means can be merged and `U` means has been added, you might not see all symbols).

Now you'll have to open all files with merge conflicts and resolve conflicts. But how do I know where are the conflicts and how to understand them and resolve them? This is what I'll be mentioning below.

Once you open the files which have merge conflicts search for something that will look like this...

`<<<<< HEAD`    # instead of `HEAD` your branch name relevant to your PR.

If you notice, by scolling lower or right below it you will even see something like this...

`=====`

and then after scrolling lower again (or right below it) you will see something like this...

`>>>>> master`   # instead of `master`, the branch to which the PR should be pushed. Might even be a random set of numbers and letters (your latest commit).

These are the merge conflicts.

To resolve these conflicts you need to understand what it means. That's what I'll explain to you now.

1. Everything that is in between `<<<<< HEAD` and `=====`:

These are what have been done in your repository which is not present in the master or head repisitory.

2. Everything that is in between `=====` and `>>>>> master` 

These are what have been done in the master or head repository that is not present in your repository.

You can either leave it at what has been done in the master or head repository by deleting everything in between `=====` and `>>>>> master` and also making sure to remove the `<<<<< HEAD`, `=====` and `>>>>> master`.

or 

You can keep only your changes and ignore what has been additionally in the master or head repository by deleting everything in between `<<<<< HEAD` and `=====` and also making sure to remove the `<<<<< HEAD`, `=====` and `>>>>> master`.

Do this for all places in that file where you find conflicts. Once that is done, move on to the next file and do the same there too. Do this until merge conflicts in all files have been resolved.

**Do note that if you are using gitpod then the `C` label will not go even if all conflicts have been resolved.**

**Be sure to save all conflicts that you have resolved by going to each file induvidually and clicking `ctrl+s`. You don't want to loose all the work you have done in resolving conflicts.**

## Step 5

Now you've completed to major part, you just need to push your changes to GitHub.

To do so simply type in your same terminal,

```bash
git add . -A
git commit -m "Resolve Merge Conflicts"  # What is under the quotes is subject to change. You can name you commit whatever you would like to name it to.
git push --force origin <branch name>  # This must be same as the branch name you added in step 1
```

Now you are finally done and your conflicts have been resolved and pushed!!
