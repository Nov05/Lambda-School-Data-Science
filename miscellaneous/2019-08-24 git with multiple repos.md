
2019-08-24   

# How to use git with multiple remote repositories

Using git with multiple remote repositories  
https://mmikowski.github.io/git-cross-origin/    
How to use git with multiple remote repositories?  
https://github.community/t5/How-to-use-Git-and-GitHub/How-to-use-git-with-multiple-remote-repositories/td-p/19836 

<br>

Push everything to the first GitHub repo (sync local and remote)   
Then use GitHub `pull request` to synchonize the 1st and the 2nd repos   
```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 394 bytes | 394.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git
   4840664..cad6978  master -> master

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git add .

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git commit -m "2019-08-24"
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

Check current remote destinations (there is only one GitHub repo for now)
```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
```

Add a new remote destination (2nd Github repo)  
```
# create a new branch locally
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git checkout -b project-master
Switched to a new branch 'project-master'

# add the 2nd GitHub repo as its remote destination
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git remote add project https://github.com/Build-Week-Safe-Routes/Data-Science.git

# check remote destinations (we have two repos now)
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (fetch)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (push)

# CAUTION: Backup your local repo before this step if you didn't synchronize all repos   
# fetch from the 2nd remote
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git fetch project master
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
From https://github.com/Build-Week-Safe-Routes/Data-Science
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> project/master

# tell your local brach 'project' to track remote branch 'master'
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git branch --set-upstream-to=project/master
Branch 'project-master' set up to track remote branch 'master' from 'project'.
```

Now we are all set. Check the `.git/config` file in your local repo.

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
[branch "master"]
	remote = origin
	merge = refs/heads/master
[remote "project"]
	url = https://github.com/Build-Week-Safe-Routes/Data-Science.git
	fetch = +refs/heads/*:refs/remotes/project/*
[branch "project-master"]
	remote = project
	merge = refs/heads/master

```


If you want to remove one of the remote destination `project`.

```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git remote remove project

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
```

## Push to the 2nd GitHub repo

> $ git add .
> $ git commit -m <message>
> $ git push project HEAD:master
```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git add .

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git commit -m "2019-08-24 test pushing to both remote repos"
[project-master e595e8e] 2019-08-24 test pushing to both remote repos
 1 file changed, 1 insertion(+), 1 deletion(-)
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git push project HEAD:master
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 897 bytes | 448.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/Build-Week-Safe-Routes/Data-Science.git
   e653056..e595e8e  HEAD -> master
```

## Push to the 1st GitHub repo
```
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (project-master)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

# make some changes to the local repo  
*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git add .

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git commit -m "2019-08-24 test pushing to both remote repos"
[master a90edb0] 2019-08-24 test pushing to both remote repos
 1 file changed, 1 insertion(+), 1 deletion(-)

*@laptop MINGW64 /d/lambdaschool/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes (master)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 387 bytes | 387.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git
   cad6978..a90edb0  master -> master
```


