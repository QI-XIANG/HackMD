# 初步掌握Git與Github應用(7) -- Git 分支 (1)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

## :memo: 簡單介紹分支 (branch)

![](https://nvie.com/img/git-model@2x.png)

:point_up:如果要進行團隊開發，**分支(branch)** 會是一個必須要了解的觀念。

* 在 **Git Bash** 操作 **Git** 的話，相信一定對路徑後方的 **master** 不陌生吧? 這個 **master** 代表的就是目前所在的分支，也可以說是現行的版本。有時為了修復 bug，會不小心搞壞現行版本，這時就可以透過建立新的 **分支(branch)**，在新的分支上進行修復工作及 **commit**，確認修正無誤後，再**合併(merge)** 回 **master** 就好。 
![](https://i.imgur.com/mIpPWuM.png)



:::info
:bulb: **Hint:** [圖片連結](https://nvie.com/posts/a-successful-git-branching-model/)
:::

---

## :memo: 瞭解目前所在分支(branch) - HEAD

> HEAD 代表目前所在位置(分支)的指標，也可以說是目前所在的 **commit** 紀錄。

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git branch`       | 確認目前所在分支|
| `git checkout commit 前四碼` |  移動 **HEAD** 查看特定的 **commit** 紀錄    |
| `git checkout master` |  回到 master 分支 上最近一次的 commit 紀錄    |

* 開新資料夾、移動路徑、安裝本地數據庫、新增檔案、加入索引、提交版本紀錄
![](https://i.imgur.com/8WwjWPp.png)

* 透過 **git branch**，看到目前星號(*)停在 **master**，**master** 就是目前所在分支
![](https://i.imgur.com/adAypME.png)

:::info
:bulb: **Hint:** 至少要有1次 commit 紀錄，才能透過 `git branch` 查詢到分支。
:::

* 修改檔案
![](https://i.imgur.com/LThJDLY.png)

* 查看狀態、加入索引、提交紀錄
![](https://i.imgur.com/IVu7Cy1.png)

* 查詢 commit 紀錄，目前有兩次紀錄
![](https://i.imgur.com/ioynD6P.png)

* 透過剛剛查詢紀錄，使用 `git checkout 版本紀錄至少前四碼`，回到之前的 **commit** 紀錄上
![](https://i.imgur.com/jd5GvkM.png)

* 檔案恢復到未編輯前
![](https://i.imgur.com/fu4ZXXQ.png)

* 回到 **master** 分支上最近一次的 **commit** 紀錄
![](https://i.imgur.com/npHC2mZ.png)

---

## :memo: 建立分支(branch)

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git branch 分支名稱`       | 新增分支|
| `git checkout 分支名稱`       | 移動分支|

* 新增分支(**feature1**)、查詢得知目前共有2分支
![](https://i.imgur.com/mS2x7fL.png)

* 移動到 **feature1** 分支上
![](https://i.imgur.com/gZzYhdO.png)

* 修改檔案
![](https://i.imgur.com/WUsSlgc.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/uxtuStz.png)

* 回到 **master** 分支上最近一次的 **commit** 紀錄
![](https://i.imgur.com/O0aBXrW.png)

* 檔案被還原
![](https://i.imgur.com/LThJDLY.png)

---

[ToC]

###### Last updated 2021/07/19 by Qi Xiang
