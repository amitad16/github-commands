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
info: *remote_name* in most cases is *origin*

**3. Delete a local branch**
```
$ git branch -d <branch_name>
```

**4. Merge branch *b* into *a***
```
git checkout a (you will switch to branch a)
git merge b (this will merge all changes from branch b into branch a)
git commit -a (this will commit your changes)
```

**5. List all branches**
`git branch`
or
`git branch -b`

**6. Switch to branch b**
`git checkout b`









# MONGODB COMMANDS

**1. Remove a member from replica set**

https://docs.mongodb.com/manual/tutorial/remove-replica-set-member/

*Run in 1st terminal*
```
mongod --port <PORT> --dbpath /data/<DB_PATH> --replSet <REPLICASET_NAME>
```

*Run in 2nd terminal*
```
mongo --port <PORT>
```

*Inside Mongo REPL*
```
cfg = rs.conf()
cfg.members.splice(2,1)
rs.reconfig(cfg)
```


# UBUNTU COMMANDS

**1. Get all Ubuntu Processes**
```
sudo netstat -lnp
```

**2. Kill a Ubuntu Process**
https://www.cyberciti.biz/faq/stop-process-ubuntu-linux-command/
```
kill -s 15 PID
```

OR
https://stackoverflow.com/questions/9346211/how-to-kill-a-process-on-a-port-on-ubuntu
```
sudo kill -9 `sudo lsof -t -i:9001`
```


# USEFUL APPLICATIONS

**1. localtunnel**
Used for serving localhost running application in www

`lt -h "http://serverless.social" -p PORT ---subdomain SUBDOMAIN`

# OTHER COMMANDS

### SSH

**1. Test SSH connection to github**
```
ssh -T git@github.com
```


**2. Add ssh identity to terminal**

```
eval "$(ssh-agent -s)"
```

`ssh-add <path to ssh private key>`
