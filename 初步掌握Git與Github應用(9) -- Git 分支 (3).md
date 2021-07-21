# 初步掌握Git與Github應用(9) -- Git 分支 (3)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

## :memo: Git Tag 標籤

實際在專案開發上，都會有上線的第一版(v1)之後的第二版(v2)等等的分類。Git 標籤也有類似的用意，提交紀錄 (commit) 時，會產生很多的 commit 紀錄，需要確認這些 commit 紀錄中到底哪一個是上線的版本或回顧重要的版本時，Git 標籤就是一個很好用的工具。

### :notebook: 使用的指令

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git tag`       | 查詢標籤 |
| `git checkout 標籤名稱`       | 切換到標籤的 commit |
| `git tag -n`       | 查詢詳細標籤 |
| `git tag -d 標籤名稱`       | 刪除標籤 |
| `git tag 標籤名稱`       | 新增輕量標籤 |
| `git tag -am "備註內容" 標籤名稱`       | 新增標示標籤 |

* 開新資料夾、切換路徑、安裝本地數據庫
![](https://i.imgur.com/jrJFTti.png)

* 新增檔案 (**index.html**)
![](https://i.imgur.com/xhXCJId.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/gpTaPvF.png)

* 加入索引、提交紀錄、查詢 **commit** 紀錄
![](https://i.imgur.com/2Z77E6l.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/UkdLpc2.png)

* 加入索引、提交紀錄
![](https://i.imgur.com/J3ofKdB.png)

* 查詢標籤、新增輕量標籤 (**v1**)、查詢標籤
![](https://i.imgur.com/3E1PB2v.png)

:::info
:bulb: **Hint:** 由於一開始沒有新增過標籤，故使用 `git tag` 查詢標籤沒有顯示任何東西。
:::

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/Q72uFDa.png)

* 加入索引、提交紀錄、查詢 **commit** 紀錄
![](https://i.imgur.com/FY0jale.png)

* 查詢標籤、切換到有 **v1** 標籤的 **commit** 紀錄
![](https://i.imgur.com/hH5buSD.png)

* 切換過去後的檔案內容 (**index.html**)
![](https://i.imgur.com/tFSRnBE.png)

* 回到 **master** 分支上最近一次的 **commit** 紀錄
![](https://i.imgur.com/7xxLWPl.png)

* 切換過去後的檔案內容 (**index.html**)
![](https://i.imgur.com/AfE7u1D.png)

* 新增檔案 (**index2.html**)、加入索引、提交紀錄
![](https://i.imgur.com/LFczX81.png)

* 新增標示標籤 (**v2**)、查詢標籤
![](https://i.imgur.com/QR03m0R.png)

:::info
:bulb: **Hint:** 無法為已新增的"輕量標籤"加上備註內容，需要刪除該輕量標籤，再以"標示標籤"的方式新增標籤。
:::

* 查詢詳細標籤資訊 (備註內容)
![](https://i.imgur.com/XpyNN94.png)

:::info
:bulb: **Hint:** 新增的"輕量標籤"的備註內容是 commit 的註解。
:::

> 透過 **tag** ，可以更加快速的分類出各種不同的版本，而 **tag** 的備註內容則提供細部版本資訊作為參照。在切換版本時，使用 **tag** 也較為方便快速。

---
## :memo: Git Stash 暫存檔案

平常寫程式或網頁到一半，有機會在途中有更重要的事要做，這時又剛好寫到一半無法做 **commit**。透過暫存 (**stash**) 的方式，可以保留現在的工作進度，等到手上的事情告一段落，再將暫存還原回去。

### :notebook: 使用的指令

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git stash`       | 暫時儲存當前目錄 |
| `git satsh list` | 瀏覽 git stash 列表 |
| `git stash pop`       | 還原暫存 |
| `git stash drop`       | 清除最新暫存 |
| `git stash clear`       | 清除全部暫存 |

* 開新資料夾、切換路徑、安裝本地數據庫
![](https://i.imgur.com/OBj4Zto.png)

* 新增檔案 (**index.html**)
![](https://i.imgur.com/5XmR1BM.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/O0HPRvy.png)

* 加入索引、提交紀錄
![](https://i.imgur.com/YziqUDR.png)

* 建立分支 (**issue**)，但暫時不切換過去
![](https://i.imgur.com/9971fHS.png)

* 繼續編輯檔案 (**index.html**)
![](https://i.imgur.com/5yVa7PZ.png)

* 查詢狀態、將目前工作進度加入暫存 (假設有 **bug** 要修而必須停下目前工作，故先不做 **commit**)、再次查詢狀態 (由於已將編輯內容放入暫存所以是空的)
![](https://i.imgur.com/MhRAR86.png)

* 將目前工作進度加入暫存後，檔案會回到最近一次 **commit** 的狀態
![](https://i.imgur.com/O0HPRvy.png)

* 瀏覽 git stash 列表，目前有一筆暫存紀錄
![](https://i.imgur.com/WgcPCKA.png)

* 切換 **issue** 分支(假設在這個分支修 **bug**)、還原暫存到 **issue** 分支
![](https://i.imgur.com/0YrAZPn.png)

* 檔案被還原到上次的工作進度
![](https://i.imgur.com/5yVa7PZ.png)

* 瀏覽 git stash 列表是空的，因為已將暫存還原、將 **issue** 的工作進度放入暫存
![](https://i.imgur.com/leSuIXY.png)

* 切換回 **master** 分支、還原暫存到 master 分支
![](https://i.imgur.com/GjGTB1M.png)

* 檔案被還原到上次的工作進度 (**issue** 分支上的進度)
![](https://i.imgur.com/5yVa7PZ.png)

:::info
:bulb: **Hint:** 透過 **Git Stash** 的暫存效果，可以快速進行不同分支的版本過渡(同步內容)，一定程度上也可以減少日後在合併分支(**branch merge**)上衝突發生的可能性。
:::

---


[ToC]

### Recently modified: 2021/07/21 by Qi Xiang
