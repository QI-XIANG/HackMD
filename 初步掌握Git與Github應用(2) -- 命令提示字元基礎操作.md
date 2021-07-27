# 初步掌握Git與Github應用(2) -- 命令提示字元基礎操作

###### tags: `初步掌握Git與Github應用`

> 希望藉由這份筆記，讓正在學習這類知識的你/妳，能夠得到些許幫助。:smile: 

:::info
:bulb: **Hint:** 以下筆記內容所使用的作業系統為"Windows 10"

:::

## :memo: 如何開始?

### Step 1: 打開你的 **Git Bash**

:::info
:bulb: **Hint:** 注意，這裡的操作都是在 Git Bash 上執行，下面使用的指令出自 Linux 作業系統，在本機 CMD 輸入下方指令可能無法執行。
:::

![](https://i.imgur.com/ggHuLTx.png)

![](https://i.imgur.com/mo7PREn.png)


### Step 2: 確認要使用到的基本指令

| 功能說明       | 指令               |
| ---------- |:------------------ |
| 移動路徑   | `cd 路徑`          |
| 回上一層   | `cd ..`            |
| 展開列表   | `ls`               |
| 開新資料夾 | `mkdir 資料夾名稱` |
| 開新檔案   | `touch 檔案名稱`   |


### Step 3: 指令練習

1. 移動路徑至C槽
![](https://i.imgur.com/hp0rNGh.png)

2. 查看C槽下的檔案、資料夾 
![](https://i.imgur.com/wmUAG00.png)

3. 移動路徑到特定資料夾
例如: Program Files
![](https://i.imgur.com/DykLDiv.png)

> 當路徑名稱有空格時，記得使用 **單引號(')** 包住路徑名稱，像是 **'Program Files'**。

4. 回上一層
![](https://i.imgur.com/d9Fj7Jq.png)

5. 開新檔案
![](https://i.imgur.com/a7UWal9.png)

6. 開新資料夾
![](https://i.imgur.com/68xE1nh.png)

7. 檢視
![](https://i.imgur.com/QQZLSGs.png)

:::info
:pushpin: 想學習更多 Linux 指令? ➜ [Linux 基本指令介紹](https://linux.vbird.org/linux_basic/redhat6.1/linux_06command.php) 
:::

---

## :rocket: BONUS: Git 環境設定

設定 Git 版本更新的資訊

| 功能說明          | 指令               |
| ----------------- |:----------------------- |
| 查詢 Git 基本設定參數值      | `git config --list`   |
| 設定該版本作者的email | `git config --global user.email "你的email"`     |
| 設定該版本作者的name         | `git config --global user.name "你的名字"`     |

* 基礎設定
![](https://i.imgur.com/16TZoZG.png)


* 查詢是否成功設定
![](https://i.imgur.com/ufMelLc.png)
---

[TOC]

###### Last updated 2021/07/12 by Qi Xiang