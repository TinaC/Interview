# Git

## What the difference between `git merge` & `git rebase`?

The first thing to understand about `git rebase is that it solves the same problem as git merge.
Both of these commands are designed to integrate changes from one branch into another branch—they just do it in very different ways.

```sh
git checkout feature
git merge main

# or
git merge feature main
```

This creates a new “merge commit” in the feature branch that ties together the histories of both branches.
多一个 merge commit.

- 优点

> Merging is nice because it’s a non-destructive operation. The existing branches are not changed in any way.

- 缺点

On the other hand, this also means that the feature branch will have an extraneous merge commit every time you need to incorporate upstream changes.
If main is very active, this can pollute your feature branch’s history quite a bit.
While it’s possible to mitigate this issue with advanced git log options, it can make it hard for other developers to understand the history of the project.

## git rebase

```sh
git checkout feature
git rebase main
```

This moves the entire feature branch to begin on the tip of the main branch, effectively incorporating all of the new commits in main.
But, instead of using a merge commit, rebasing re-writes the project history by creating brand new commits for each commit in the original branch.

The major benefit of rebasing is that you get a much cleaner project history.

https://www.atlassian.com/git/tutorials/merging-vs-rebasing

## What the difference between `git fetch` & `git pull`?
