# Week 3 Data Science Lab - Solutions

## Collaborative Data Science

### Short answer

```bash
$ git revert 2e185d8e
$ git merge origin/fix_bug
$ git merge origin/feature_validation
$ git push
```

### Long answer

There are multiple ways of solving this exercise, so don't worry if you did a bit differently, as long as you end up with something working.

First let's have a look at the git repository content. You can either use the "graph" view from gitlab or

```
git log --graph --pretty=oneline --abbrev-commit
```

Exploring further you will notice that the commit ```2e185d8e``` accidentally removes two important files. You will first need to revert it.
For doing that you have two options: either you revert the action of this commit, adding a new one that does the opposite (```git revert 2e185d8e```) or you set the master branch pointer to the state just before this commit (```git reset --hard e1a56418```). The revert is preferred here because it doesn't rewrite past history and thus doesn't need to "force push" (which is blocked by default on the master branch on gitlab).

Then you will also notice the two branches ```fix_bug``` and ```feature_validation```. From gitlab interface or by doing ```git checkout <branch>```, you can explore the changes they apply, in this case fixing a bug and adding some input validation. This is exactly what you need to make the tests pass. So you can merge the branches on master with

```
git merge origin/fix_bug
git merge origin/feature_validation
```

You can omit the "origin/" in the branch name if you have them locally. For example this would be the case if you had checkout onto them before.


