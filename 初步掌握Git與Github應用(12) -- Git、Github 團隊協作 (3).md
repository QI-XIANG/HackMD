# 初步掌握Git與Github應用(12) -- Git、Github 團隊協作 (3)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

## :memo: 實際模擬小型團隊協作

團隊開發，通常會先做整個環境的 commit 紀錄 (ex. master 分支)，之後會陸續建立出各個分支，建立完分支後，接著就會去討論如何在各分支上進行分工(誰負責版面設計、誰負責實作功能等...)，最後再進行分支合併。

### :mag_right: 架構圖

![](https://i.imgur.com/bDzC8zj.png)

### :triangular_flag_on_post: 實際操作

* 建立資料夾、移動路徑、安裝本地數據庫
![](https://i.imgur.com/RqNrn5h.png)

* 新增檔案 (**index.html**)
![](https://i.imgur.com/L3qTUOK.png)

* 編輯檔案 (**index.html**)
![](https://i.imgur.com/WqhcFjj.png)

* 加入索引、提交紀錄，建立 **master** 分支 (預設)
![](https://i.imgur.com/zQhwul5.png)

* 目前結構如下: 
![](https://i.imgur.com/5NxCqWc.png)

* 建立 **develop** 分支、查詢分支、切換到 **develop** 分支
![](https://i.imgur.com/SkYw68M.png)

* 目前結構如下:
![](https://i.imgur.com/VidvMQE.png)

* 在 **develop** 分支上建立 **feature/view** 分支、切換到 **feature/view** 分支、新增檔案 (**all.css**)、加入索引、提交紀錄
![](https://i.imgur.com/CMHiSXu.png)

* 目前結構如下:
![](https://i.imgur.com/mFPdNiP.png)

* 切換回 **develop** 分支、合併 **feature/view** 分支到 **develop** 分支
![](https://i.imgur.com/GTxpU4E.png)

* 目前結構如下:
![](https://i.imgur.com/8IrjpHl.png)

* 在 **develop** 分支上建立 **feature/JS** 分支、切換到 **feature/JS** 分支、新增檔案 (**all.js**)、加入索引、提交紀錄
![](https://i.imgur.com/L0kD7TA.png)

* 目前結構如下:
![](https://i.imgur.com/iSCuMl7.png)

* 切換回 **develop** 分支、合併 **feature/JS** 分支到 **develop** 分支
![](https://i.imgur.com/QUd4RW1.png)

* 目前結構如下:
![](https://i.imgur.com/W4vGewI.png)

* 切換回 **master** 分支、合併 **develop** 分支到 **master** 分支
![](https://i.imgur.com/ezeDLB7.png)

* 最終結構如下:
![](https://i.imgur.com/bDzC8zj.png)

> 上方模擬的就是小型團隊協作時，該如何使用分支去完成專案開發。:notes:

---

[ToC]

###### Last updated 2021/07/26 by Qi Xiang

