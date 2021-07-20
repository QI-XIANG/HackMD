# 初步掌握Git與Github應用(4) -- Git 基礎操作(2)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: 本篇將學到的指令

![](https://i.imgur.com/mKYcCHQ.png)

| 功能說明          | 指令               |
| ----------------- |:----------------------- |
|   加入索引   |  `git add .`   |
| 檢查狀態 |   `git status`   |
|    提交更新    |  `git commit -m "修改紀錄"`   |
|     查詢紀錄    |  `git log`  | 

1. `git add .`，表示將所有檔案加入索引，也可使用`git add 檔案名稱` 將特定檔案放入索引。
![](https://i.imgur.com/WNZNhAr.png)

2. `git status`，檢視當前路徑下索引內檔案狀態，像是 **untracked** (未commit)、**tracked** (已commit)。變更檔案後，使用`git status`會自動偵測更動的(**modified**)檔案紀錄(**untracked files**)。
![](https://i.imgur.com/fy6BpbY.png)<br>
:point_down:**變更 index.html 內容**
![](https://i.imgur.com/m4GNF8T.png)<br>
:point_down:**偵測到 index.html 內容變更**
![](https://i.imgur.com/TZSB1uI.png)


3. `gti commit -m "修改紀錄(版本註解)"`，將索引做成紀錄，提交版本進入本地數據庫 (**.git**)，最後清空索引。善加利用版本註解，可以讓人更加清楚版本實際更新內容。**commit** 後再用`git status`會沒有東西，因為已提交索引(沒有要更新的資料)。
![](https://i.imgur.com/JUJSafM.png)

4. `git log`，查詢 **commit** 的歷史紀錄，包括作者、commit 時間，其中的亂碼代表版本紀錄。 
![](https://i.imgur.com/J0Jmg3s.png)

---

## :rocket: BONUS: .gitignore 忽略檔案

有時候，我們會不希望部分檔案(像是暫存檔、測試檔案)進入**版本控制**，這時就可以透過 **.gitignore** 來忽略特定檔案。

* 舉例
    * *.html : 忽略全部 html 檔案
    * forder/ : 忽略 folder 

* 新增 **index2.html、.gitignore**，使用`git status`查看狀態。
![](https://i.imgur.com/IWOMiX2.png)

* 修改 **.gitignore**，排除index2.html進入版本控制。
![](https://i.imgur.com/By4cL23.png)

* 成功排除 **index2.html** 進入版本控制。
![](https://i.imgur.com/9PnyHec.png)

:::info
:bulb: **Hint:** [.gitignore 忽略檔案大全](https://github.com/github/gitignore)
:::

> 忽略特定資料夾的方法與上面作法相同，故不再贅述。

---
[ToC]

### Recently modified: 2021/07/14 by Qi Xiang
