git init //建立git仓库，其实是建立.git文件夹，同时本地仓库
git add  <filename>
git commit -m "comment"
git status
git log
git log --pretty=oneline      
git checkout -- <filename>    //让<filename>回到最近一次git commit或git add时的状态；即丢弃共工作区的修改。
git reset HEAD <filename>     //把放入暂存区的修改拉取到工作区，并清空暂存区。
git reset --hard HEAD~<N>/<commitid> //版本切换，同时工作区的修改会被丢弃



git remote add origin git@github.com:michaelliao/learngit.git //给远程仓库起个别名origin，以后都可使用别名origin来替代git@github.com:michaelliao/learngit.git
git clone git@github.com:michaelliao/learngit.git //在本地建立master分支，从远程checkout master分支到本地，将本地master分支和远程master分支关联，切换到master分支。
git checkout -b dev origin/dev //在本地建立dev分支，从远程checkout dev分支到本地，将本地dev分支和远程dev分支关联，切换到dev分支。
git checkout -t dev origin/dev //在本地建立和远程一样的分支（这里是dev），从远程checkout dev分支到本地，将本地dev分支和远程dev分支关联，切换到dev分支。



git push origin master  //把分支master的修改推送到远程仓库origin上。
git push -u origin master  //把分支master的修改推送到远程仓库origin上。并把本地分支


git branch -l //查看本地分支；local
git branch -r //查看远程分支：remote
git branch -a //查看所有分支：all
git branch <branchname> //创建branchname分支
git checkout <branchname> //切换到branchname分支
git checkout -b <branchname> //创建并切换到branchname分支
git merge <branchname> //合并branchname分支到当前分支
git branch -d <branchname> //删除branchname分支




git remote //列出所有的远程主机名
git remote -v //列出所有的远程主机 详细信息；verbose
git remote add <主机名> <网址> //添加远程主机
git remote rm <主机名> //删除远程主机
git remote rename <原主机名> <新主机名> //修改主机名
git remote show <主机名> //显示主机详细信息

git fetch <主机名> [<分支名>]//将某个远程主机的更新，全部取回本地。
                             //"<分支名>"可以忽略，忽略时默认取回所有分支的更新 




git clone [-o <主机名>] <版本库的网址> [<本地目录名>] 
																											//"-o <主机名>"可以忽略，忽略时默认为origin；
                                                      //<本地目录名> 可以忽略，忽略时默认保持和远程一致；
                                                      