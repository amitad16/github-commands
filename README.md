# github-commands


**1. Create a branch your master branch**
```
git checkout better_branch
git merge --strategy=ours master    # keep the content of this branch, but record a merge
git checkout master
git merge better_branch             # fast-forward master up to the merge
```
[https://stackoverflow.com/questions/2763006/make-the-current-git-branch-a-master-branch](https://stackoverflow.com/questions/2763006/make-the-current-git-branch-a-master-branch)

**2. Delete a remote branch**
```
$ git push --delete <remote_name> <branch_name>
```

**3. Delete a local branch**
```
$ git branch -d <branch_name>
```

**4. Merge branch b into a**
```
git checkout a (you will switch to branch a)
git merge b (this will merge all changes from branch b into branch a)
git commit -a (this will commit your changes)
```
