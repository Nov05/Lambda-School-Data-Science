2019-08-24

Remote repos:   
`Repo 1` https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes  
`Repo 2` https://github.com/Build-Week-Safe-Routes/Data-Science

`Local Repo` is cloned from `Repo 1`.

### 1. check remotes
```
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
```

### 2. add `Repo 2` url to origin   
```
$ git remote set-url --add --push origin https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
origin  https://github.com/Build-Week-Safe-Routes/Data-Science.git (push)
```

### 3. make some changes to the `Local Repo` and push to `Repo 1` and `Repo 2`  
```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git add .

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git commit -m "2019-08-24"
[master f44e1ed] 2019-08-24
 1 file changed, 1 insertion(+), 1 deletion(-)

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 294 bytes | 294.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes
   f44e1ed..9e59829  master -> master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 294 bytes | 294.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Build-Week-Safe-Routes/Data-Science
   f44e1ed..9e59829  master -> master
```

**In the `Local Repo`, the `.git/config` file looks like this now.**
```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git
	fetch = +refs/heads/*:refs/remotes/origin/*
	pushurl = https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git
	pushurl = https://github.com/Build-Week-Safe-Routes/Data-Science.git
[branch "master"]
	remote = origin
	merge = refs/heads/master
```

