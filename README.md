# NTU Mission 臺大總動員

## 版本控制模式

以 `master` 分支為主要版本，反映伺服器上的狀態。

每次要修改的時候，先從既有的版本建立新的 branch（例如 `patch-2nd-wave`）：

```
# 建立分支
git checkout -b patch-2nd-wave

# 做些修改
...
git commit

# 推送版本到伺服器上
git push origin patch-2nd-wave
```

然後再以 **pull request** 的方式提交修改。當網管小組收到 PR 通知時，就會在 merge 之後、於伺服器端 `git pull` `master` 分支上的所有更新。

這時就可以回到 `master` 分支上了：

```
# 切換工作分支為 master
git checkout master

# 從遠端取得 master 的更新至本地
git pull --rebase
```


## 授權

Grayscale copyright 2013-2015 Iron Summit Media Strategies, LLC. Code released under the [Apache 2.0](https://github.com/IronSummitMedia/startbootstrap-grayscale/blob/gh-pages/LICENSE) license.
