# 初步掌握Git與Github應用(1) -- Git環境建置
###### tags: `初步掌握Git與Github應用`
> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: 安裝Git

### Step 1: [前往Git官方網站下載Git](https://git-scm.com/)

![](https://i.imgur.com/9xK19iI.png)

* 根據作業系統的不同，網頁會自動偵測適合的版本，點擊紅框中的下載按鈕即可。

### Step 2: 執行安裝檔

原則上用**預設**的設定就好，持續點擊"Next"，最後點擊"Install"即可完成安裝。

![](https://i.imgur.com/a1Enqzn.png)

![](https://i.imgur.com/WcchtR4.png)

![](https://i.imgur.com/dnbOcLF.png)


* 點擊"Finish"結束

### Step 3: 確認是否成功安裝

請打開"命令提示字元(CMD)"並輸入`git --version`。

![](https://i.imgur.com/LDZd2WT.png)

:point_up_2: 看到類似上方的結果，則表示已成功安裝Git。

### Step 4: 查看Git資料夾

![](https://i.imgur.com/ahalZef.png)

![](https://i.imgur.com/rxTPrZy.png)

:point_right: 我們主要會用到的3個東西: **Git Bash、Git CMD、Git GUI**。(特別是 **Git Bash**)

:::info
:bulb: **Hint:** 預設安裝路徑為**C:\Program Files\Git**
:::

---

## :rocket: BONUS: 更新現有的Git

如果目前的版本是早於 **2.14.1** 版，請到 Git 官網[下載](https://git-scm.com/)新版，解除安裝本機的 Git 後手動安裝新版，因為這之前的版本沒有提供更新的指令。

如果目前的版本是介於 **2.14.2** 和 **2.16.1** 之間，可以使用 `git update` 進行升級。

如果目前的版本是 **2.16.1** 以上，請使用 `git update-git-for-windows` 進行升級。

不管是使用哪個指令進行升級，他背後其實也是幫你解除安裝，然後下載新版安裝，但至少不用打開瀏覽器自己去網頁下載。

--- 資料來源: [更新本機 Git 到最新版](https://blog.poychang.net/git-update-to-latest-version/)

:::info
:bulb: **Hint:** 以上指令都是輸入在 **命令提示字元(CMD)** 上。
:::

---

[ToC]

###### Last updated 2021/07/11 by Qi Xiang

