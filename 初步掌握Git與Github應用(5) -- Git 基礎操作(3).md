# 初步掌握Git與Github應用(5) -- Git 基礎操作(3)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: 本篇將學到的指令

![](https://i.imgur.com/mKYcCHQ.png)

| 功能說明          | 指令               |
| ----------------- |:----------------------- |
|   將全部檔案取消索引   |  `git reset HEAD`   |
| 將單一檔案取消索引 |   `git reset HEAD 檔案名稱`   |
|    還原單一檔案   |  `git checkout 檔案名稱`   |
|     還原整個工作目錄與索引    |  `git reset --hard`  | 

1. `git reset HEAD`，將全部檔案取消索引，原本加入索引的檔案會被全部移出索引，用`git status`查看索引，會發現檔案變為 **untracked** 的狀態。

2. `git reset HEAD 檔案名稱`，僅將單一特定檔案取消索引，與上方指令功能基本相同。

3. `git checkout 檔案名稱`，恢復單一檔案到最新的 **commit** 狀態，讓檔案損毀時有救回來的可能。

4. `git reset -hard`，還原整個工作目錄與索引，與上方不同，不限於恢復單一檔案，版本會恢復到跟最新的(最後一次) **commit** 一樣。同時，它也會清空舊有索引包括編輯紀錄。

> **HEAD** 類似指標，它指向當前所在分支(**branch**)，後續會有詳細說明。

---

## :x: 取消索引

* 移動路徑到桌面 :point_right: 新增資料夾 :point_right: 移動到新資料夾下 :point_right: 安裝本地數據庫
![](https://i.imgur.com/dEXhozf.png)

* 新增檔案 :point_right: 將檔案加入索引 :point_right: commit 提交紀錄  :point_right: 查詢紀錄
![](https://i.imgur.com/XXC7SAz.png)

* 新增 **all.css、all.js** 兩個檔案，將其加入索引
![](https://i.imgur.com/SHjCRSM.png)

* 查詢目前索引狀態
![](https://i.imgur.com/A8Bk8Qk.png)

* 將全部檔案移出索引，然後查詢索引狀態，會發現 **all.css、all.js** 皆變為 **untracked**。
![](https://i.imgur.com/n7JsrJ3.png)

* 先將檔案加回索引，然後將 **all.css** 移出索引，此時查詢索引狀態會發現僅有 **all.css** 變為 **untracked**。
![](https://i.imgur.com/5v8xK88.png)

---

## :arrows_counterclockwise: 還原檔案

* 編輯 **index.html**
![](https://i.imgur.com/jqVBA5T.png)

* 用 **git status** 查詢狀態，發現 **index.html** 變為 **modified**。
![](https://i.imgur.com/ZewYkPC.png)

* 用 **git checkout index.html**，將 **index.html** 還原到最後一次 **commit** 時的狀態。
![](https://i.imgur.com/ppRqDOx.png)

* 最後一次 **commit** 時，**index.html** 為空檔案。
![](https://i.imgur.com/wW0worN.png)

* 將所有檔案加入索引  :point_right: 還原工作目錄與索引(跟最後一次 **commit** 狀態一樣)  :point_right: 查詢索引狀態為空。
![](https://i.imgur.com/YSouyll.png)

* 因為最後一次的 **commit** 沒有提交 **all.css、all.js**，故還原之後，工作目錄(**project**)內僅剩 **index.html**。
![](https://i.imgur.com/VL2xovz.png)

---

[ToC]

### Recently modified: 2021/07/14 by Qi Xiang

