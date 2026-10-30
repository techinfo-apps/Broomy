<p align="center"><img src="icon.png" width="128" alt="小掃帚圖示"></p>

# 小掃帚（Broomy）

[English](README.md) · [简体中文](README.zh-CN.md) · **繁體中文** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md)

一個小而老實的 Mac 清理工具。小掃帚找出可以放心刪除的東西，解除安裝 App 時連它留下的東西一起帶走，順便看著 Mac 的溫度、硬碟健康和顯示器。在你確認之前什麼都不刪，刪的東西也都先進垃圾桶。免費，沒有廣告，從不連網。

<p align="center">
  <img src="screenshots/overview-zh-Hant.png" width="720" alt="小掃帚的總覽頁：找到的垃圾、CPU 溫度、硬碟健康和顯示器亮度">
</p>

## 下載

**[Broomy 1.2](https://github.com/techinfo-apps/Broomy/releases/latest)**：需要 macOS 14 以上，Apple 晶片和 Intel 都可以。打開 .dmg，把小掃帚拖進「應用程式」。

這個 App 還沒經過 Apple 公證，第一次打開時 macOS 會擋一下。macOS 14：**按右鍵點小掃帚 → 打開 → 打開**。macOS 15 及以後：先打開一次，再到**系統設定 → 隱私權與安全性**，往下捲，點小掃帚旁邊的**強制打開**。

只從這裡的 [Releases](https://github.com/techinfo-apps/Broomy/releases) 或官網 https://techinfo-apps.github.io/ 下載小掃帚。Releases 頁面上每個檔案都標著 SHA-256，可以核對下載的檔案沒被改過。

每個版本加了什麼：[版本紀錄](CHANGELOG.zh-TW.md)。

### Linux

**[小掃帚 Linux 版 0.1.0](https://github.com/techinfo-apps/Broomy/releases/tag/linux-v0.1.0)** 是終端機裡的一個指令 `broomy`。64 位元的 Linux（x86_64 或 ARM）都能直接用，不用另外安裝任何東西。

Ubuntu、Debian 和它們的兄弟們：

    wget https://github.com/techinfo-apps/Broomy/releases/download/linux-v0.1.0/broomy_0.1.0_amd64.deb
    sudo apt install ./broomy_0.1.0_amd64.deb
    broomy

（ARM 電腦換成 `broomy_0.1.0_arm64.deb`。） 別的 Linux：下載 `broomy-0.1.0-linux-amd64`（或 `-arm64`），`chmod +x` 之後直接執行。

`broomy` 只看、只列：快取、舊專案的建置檔案夾、「下載」裡的安裝檔、snap 的舊版本、下載過的軟體套件和日誌。`broomy show 3` 看某一項裡有什麼，`broomy clean` 問過你之後清理打了 ✓ 的幾項。你的檔案放進垃圾桶，檔案管理員裡能放回去；系統的幾項用系統自己的指令，會問你密碼。從不連網。

<p align="center"><img src="screenshots/linux-scan-zh-Hant.png" width="720" alt="終端機裡的小掃帚 Linux 版：找到的東西按類列出，帶大小"></p>

## 一頁一個功能

兩指左右滑動、點頂部的頁籤，或按 ⌘1…⌘7 換頁。

### 清理垃圾

找出可以放心刪除的垃圾，動手之前把每一樣是什麼都寫清楚。

- **開發工具**：Xcode 的建置資料、快取、裝置支援檔案、封存和模擬器；Gradle、Homebrew 的下載；pip、npm、pnpm、Yarn、Bun、CocoaPods、Swift Package Manager、Go、Cargo 的快取；30 天沒人改過的專案裡的建置檔案夾（node_modules、.build、target、dist、Gradle 的 build），git 追蹤的東西一律不動。
- **App 快取和日誌**，還有留在「下載」和桌面上的安裝檔。
- **已刪除 App 的殘留**：App 刪掉了，它的登入項目和背景服務還在，macOS 一遍又一遍地想啟動它們。系統檔案夾裡的那些，移除時會用 macOS 自己的對話框問一次密碼。

值得多看一眼的（裝置支援檔案、封存、模擬器、安裝檔、舊專案的建置檔案夾）預設不勾。

<p align="center">
  <img src="screenshots/main-zh-Hant.png" width="620" alt="清理垃圾：開發工具的快取和大小">
</p>

### 解除安裝

解除安裝一個 App 時，連它的容器、快取、設定、應用程式支援檔案、視窗狀態、網頁資料和登入項目一起移走，每一樣都寫著大小。依 App 的識別碼（和它裡面輔助程式的識別碼）去找；只是名稱一樣的檔案夾會列出來，但不勾。Apple 的 App 不列；正在執行的要先結束；別的 App 共用的檔案不動；App 本身若移不走，其他的也都不動。

<p align="center">
  <img src="screenshots/uninstall-zh-Hant.png" width="620" alt="解除安裝：一個 App 和屬於它的所有東西">
</p>

### 搬移到外接硬碟

很少用的 App、一個月沒打開的大檔案，可以放到外接硬碟上，想用的時候隨時搬回來。小掃帚列出 100 MB 以上的 App，寫著最近 90 天用過幾天；還有「下載」「桌面」「文件」「電影」裡 500 MB 以上、30 天沒打開也沒改過的檔案。你不勾選、不確認清單，什麼都不會動。

每一樣先拷貝到硬碟上的「Moved by Broomy」檔案夾，再跟原件比對（檔案、大小、內容，App 還要驗證簽章），都對上了原件才進垃圾桶；App 會在原位置留一個連結，照樣能打開（原本在 Dock 裡的，要重新拖進去）。任何一步不對，拷貝刪掉，原件留在原處。**搬回**也是同樣的步驟，反過來走。

App 只放固態硬碟：放在傳統硬碟上打開會很慢，所以傳統硬碟只放檔案；硬碟沒有說明是哪一種時，由你來選。硬碟要格式化為 APFS 或 Mac OS 擴充格式。App Store 裝的、用安裝程式裝的、會在背景執行的、正在執行的 App 留在原處，每一個都寫著原因。第一次搬移 App 時，macOS 可能會請你在「系統設定」的「App 管理」裡允許小掃帚。外接硬碟通常不在「時光機」備份範圍內；清空垃圾桶之後，空間才會真正騰出來。

<p align="center">
  <img src="screenshots/move-zh-Hant.png" width="620" alt="搬移：很少用的 App、一個月沒打開的大檔案，和能放它們的硬碟">
</p>

### 系統狀態和硬碟健康

每個核心的 CPU 使用率、記憶體和記憶體壓力、啟動磁碟空間、CPU 和固態硬碟的溫度、風扇轉速。內建固態硬碟：總共寫了多少、硬碟自己估計的磨損、錯誤計數，都是直接從硬碟讀取；還有最近 30 天每天寫入多少、已用空間怎麼變。

<p>
  <img src="screenshots/system-zh-Hant.png" width="49%" alt="系統狀態：CPU、記憶體、啟動磁碟、溫度和風扇">
  <img src="screenshots/disk-zh-Hant.png" width="49%" alt="硬碟健康：已用壽命、總寫入量、每天寫入">
</p>

### 周邊裝置

調整顯示器的亮度和音量，外接顯示器也可以（透過 DDC）。調不了的會直說：不支援、為什麼、可以試試什麼。還有聲音輸出的音量、更順手的滑鼠滾輪（反轉方向、平滑捲動），以及外接硬碟、USB 和 Thunderbolt 裝置。

<p align="center">
  <img src="screenshots/devices-zh-Hant.png" width="620" alt="周邊裝置：每台顯示器的亮度和音量，以及調不了的原因">
</p>

### 選單列

願意的話，小掃帚可以常駐選單列：掃把圖示旁邊顯示垃圾大小或 CPU 溫度，再加一個小太陽，點一下就能調亮度和音量。

## 隱私

- **從不連網。** 小掃帚裡沒有任何連網的程式碼；僅有的連結（這個頁面、信箱）都是你點了才在瀏覽器或郵件裡打開。
- 什麼都不收集，什麼都不往外送。紀錄（每天寫入、已用空間）只留在這台 Mac 上；「記下每個 App 在哪幾天開啟過」也一樣，預設關著，在設定裡打開了才記。
- 在外接硬碟上只動自己的「Moved by Broomy」檔案夾，而且要你確認搬哪些；也從不顯示序號。
- 移走的東西都進垃圾桶，清空之前隨時可以放回去。

## 語言

English、简体中文、繁體中文、日本語、한국어、Español、Français、Русский、हिन्दी。翻譯有不對的地方，歡迎寫信告訴我們（地址在下面）。

## 意見回饋

techinfor404@gmail.com，或在這裡開 issue。

小掃帚免費使用，原始碼不公開。

---

**永遠免費，永遠沒有廣告。** 只做小而美的軟體和小遊戲。免費，無廣告，守護你的隱私——資料只留在你自己的裝置上。

聯絡：techinfor404@gmail.com · 官網：https://techinfo-apps.github.io/

<details>
<summary><img src="donate/coffee-cup.png" width="18" height="18" alt=""> 請作者喝咖啡</summary>

自願的，不請也一樣用。每一杯咖啡，都會變成下一次更新。

<p>
<img src="donate/wechat.png" height="220" alt="微信支付">
<img src="donate/alipay.png" height="220" alt="支付寶">
<img src="donate/paypal.png" height="220" alt="PayPal">
</p>

</details>
