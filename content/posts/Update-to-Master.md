---
title: "Update your fork to the latest master build"
date: 2021-03-15T18:44:37Z
draft: true
---

# How to Update your fork to the latest master build?

To update your fork to the latest commit in the master repository, you'll first need a terminal. This terminal has to be connected to your repository, otherwise it will not work. If you do not know how to get your local pc terminal connected to GitHub, you can use gitpod. The link to your browser extension gitpod terminal would be `https://gitpod.io/#<github repo link>`, where you replace  `<github repo link>` with the complete link of your GitHub fork of the repository (including the `https://` and the entire link.

Now that you have opened your terminal, you'll have to know what the name of the branch in the head repository is. Once you know that, begin typing this in your terminal.

```bash
git checkout <branch name>
git fetch upstream <branch name>
git reset --hard upstream/<branch name>
git push --force
```

In the above commands, replace `<branch name>` with the name of the branch of the repository that you want to update.

Now you're done and have updated to the latest version of your master repository! Do note that this will remove all changes that you have made that has made your repository fork ahead of the head or master repository.
