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
Using "git reset HEAD "filename""  can cancel the contetnt to the work place that you add to the stage but doesn't commit.
AKA unstage.
使用“rm”和“git rm”可以删除文件，区别在于"git rm"是rm+git add命令，即提交了删除文件的状态到暂存区，这样一来就无法通过git checkout来恢复了，
只能通过git reset HEAD来恢复到版本库的最新状态。而rm则可以通过git checkout来恢复。
使用"git checkout -b branchname"可以创建并切换分支,相当于git brach branchname+git checkout branchname。