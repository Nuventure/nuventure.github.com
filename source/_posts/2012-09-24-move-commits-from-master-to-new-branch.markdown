---
layout: post
title: "Move commits from master to new branch"
author: Tinu Cleatus
date: 2012-09-24 01:37
comments: true
categories: Git Tips
---

Ever found yourself committing to the master branch instead of having a separate branch for that new feature you are working on ? This handy tip will let you *move* those commits to a separate new branch keeping your master branch untouched. **Note that this would only work if you haven't pushed your changes to remote yet**.

**Create a new branch from master**

```
$ git branch new-changes
```

This would copy over the new commits from master to the newly created branch.

**Remove commits from master**

```
$ git reset --hard HEAD~3
```

where 3 is the number of commits you have already made, that are to be moved over and unpushed to remote.

Now, you have a clean working copy of master branch, while retaining the new commits in the new branch.

Thanks to [Ariejan](http://ariejan.net/) for the tip!