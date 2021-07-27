# 初步掌握Git與Github應用(10) -- Git、Github 團隊協作 (1)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"
::: 

## :memo: 推送分支到遠端數據庫 (Github)

### :notebook: 使用的指令

| 指令         | 功能說明               |
| ----------------- |:----------------------- |
| `git remote`       | 查詢遠端數據庫 |
| `git remote rename 原名稱 修改名稱`       | 修改遠端數據庫名稱 |
| `git push origin master`       | 推送 master 分支到 origin (預設的遠端數據庫名稱) |

### :triangular_flag_on_post: 實際操作

* 到 **Github** 上建立新的 **repository**
![](https://i.imgur.com/Vv9aSaM.png)
![](https://i.imgur.com/gL7AElV.png)
![](https://i.imgur.com/jqWZqUM.png)

* 建立資料夾、切換路徑
![](https://i.imgur.com/2TCGdHS.png)

* 將遠端數據庫 **clone** 到當前路徑
![](https://i.imgur.com/TIzkmlN.png)

* 資料夾內容
![](https://i.imgur.com/cEMgLor.png)

* 切換路徑到 **clone** 下來的資料夾內、新增檔案 (**index.html**)、加入索引、提交紀錄
![](https://i.imgur.com/Nh0RyAC.png)

* 推送 **master** 分支到遠端數據庫
![](https://i.imgur.com/nFnlMJT.png)

* 重新整理後 **Github** 上的 **repository** 如下
![](https://i.imgur.com/UrLhkQq.png)

* 建立新分支 (**issue**)、切換分支
![](https://i.imgur.com/ZkNenSH.png)

* 新增檔案 (**issue.html**)、加入索引、提交紀錄
![](https://i.imgur.com/EC8EsFc.png)

* 推送到遠端數據庫，但出現錯誤
![](https://i.imgur.com/HZpPdCp.png)

:::info
:bulb: **Hint:** 對於新建立的分支而言，因為沒有指定要推送到的遠端數據庫，所以無法單用 `git push` 就推送成功。
:::

* 查詢遠端數據庫
![](https://i.imgur.com/rnWaQjo.png)

* 指定將 **issue** 分支推送到 **origin** 遠端數據庫
![](https://i.imgur.com/WMYrz0O.png)

* 重新整理後，**branch** 數量更新為2
![](https://i.imgur.com/iCqwQXG.png)

* 推送分支後，**issue** 分支上的檔案內容
![](https://i.imgur.com/y0Z0ffm.png)

* 更改遠端數據庫的名稱(非 **github** 上的名稱)、查詢遠端數據庫
![](https://i.imgur.com/tMrcgWX.png)

* 新增檔案 (**issue2.html**)、加入索引、提交紀錄
![](https://i.imgur.com/wmrHuFT.png)

* 將 **issue** 分支推送到 **origin** 遠端數據庫，由於已經變更遠端數據庫名稱，故推送失敗、使用新遠端數據庫名稱進行推送
![](https://i.imgur.com/WQCSdKL.png)

* 推送分支後，**issue** 分支上的檔案內容
![](https://i.imgur.com/dFGoO9p.png)


---

## :rocket: BONUS: 在 Github 上放置靜態網頁

### :triangular_flag_on_post: 實際操作

* 到 **Github** 上建立新的 **repository**
![](https://i.imgur.com/C8uaoir.png)
![](https://i.imgur.com/inRUFoD.png)
![](https://i.imgur.com/9mv3Pj4.png)

* 切換路徑到"桌面"、新增資料夾、移動路徑到新增的資料夾
![](https://i.imgur.com/GwORYfU.png)

* 將遠端數據庫 **clone** 到當前路徑、切換路徑到 **clone** 下來的資料夾內、新增檔案 (**index.html**)
![](https://i.imgur.com/Je3Qjo0.png)

*  編輯檔案 (**index.html**)
![](https://i.imgur.com/f9NK8ll.png)

* 加入索引、提交紀錄、推送 **master** 分支到 **origin** 遠端數據庫
![](https://i.imgur.com/FRCnQ9G.png)

* 重新整理頁面後，點擊 **Settings**
![](https://i.imgur.com/gNtqqQV.png)

* 點擊 **Settings**
![](https://i.imgur.com/iFO78iq.png)

* 點擊"**紅框**"
![](https://i.imgur.com/dqhOg8r.png)

* 選擇剛剛推送的 **master** 分支並按下 **Save** 
![](https://i.imgur.com/PAW8GDq.png)

* 上方會出現網址
![](https://i.imgur.com/K9dKKjE.png)

* 點擊網址即可看到剛剛推送上去的 **"靜態網頁"**
![](https://i.imgur.com/lkb8icN.png)


---

[ToC]


###### Last updated 2021/07/24 by Qi Xiang


