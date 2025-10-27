Git is a version control system.
Git is free software.
Using git to add files needs two steps:git add & git commit.
git add can just add one file once a time.but git commit can add many files a time.
Using git status can check out the content in the file if the content is change or not.
Using git diff to figure out what changes hanpend.
Using git log to show each change and the change message in each time.
Git has a mutable index called stage,which is the git add submmit place.
Using "git reset -- [options] numbers" to reset the present library version.The [options] can be "hard","soft","mixed".
Numbers is the only ID for the version you want to reset.
Using "git checkout -- "filename"" can reset the content that you add but doesn't commit or the content that you doesn't add.
Using "git reset HEAD "filename""  can cancel the contetnt to the work place that you add to the stage but doesn't commit.AKA unstage.
使用“rm”和“git rm”可以删除文件，区别在于"git rm"是rm+git add命令，即提交了删除文件的状态到暂存区，这样一来就无法通过git checkout来恢复了，
只能通过git reset HEAD来恢复到版本库的最新状态。而rm则可以通过git checkout来恢复。
使用"git checkout -b branchname"可以创建并切换分支,相当于git brach branchname+git checkout branchname。
在git下创建分支是相当快捷的。
当某个分支出现bug时,我们可以从这个分支创建出一个分支来进行修复工作，完成之后再merge回去。如果这时候我们正在工作的分支还未完成并且我们此时分支的工作
只做了一半还无法提交，那么我们可以用"git stash"来把当前的工作现场“储存”起来。此时该工作分支会回到版本库中的最新状态，类似于"git reset -- [options] numbers",等其他工作完成之后再恢复当前的工作现场。
在完成其他工作后，我们可以用"stash list"来查看当前保存的所有工作现场，再用"git stash pop"或者"git stash apply"来恢复，区别在于"git stash pop"会在还原
工作现场之后将其从stash内容删除，下一次再有这种情况是需要再次使用“git stash”，而“git stash apply”并不会删除。
在修复完bug并合并之后，如果我们想在当前工作分支修改同样的Bug,我们无需再操作一遍，只需要使用"git cherry-pick ID"，ID是修复bug那次操作的commit ID。
使用"git rebase"完成变基操作。

