## Git命令提交代码

#### 1. 使用顺序

* git add .     //向仓库中添加修改的内容
* git commit -m 'description'     //提交此次修改
* git pull origin <仓库名>      //拉下远程仓库的代码(你需要合并进去的那个仓库)
* git status       //查看哪些文件修改了，并解决冲突
* git add .         //冲突解决完成后再次add
* git commit -m 'description'     
* git push origin head        //push到当前分支上去
* 在bitbucket可视化页面中, 提交pull request



#### 2. git 切换分支

* git checkout <分支名>



#### 3. 切换到一个新建的分支时出现错误

**若错误为：error: pathspec 'XXX' did not match any file known to git.**

* 执行 git fetch        //取回所有分支的更新
* git branch -a        //可以看到自己新建的分支名
* git checkout <分支名>     //再次切换分支就会成功了