hello!!
区域划分：
	工作区   –本地文件夹
	暂存区
	本地仓库
	远程仓库 –如github仓库、gitlab仓库、gitee仓库
git init  #在本地文件夹中创建git本地仓库，有一个“.git”文件。

git add .  #.表示添加所有文件到暂存区，也可以指定文件。

git commit：
git commit -m “这次提交想说的话”

git log：
git log --oneline #简洁版

git status #当前所有文件的状态，是未跟踪、已跟踪还是已提交
		 #未跟踪是指在本地文件夹中，不在其他区域。
		 #已跟踪是指使用了git add命令使这个文件进入暂存区。
		 #已提交是指文件提交到了本地仓库。

git ls-files #查看暂存区文件有哪些。

git reset --soft/hard/mixed 版本号 #退回版本，不想要的当前版本的本地文件可以退回到以前的版本。

git rm 文件名 #表示想要把某个文件从工作区和暂存区同时删除，记得删除后要使用git commit命令提交，本地仓库才会被更改。
#（想要把某个文件从工作区和暂存区同时删除，也可以通过先删除本地文件，再使用git add。）
git rm --cached 文件名 #只删除暂存区文件。
git rm -r * #删除当前目录下的所有文件。

.gitignore #这是一个文件，在里面可以写出添加时想要忽略的文件名。

git remote add 你想给远程仓库起的名字 远程仓库的SSH

git push：
git push -u 远程仓库名字 分支（比如main）

git pull：
git pull 远程仓库名字 分支（比如main）

git remote：
git remote -v #查看远程仓库和它的名字。

git branch #查看分支列表。
git branch 分支名字

git checkout 分支名字 #恢复旧分支或者切换到一个已经存在的分支。
git checkout -b 分支名字 版本号 #恢复分支

git switch 分支名字 #切换分支。（推荐使用这个）

git merge 想要合并的分支的名字 #合并分支前，你需要先回到主分支，它会把你想要合并的分支加到当前分支上。

git branch -d 分支名字 #将已合并的分支删除
git branch -D 分支名字 #将未合并的分支强制删除

git rebase 目标分支名字 #这个命令会将当前的分支分散的部分合并在目标分支的后面

组合命令：
添加并提交：
git add .
git commit -m “我修改了”
git push