# git-demo
demo for the usage of  github
這是我的git練習本

git remote add origin git@github.com:kaochenlong/practice-git.git

origin 是一個「代名詞」，指的是後面那串 GitHub 伺服器的位置。

git push -u origin master

在前面進行 Push 的時候，有加入了一個 -u 參數，表示要設定 upstream 的意思。嗯…問題是，什麼是「upstream」？

upstream，中文翻譯成「上游」。不要被名詞嚇到了，這 upstream 的概念其實就只是另一個分支的名字而已。在 Git 裡，每個分支可以設定一個「上游」（但每個分支最多只能設定一個 upstream），它會指向並追蹤（track）某個分支。通常 upstream 會是遠端 Server 上的某個分支，但其實要設定在本地端的其它分支也可以。

就會把 origin/master 設定為本地 master 分支的 upstream，當下回執行 git push 指令而不加任何參數的時候，它就會猜你是要推往 origin 這個遠端節點，並且把 master 這個分支推上去。

反之，沒設定 upstream 的話，就必須在每次 Push 的時候都跟 Git 講清楚、說明白


git pull = git fetch + git merge
