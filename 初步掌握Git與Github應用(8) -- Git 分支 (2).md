# 初步掌握Git與Github應用(5) -- Git 分支 (2)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

接續前面的內容，接下來將說明如何進行分支(**branch**)的合併(**merge**)。:blush:

## :memo: 分支合併(merge) -- Fast Forward

### :question: 什麼是 Fast Forward ?

> Git 的合併(merge) 原則上預設是 Fast Forward。

如下圖 **bugfix** 分支是在 **master** 分支上新建的分支。
![](https://backlog.com/git-tutorial/tw/img/post/stepup/capture_stepup1_4_1.png)

合併 **bugfix** 分支到 **master** 分支時， 如果**master** 分支的狀態是沒有更改過的話(開新分支後，沒有在 **master** 分支額外提交紀錄 -- **commit**)，那麼這個合併是非常簡單的。 **bugfix** 分支的歷史記錄包含了 **master** 分支的歷史記錄，所以只要把 **bugfix** 移動到 **master** 分支就可以導入 **bugfix** 分支的內容(簡單來說，就是將 **master** 當作標籤撕下來貼到 **bugfix** 目前所在之處)。這樣的合併被稱為 **Fast-Forward (快轉合併)**。
![](https://backlog.com/git-tutorial/tw/img/post/stepup/capture_stepup1_4_2.png)

### :dart: 情境說明

新分支: **feature/add-page**

1. 使用預設的 **merge** 採用 **fast-forward** 進行:<br>
會將 branch 的 commit 紀錄合併到 master 上<br>
指令：`git merge 分支名稱`

![](https://i.imgur.com/oPLxsue.png)

2. 不使用 **fast-forward** ，以 **no fast-forward** 進行：<br>
會保留原始 **branch** 上的 **commit** 紀錄，並在 **master** 上增加一個 **merge branch '分支名稱' into master**<br>
指令：`git merge 分支名稱 --no-ff`
**–no-ff** 不要快速合併

![](https://i.imgur.com/jtXK79v.png)


**no fast-forward** 的好處:
可以完整保留每一個分支的 **commit** 紀錄

**no fast-forward** 的壞處:
若是 **commit** 紀錄只有一個，合併多次就會出現很多小叉路

-- 資料來源: [連猴子都能懂的Git入門指南](https://backlog.com/git-tutorial/tw/stepup/stepup1_4.html)、[連葉子都秒懂的 Fast Forward](https://tzuhui.github.io/2019/06/20/Git/fast-forward/)


---
## :triangular_flag_on_post: 實作 Git Merge -- Fast Forward

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git merge 分支名稱`       | 將目前所在分支和特定分支合併|

* 開新資料夾、切換路徑、安裝本地數據庫、新增檔案
![](https://i.imgur.com/8Fraa2a.png)

* 加入索引、提交紀錄
![](https://i.imgur.com/M9lsnJS.png)

* 修改檔案 (**index.html**)
![](https://i.imgur.com/in1aF1J.png)

* 查詢狀態 (**modified**)、加入索引、提交紀錄
![](https://i.imgur.com/6Ae14Yr.png)

* 新增分支 (**feature1**)、查詢分支
![](https://i.imgur.com/uzOAaE1.png)

* 切換到分支 feature1 
![](https://i.imgur.com/so85tgU.png)

* 開新資料夾 (**css**)、切換路徑、新增檔案 (**all.css**)、返回上一層
![](https://i.imgur.com/giU3aRg.png)

* 目前資料夾內情況
![](https://i.imgur.com/s3nNDfI.png)

* 修改檔案 (**index.html**)
![](https://i.imgur.com/HcGw8tb.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/ruCdKb6.png)

* 回到 **master** 分支的最新紀錄
![](https://i.imgur.com/SXMYWfs.png)

* 目前資料夾內情況 (css資料夾不見了)
![](https://i.imgur.com/chQCsif.png)

* 將 **feature1** 和 **master** 進行分支合併
![](https://i.imgur.com/BHWw2dI.png)

* 目前資料夾內情況 (css資料夾回來了)
![](https://i.imgur.com/esr5ZNH.png)

:::info
:bulb: **Hint:** 建立新分支後，若回到 master 額外提交紀錄 (**commit**)，合併分支時有可能會出現**版本衝突**的提示訊息。
::: 

---

## :flags: 實作 Git Merge -- 自動合併

以下說明當 **master** 更新的版本超過新建立的分支時(建立分支後，又回頭去更新 **master** 分支)，如何進行同時更新。(**情境: 無衝突版本**)

![](https://backlog.com/git-tutorial/tw/img/post/stepup/capture_stepup2_7_2.png)

-- 圖片來源: [連猴子都能懂的Git入門指南](https://backlog.com/git-tutorial/tw/stepup/stepup2_7.html)

* 建立資料夾、移動路徑、安裝本地數據庫
![](https://i.imgur.com/eVPfGFn.png)

* 新增檔案 (**index.html**)
![](https://i.imgur.com/xgwwZB7.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/9rnDV5l.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/dZkjKQQ.png)

* 建立分支 (**feature1**)、切換分支
![](https://i.imgur.com/SkcRs26.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/o9wlssf.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/k4GJHrE.png)

* 切換分支，回到 **master** 分支
![](https://i.imgur.com/NZdvo3n.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/ZmQ9HRh.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/MGYF1US.png)

* 將 **feature1** 和 **master** 進行分支合併
![](https://i.imgur.com/MsTXNS7.png)

* 出現提示訊息，因為建立分支(**feature1**)後，又去 **master** 分支上提交新版本紀錄 (**commit**)，進入 **vim** 編輯器，輸入 `:q`退出。
![](https://i.imgur.com/oymx2qS.png)

* 合併分支後，兩版本進行整合 (無衝突出現)。
![](https://i.imgur.com/MjHxZZE.png)

---
## :golf: 實作 Git Merge -- 解決衝突

假設團隊其中一部分在新分支上作更新，另一部分則繼續在 **master** 分支上作更新，這樣就很有可能會發生程式碼剛好寫在同一支檔案的某一行，在合併 **(merge)** 時就會發生衝突。

![](https://backlog.com/git-tutorial/tw/img/post/stepup/capture_stepup2_7_2.png)

-- 圖片來源: [連猴子都能懂的Git入門指南](https://backlog.com/git-tutorial/tw/stepup/stepup2_7.html)

以下說明如何解決衝突:

* 新增資料夾、切換路徑、安裝本地數據庫
![](https://i.imgur.com/chNCqPP.png)

* 新增檔案 (**index.html**)
![](https://i.imgur.com/RNWhfmI.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/yS5A4hl.png)

* 加入索引、提交紀錄
![](https://i.imgur.com/XjB6qs4.png)

* 建立分支 (**feature1**)、查詢分支、移動分支
![](https://i.imgur.com/dkOc37t.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/EMWRcd2.png)

* 查詢狀態、加入索引、提交紀錄
![](https://i.imgur.com/MswoDPT.png)

* 切換分支，回到 **master** 分支
![](https://i.imgur.com/Gum6cIu.png)

* 編輯檔案 (**index.html**)，修改與 **feature1** 分支同一行的程式碼，刻意製造衝突。
![](https://i.imgur.com/ddTIZzS.png)

* 加入索引、提交紀錄
![](https://i.imgur.com/gtoacyi.png)

* 將 **feature1** 和 **master** 進行分支合併，提示出現衝突(**CONFLICT**)，無法正常合併分支。
![](https://i.imgur.com/jJIquSF.png)

* 進入檔案 (**index.html**) 查看
![](https://i.imgur.com/aq1Gy84.png)

* 手動解決衝突，保留2個 **h1** 標籤內容
![](https://i.imgur.com/F9Vu8qQ.png)

* 因為有衝突無法進行自動合併，手動加入索引、提交紀錄，成功合併2分支
![](https://i.imgur.com/wfo3lhS.png)

---

[ToC]

### Recently modified: 2021/07/20 by Qi Xiang
