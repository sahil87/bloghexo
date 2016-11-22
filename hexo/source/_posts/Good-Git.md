---
title: Good Git!
date: 2016-11-22 20:26:16
tags:
---
Most used (but yet unremembered git commands):

### To delete remote branches
```
git push origin --delete branch_to_delete
```

### Tags
```
npm version patch/minor/major #Changes packages.json and applies git tag
git push origin v1.5 (or) git push origin --tags
git tag v1.5 (lightweight tag)
git tag -a -f -m "my version 1.4" v1.6 (annotated tag)
git push --tags (or) git push upstream v2.3.3
git tag -l "v1.8.5*" (list tags)
git show v1.4
```

### To undo commit
```
git commit -m "Something terribly misguided"
git reset --soft HEAD~
<< edit files as necessary >> 
git add ... 
git commit -c ORIG_HEAD
```
* `git reset --soft HEAD~1` doesn't remove the changes from index (i.e. `git commit` adds them again, no need to git add.).
* `git reset HEAD~1` undoes the commit, removes changes from index but keeps the changes locally
* `git reset --hard HEAD~1` removes the changes from the filesystem too.

### More awesome references:
* How to use git: https://guides.github.com/activities/contributing-to-open-source/#contributing
* How to write git commit messages: http://chris.beams.io/posts/git-commit/
* Commit guidelines: http://contribute.jquery.org/commits-and-pull-requests/#commit-guidelines
* Git reset/revert: https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting/
* Easy git rebase: http://hackalyst.info/easy-git-rebase/
* Real git rebase: http://hackalyst.info/real-rebase/
* A few git tricks: http://prakhar.me/articles/a-few-git-tricks/