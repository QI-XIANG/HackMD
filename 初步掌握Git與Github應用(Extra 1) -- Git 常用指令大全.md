# 初步掌握Git與Github應用(Extra 1) -- Git 常用指令大全

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: 實務上常用的 **git** 指令

### :sparkles: 基礎設定

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git --version`  |   查詢使用的 **git** 版本|
|    `git config --list`  |   查詢設定列表​(參數設定值)|
|    `git config --global user.name "你的名字"`  |   設定作者姓名|
|    `git config --global user.email "你的email"`  |   設定作者 email|


### :sparkles: 新增本地/遠端數據庫

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git init`  |   在本地資料夾新增數據庫|
|    `git clone 遠端數據庫網址`  |   複製遠端數據庫|

### :sparkles: 增加/刪除檔案

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git add 檔案名稱`  |   增加檔案進入索引|
|    `git add .`  |   增加全部檔案進入索引|
|    `git status`  |   查詢狀態|
|    `git log`  |   顯示 **commit** 歷史紀錄|
|    `git commit -m '更新訊息'`  |   將索引提交到本地數據庫|

### :sparkles: 還原指令

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git reset --hard `  |   還原工作目錄與索引，會跟最後一次 commit 保持一樣|
|    `git reset HEAD`  |   全部檔案取消索引|
|    `git reset HEAD 檔案名稱`  |   單一檔案取消索引|
|    `git checkout 檔案名稱 `  |   恢復單一檔案到最新 commit 狀態|
|    `git reset --hard HEAD^`  |   刪除最近一次 commit |
|    `git reset --hard ORIG_HEAD`  |   上面語法如果刪除錯了可以再用此語法還原|
|    `git reset --soft HEAD^`  |   刪除最近一次 commit，但保留異動內容|
|    `git commit --amend`  |   commit 後發現有幾個檔案忘了加入進去，想要補內容進去時|

### :sparkles: 分支

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git branch`  |   顯示所有本地分支|
|    `git branch 分支名稱`  |   新增分支|
|    `git checkout 分支名稱`  |   切換分支|
|    `git merge 分支名稱`  |   合併指定分支到目前的分支|
|    `git branch -d 分支名稱`  |   刪除分支|

### :sparkles: 遠端數據庫操作

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git clone 遠端數據庫網址`  |   複製遠端數據庫|
|    `git remote`  |   查詢遠端數據庫|
|    `git push 遠端數據庫名稱 遠端分支名稱`  |   將本地分支推送到遠端分支|
|    `git pull`  |   將遠端分支拉下來與本地分支進行合併|

### :sparkles: 標籤

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git tag`  |   查詢標籤|
|    `git tag -n`  |   查詢詳細標籤|
|    `git tag -d 標籤名稱`  |   刪除標籤|
|    `git tag 標籤名稱`  |   新增輕量標籤|
|    `git tag -am "備註內容" 標籤名稱`  |   新增標示標籤|

### :sparkles: 暫存

|     指令      |    功能說明            |
| ----------------- |:----------------------- |
|    `git stash`  |   暫時儲存當前目錄|
|    `git stash list`  |   瀏覽 stash 列表|
|    `git stash pop`  |   還原暫存|
|    `git stash drop`  |   清除最新暫存|
|    `git stash clear`  |   清除全部暫存|

:::info
:bulb: **Hint:** 學習更多的 git 指令 ➜ [連猴子都能懂的Git入門指南](https://backlog.com/git-tutorial/tw/reference/
)
:::

---
[ToC]

###### Last updated 2021/07/15 by Qi Xiang




