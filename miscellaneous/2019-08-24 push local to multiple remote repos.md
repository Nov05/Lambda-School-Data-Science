2019-08-24

Remote repos:   
`Repo 1` https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes  
`Repo 2` https://github.com/Build-Week-Safe-Routes/Data-Science

`Local Repo` is cloned from the `Repo 1`.

1. add `Repo 2` url as remote with name `project`
```
$ git add remote project https://github.com/Build-Week-Safe-Routes/Data-Science
```

2. check remotes
```
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (fetch)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (push)
```

3. add `Repo 2` url to origin   
```
$ git remote set-url --add --push origin https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes
$ git remote -v
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (fetch)
origin  https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes.git (push)
origin  https://github.com/Build-Week-Safe-Routes/Data-Science.git (push)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (fetch)
project https://github.com/Build-Week-Safe-Routes/Data-Science.git (push)
```

4. make some changes to the `Local Repo` and push to `Repo 1` and `Repo 2`  
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
Writing objects: 100% (3/3), 292 bytes | 292.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Build-Week-Safe-Routes/Data-Science
   fde9c09..f44e1ed  master -> master
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/Nov05/DS-Unit-3-Sprint-4-Build-Week-Safe-Routes
   fde9c09..f44e1ed  master -> master
```

