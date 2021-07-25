# 初步掌握Git與Github應用(11) -- Git、Github 團隊協作 (2)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

## :memo: 下載遠端數據庫

![](https://i.imgur.com/MAYUBfb.png)

### :notebook: 使用的指令

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git pull`       | 將遠端數據庫的檔案內容更新到本地工作目錄 |

### :question: 情境假設

假設現在有 "**A** (使用 a 資料夾作為工作目錄)"、"**B** (使用 b 資料夾作為工作目錄)" 兩個人在進行共同開發，而且沒有衝突發生。

#### :triangular_flag_on_post: 實際操作

* 先到 **Github** 上建立 **repository**
![](https://i.imgur.com/B8Zh9Wj.png)
![](https://i.imgur.com/wLPeWj4.png)
![](https://i.imgur.com/fb7oa67.png)

* A: 建立資料夾、移動路徑、**clone** 遠端數據庫到本地路徑下、移動路徑到遠端數據庫的資料夾下 (**gittest3**)
![](https://i.imgur.com/2HPq6Gc.png)

* B: 建立資料夾、移動路徑、**clone** 遠端數據庫到本地路徑下、移動路徑到遠端數據庫的資料夾下 (**gittest3**)
![](https://i.imgur.com/tL5wBxG.png)

* A: 新增檔案 (**index.html**)、加入索引、提交索引、推送 **master** 分支到 **origin** 遠端數據庫
![](https://i.imgur.com/6DMNMr0.png)

* B: 查詢 **commit** 紀錄(目前是空的)、將 **A** 剛剛更新到遠端數據庫的檔案內容拉到 **B** 的工作目錄、查詢 **commit** 紀錄(可以看到 **A** 的 **commit** 紀錄)
![](https://i.imgur.com/iOLe3vs.png)

* B: 新增檔案 (**b.html**)、加入索引、提交紀錄、推送 **master** 分支到 **origin** 遠端數據庫
![](https://i.imgur.com/CG7cea3.png)

* A: 將 **B** 剛剛更新到遠端數據庫的檔案內容拉到 **A** 的工作目錄、查詢 **commit** 紀錄(可以看到 **B** 的 **commit** 紀錄)
![](https://i.imgur.com/1XjkQxC.png)

:::info
:bulb: **Hint:** 
1. 使用`git pull`的時機: 要更新其他開發者的檔案內容到自己的工作目錄。 
2. 使用`git push`的時機: 要將檔案內容更新到遠端數據庫。
::: 

---

## :pushpin: 解決 git pull 帶來的衝突

有些情況下會無法進行 **push**，要先進行 **pull**。這種情況出現的主要原因是遠端數據庫的檔案內容與本地工作目錄的檔案內容有所不符 (有一方去更新遠端數據庫，但另一方並不知情就試圖進行 **push**)。

### :question: 情境假設

假設現在有 "**A** (使用 a 資料夾作為工作目錄)"、"**B** (使用 b 資料夾作為工作目錄)" 兩個人在進行共同開發，現在因為 **A** 在 **B** 不知情的情況下更新遠端數據庫，所以在 **B** 之後做 **push** 時有衝突發生。

### :triangular_flag_on_post: 實際操作

* 先到 **Github** 上建立 **repository**
![](https://i.imgur.com/V5nw8yU.png)
![](https://i.imgur.com/G4pK9xD.png)
![](https://i.imgur.com/NeuRGDw.png)

* A: 建立資料夾、移動路徑、**clone** 遠端數據庫到本地路徑下、移動路徑到遠端數據庫的資料夾下 (**gittest5**)
![](https://i.imgur.com/51qVX23.png)

* B: 建立資料夾、移動路徑、**clone** 遠端數據庫到本地路徑下、移動路徑到遠端數據庫的資料夾下 (**gittest5**)
![](https://i.imgur.com/K0ueWA4.png)

* A: 新增檔案 (**index.html**)、加入索引、提交索引、推送 **master** 分支到 **origin** 遠端數據庫
![](https://i.imgur.com/4mHDixM.png)

* B: 將 **A** 剛剛更新到遠端數據庫的檔案內容拉到 **B** 的工作目錄
![](https://i.imgur.com/B8E1ljN.png)

* A: 新增檔案 (**index2.html**)、加入索引、提交紀錄、推送 **master** 分支到 **origin** 遠端數據庫
![](https://i.imgur.com/TY1dQiL.png)

* B: 新增檔案 (**b.html**)、加入索引、提交紀錄
![](https://i.imgur.com/knrSpia.png)

* B: 推送 **master** 分支到 **origin** 遠端數據庫時，出現錯誤訊息，因為在 **B** 做 **push** 之前，**A** 已經先跑去更新遠端數據庫，造成 **B** 沒有 **A** 推送的 **commit** 紀錄，無法成功更新遠端數據庫
![](https://i.imgur.com/BvAehvM.png)

* B: 將 **A** 先前更新到遠端數據庫的檔案內容拉到 **B** 的工作目錄
![](https://i.imgur.com/4ont0ON.png)

* B: 出現合併分支的提示訊息，輸入`:q`後按 enter 關閉訊息
![](https://i.imgur.com/cB4Bdw5.png)

* B: 成功推送紀錄到遠端數據庫
![](https://i.imgur.com/LuwOhz5.png)

* A: 將 **B** 剛剛更新到遠端數據庫的檔案內容拉到 **A** 的工作目錄
![](https://i.imgur.com/kkrYDy4.png)

:::info
:bulb: **Hint:** 不用擔心 **push** 之後，覆蓋掉別人的檔案，因為一定要有先前別人的 **commit** 紀錄，才能進行 **push**。
::: 

---

## :rocket: BONUS: git pull 的實質意義

### :pencil2: git pull = git fetch + git merge

使用過`git pull`指令後，可以知道它就是將遠端分支拉下來和本地分支進行合併(**merge**)。

有時候因為不希望 `git pull` 下來的檔案內容造成本地數據庫太亂或有衝突，可以使用`git fetch origin(遠端數據庫名稱) branch(遠端分支名稱)`，此時本地工作目錄會多出一個 **FETCH_HEAD** 分支，這個分支上放的就是來自遠端數據庫的檔案內容。可以等到確認沒問題後，再合併 **FETCH_HEAD** 分支。

---

[ToC]

### Recently modified: 2021/07/25 by Qi Xiang
