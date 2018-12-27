# git-demo
demo for the usage of  github
這是我的git練習本

第一次使用git設定:
$ git config --global user.name " "

$ git config --global user.email " "

-----------------------------------
$ git log --oneline --graph
$ git branch dev    # 建立 dev 分支
$ git branch        # 查看當前分支
$ git checkout dev  # 切换去 dev 分支

$ git checkout -b  dev # 使用 checkout -b + 分支名, 就能直接創建和切換到新建的分支:

$ git commit -am "放入想要的commit"  # -am": add 所有改變 並直接 commit

------------------------------------

$ git init

$ git add README.md

$ git commit -m "first commit"

$ git remote add origin git@github.com:kaochenlong/practice-git.git

origin 是一個「代名詞」，指的是後面那串 GitHub 伺服器的位置。

$ git push -u origin master

在前面進行 Push 的時候，有加入了一個 -u 參數，表示要設定 upstream 的意思。嗯…問題是，什麼是「upstream」？

upstream，中文翻譯成「上游」。不要被名詞嚇到了，這 upstream 的概念其實就只是另一個分支的名字而已。在 Git 裡，每個分支可以設定一個「上游」（但每個分支最多只能設定一個 upstream），它會指向並追蹤（track）某個分支。通常 upstream 會是遠端 Server 上的某個分支，但其實要設定在本地端的其它分支也可以。

就會把 origin/master 設定為本地 master 分支的 upstream，當下回執行 git push 指令而不加任何參數的時候，它就會猜你是要推往 origin 這個遠端節點，並且把 master 這個分支推上去。

反之，沒設定 upstream 的話，就必須在每次 Push 的時候都跟 Git 講清楚、說明白


$ git pull = git fetch + git merge

要使用 Clone 指令就可以把整個專案複製一份回來了。在 GitHub 專案的頁面有一個「Clone or download」的按鈕：
同樣可以選擇 HTTPS 或是 SSH，這裡我選擇 SSH。複製連結之後，接著便可使用 Clone 指令把它複製下來：

$ git clone https://github.com/e04ji3w94gj94/git-demo.git

這個指令會把整個專案複製一份下來並存在同名的目錄裡。如果想要 Clone 下來之後存成不同的目錄名稱的話，只要在後面加上目錄的名字即可：
$ git clone https://github.com/e04ji3w94gj94/git-demo.git testclone
