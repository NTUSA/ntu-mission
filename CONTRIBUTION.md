# 版本控制模式說明

以 `master` 分支為主要版本，反映伺服器上的狀態。

## 如何提交修改

### 事前準備

每次要修改的時候，先從既有的版本建立新的 branch（例如 `patch-2nd-wave`）：

    # 建立分支
    git checkout -b patch-2nd-wave

一個分支上可以有多個 commit —— 就像備份一樣，你可以在改到一個段落時先做 commit。

    # 做些修改並 commit
    echo "你真的很棒！" > test.txt
    git commit -m "增加一些正向力語錄"

當你改到滿意之後，就可以把這個分支推送到 GitHub 上了：

    # 推送版本到伺服器上
    git push origin patch-2nd-wave


### 提交 PR

通知網管小組更新網站的方式，是以 GitHub **pull request (PR)** 提交修改的分支。

當網管小組收到 PR 通知時，會將 `patch-` 分支合併回 `master`，並把伺服器上的網頁更新到 `master` 分支上的版本。這樣就能確保各方的修改都不致於互相覆蓋，也讓網管小組知道什麼時候有新的內容而不必手動上傳。


### 繼續作業

別忘記在本地端回到 `master` 分支上：

```
# 切換工作分支為 master
git checkout master

# 從遠端取得 master 的更新至本地
git pull --rebase
```

## 貢獻者

* Ang Fu (作者)
* Poren Chiang (網管小組)
