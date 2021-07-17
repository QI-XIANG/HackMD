# 初步掌握Git與Github應用(4) -- Github 基礎應用

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

::: 

## :memo: 註冊 Github

[點擊前往 Github 註冊](https://github.com/)

### Step 1: 前往註冊 Github :rocket: 

![](https://i.imgur.com/LrzOrss.png)

### Step 2: 依序填入 email、password、username

![](https://i.imgur.com/v2gCd31.png)

> 另外，它會要求填入是否 (y/n) 願意用填入的 email 收到 github 的相關資訊。

### Step 3: 智力測驗 (我不是機器人驗證)

![](https://i.imgur.com/TXmZEC8.png)

### Step 4: 填入 email 信件中的驗證碼

![](https://i.imgur.com/ktoavEG.png)

> 填入正確驗證碼後，會自動進行頁面跳轉。

### Step 5: 大功告成!!!

![](https://i.imgur.com/asNl3n9.png)

---

## :mag: 簡單介紹 Github

![](data:image/png;base64,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)

GitHub是透過Git進行版本控制的軟體原始碼代管服務平台，由GitHub公司（曾稱Logical Awesome）的開發者Chris Wanstrath、P. J. Hyett和湯姆·普雷斯頓·沃納使用Ruby on Rails編寫而成。--- [Wikipedia](https://zh.wikipedia.org/wiki/GitHub)

### 使用 Github 的一些好處 :+1:

1. 提供遠端 repository (儲存空間) 放置原始碼
2. 使 git 後的原始碼更加透明化
3. 其他開發者可以給予意見(bug回報..)
4. 方便團隊協作開發
5. 快速找到實用的插件
6. 放置靜態網頁的免費空間 XD ...

:::info
:bulb: **Hint:** Github公司被微軟收購後，現在免費用戶也可以建立 private repository，只是付費用戶提供的功能比較多。
:::

---

## :wrench: 實際操作 Github

![](https://i.imgur.com/73Xz6rL.png)

使用到的指令:

| 指令          | 功能說明               |
| ----------------- |:----------------------- |
| `git clone 遠端數據庫網址`       | 複製遠端數據庫到本地端   |
| `git push 遠端數據庫名稱 遠端分支名稱` | 將本地分支推送到遠端分支     |



### :arrow_down: 將遠端數據庫 clone 到本地數據庫  

1. 在 github 上建立數據庫

* 點擊 New respository
![](https://i.imgur.com/UvAqh1g.png)

* 為數據庫取名、點擊建立數據庫
![](https://i.imgur.com/deIxL5a.png)

* 關於如何操作數據庫的一些說明
![](https://i.imgur.com/0nZUdMt.png)

2. 透過 https 將數據庫 clone 到本地端

* 建立資料夾、移動路徑
![](https://i.imgur.com/vIgCOT7.png)

* 用 https 形式將數據庫 clone 到本地端
![](https://i.imgur.com/0nZUdMt.png)

* 使用 **git clone** 指令、提示 **test** 是一個空的 repository
![](https://i.imgur.com/ATbXjz9.png)

* 成功 clone 到本地端
![](https://i.imgur.com/Dt5itly.png)

### :arrow_up: 將本地數據庫推送到 github 上

* 切換路徑到 **test** 下，新增 **index.html**
![](https://i.imgur.com/siMnCd0.png)

* 加入索引，**commit** 成紀錄
![](https://i.imgur.com/D0hhlbD.png)

* 推送(**push**)到遠端數據庫(github)
![](https://i.imgur.com/7rJamuN.png)

* 帳號驗證
![](https://i.imgur.com/OfbU8cz.png)
![](https://i.imgur.com/xq81YIe.png)

* 成功推送到遠端數據庫(github)
![](https://i.imgur.com/0PieaWB.png)

---

## :rocket: BONUS: 找出實用的插件

開發者通常會將一些有用的東西上傳到 github 上，其他開發者若想要使用到類似的效果，可以透過關鍵字搜尋。

### 以 js calendar 為例:

* 搜尋 **js calendar** 並選擇[數據庫](https://github.com/GramThanos/jsCalendar)
![](https://i.imgur.com/lRUdy3G.png)

* 數據庫裡通常會有如何使用插件的說明
![](https://i.imgur.com/Nm8e8SP.png)

* 使用說明與範例效果
![](https://i.imgur.com/ehu8g7f.png)

### 如何選擇合適的數據庫?

* 使用的語言
* star 的數量，愈多代表有愈多開發者的認同
* update 的時間，最好是在半年內有更新，避免與現行環境不符
* 使用說明的易讀性
* issue (bug) 是否有被妥善解決
* 環境支援與否

---
[ToC]

### Recently modified: 2021/07/18 by Qi Xiang
