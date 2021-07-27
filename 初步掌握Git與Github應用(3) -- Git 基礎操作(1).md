# 初步掌握Git與Github應用(3) -- Git 基礎操作(1)

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: Git 版本控制流程
![](https://i.imgur.com/2QbFuQJ.png)

:point_up_2: **Git 的大致流程圖**

---

## :wrench: 安裝數據庫

* 使用 `git init` 安裝本地數據庫，紀錄版本變更。

![](https://i.imgur.com/EaeNlFg.png)

:point_up_2: 可以觀察到路徑後方多出 **(master)**，代表有使用 **Git** 進行版本控制。

* 版本記錄被放在 **.git** 資料夾內(預設隱藏)

![](https://i.imgur.com/zx23dcz.png)

![](https://i.imgur.com/oqLc8Mn.png)

![](https://i.imgur.com/nbeMKpZ.png)

![](https://i.imgur.com/KEJyvao.png)

> 請勿隨意更動 **.git** 資料夾內的內容!

---
## :pencil2: 提交版本 (**commit**)

在新增完本地數據庫之後，接下來我們要將工作目錄加到(**add**)索引，然後放到(**commit**)本地數據庫。

首先，讓我們到 **[Github](https://github.com/QI-XIANG/JQuery_Book_2021)**  上進行觀察，進一步了解 **commit**。

:point_down: **11 commits** 可以說是進行11次的版本更新

![](https://i.imgur.com/OHMXWHI.png)

:point_down: 觀察版本註解、更新時間、作者

![](https://i.imgur.com/qeeEWNi.png)

:point_down: 觀察版本更新內容(新增或刪除)、檔案更新數量

![](https://i.imgur.com/HjOpzSy.png)

> 下一篇，將介紹細部的 git 操作，例如: 將檔案加入索引、檢查狀態、提交更新等...。
---

[ToC]

###### Last updated 2021/07/13 by Qi Xiang
