---
title: 第 126 期 後端開發 推薦文章
date: 2022-03-29
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [Multi-Tenant Application](https://levelup.gitconnected.com/multi-tenant-application-a29153d31c5a)

所謂的 Multi-Tenancy 概念就是眾多的使用者在看不到彼此資料的前提之下，一起分享運算資源，網路和儲存裝置，所以 Multi-Tenancy 應用程式必須讓每一群使用者 (或稱為 Tenant) 可以去客製化，但是整個架構和核心功能仍然保持一致，所以 Multi-Tenancy 也是 SaaS 廠商常常採用的方式，讓資源利用達到最大化
<!-- summary -->

💡 使用案例
以 Multi-Tenant 的架構來說通常適合下列的應用情境：
👉 ＳaaS (software as a service) 或是  AaaS (application as a service)
👉 PaaS (platform as a service)
👉 IaaS (infrastructure as a service)
👉 對於那種擁有眾多 Client 且都使用相同演算法推疊起來的應用服務，也就是說主要的功能都一樣或是已經模組化，而且可以滿足不同使用者的需求

💡 Multi-Tenant vs. Single-Tenant
為了更深入了解，讓我們來了解 Multi-Tenant 和 Single-Tenant 兩者分別是如何運行的

👉 Single-Tenant: 每個使用者獲得專用的運算，網路和儲存資源，每個環境都是獨立開發與管理，本質上來說就是不允許共享任何的資源
👉 Multi-Tenant: 允許在同一個環境中服務多個客戶且重複使用程式的核心功能，每個 Tenant 都是隔離且無法看到彼此，同一個環境的資源只有在邏輯上是切開的，實體上是共享的，好處是可以簡化安全性上的管理，更容易負擔的 Licensing 授權，將時間投資在彼此共用的核心功能上，而不是去開發很多功能不同且分歧的程式

💡 不同的 Multi-Tenancy 資料庫管理方式

👉 Single Database + Single Schema:
Tenant 間資料的隔離是這種作法最需要注意的地方，可能可以使用例如 TeantID 或是 ClientID 的 Database Index 來讓資料具有隔離的效果
😊 好處: 跟其他方式比起來維護相對容易，可以任意增加新的客戶
😢 壞處: 對於需要不同資料使用方式的客戶來說彈性太低，會需要為了非典型客戶特別去做特別的修補；需要耗費很大的心力去妥善分離資料庫使用權限，然後再備份和還原時也會遇到問題，因為所有客戶的資料都混合在一起，所以無法擁有個別政策

👉 Single Database + Multiple Schemas: 利用多個 Table 來拆分不同客戶的資料，Schema 變得像是 Namespace 一樣包含特定的 Table, Procedure 和權限
😊 好處: Schema 在 DBMS 層級上算是達成安全地共享存取，只需擁有少數的資料庫，意味著更少的硬體資源，彈性相對高，假如需要新的 Schema，可以根據既有的去建立起來，再根據需求做客製化即可
😢 壞處: 不同客戶的資料還是存放在一起，因為只是邏輯性的隔離而不是物理性，因此再備份和還原上還是會遭遇問題，因為只有一個資料庫，假如其中有什麼東西壞掉了，所有在資料庫中的東西就必須跟著一起恢復到正常時的狀態，但裡面有不同客戶的資料，這樣是不可被接受的，所以管理者可能會需要合併新舊資訊，這可能不是那麼地簡單

👉 Separate Databases: 多個資料庫的模式可以達成程式碼和資料在觀念上是共享 (透過共同的使用者介面和商業邏輯)，但在不同的客戶之間是實體分離
😊 好處: 增加一個新的客戶時，只需要設定一組新的資料庫；當不同的客戶擁有自己的 Database 時，要擴展也相對容易，要針對不同的客戶去做客製化也容易，再備份和還原也不用擔心上面遇到的問題
😢 壞處: 成本昂貴！在硬體和管理層面上都是

### [1 min guide to Golang development best practices in 2022](https://blog.canopas.com/1-min-guide-to-golang-development-best-practices-in-2022-b50d846fd6c)

推薦一篇不錯的小品，作者希望用最短的時間讓讀者快速了解在 2022 的當下，開發 Golang 時必使用的函示庫和最重要的小事，讓 Golang 開發者天天擁有高效率與簡易的開發人生 😊

01. 熟悉如何使用 Go Modules 來管理 Golang 套件相依性
02. 使用 Gin 來構建 Web API
03. 透過 Repository Structure 來避免濫用全域變數 
04. 利用 SQLX 來完成資料庫查詢作業
05. 一定要在 API 加上認證機制
06. 使用 Microservices 的概念來撰寫 API 功能
07. 輸出良好的 Log 來追蹤錯誤或是臭蟲，例如 Zap, Logrus
08. 使用 HttpTest 和 asset 來做測試
09. 使用 Redigo 來處理跟 Redis 的連線
10. 利用 CI/CD 來自動化開發流程
11. 讓 pre-commit hooks 幫助省下 commit 前要花費的時間

### [macOS Tools and Apps for Development in 2022](https://medium.com/@etc088/macos-tools-and-apps-for-development-in-2022-963bd4d0f876)

相信有不少人使用 macOS 來當作日常的開發環境，正所謂工欲善其事必先利其器，這篇文章的作者表示雖然網路上有不少介紹 macOS 相關的開發工具文章，不過好像介紹的東西對他來說都不那麼有用，有些甚至還讓他浪費更多寶貴的時間

所以他決定自己寫一篇來介紹真的對改善他自己工作效率有效的 macOS 開發工具大補帖💪 底下簡易列出分類和名稱，有興趣的人可以直接參閱內文通通裝起來 🤩  (自己覺得這個作者應該是比較偏前端一點的工程師，不過他推薦的東西，我這個 SRE 也使用超過一半以上 👍 )

📚 Terminal 工具類
🛠️ Homebrew: macOS 套件管理工具
🛠️ iTerm2：取代 macOS 預設 Terminal 
🛠️ ZSH: 構築於 Bash 上的 Unix Shell, 目前已經是預設
🛠️ Oh My ZSH!: Zsh 套件，組態管理工具
🛠️ Fig: 讓 Terminal 也有 VSCode 般的自動完成功能
🛠️ Volta: 可以想像是更好的 NVM 工具 
🛠️ Ngrok: 允許在自己的本地端環境擁有一個公開且對外的網站

📚 桌面軟體
🛠️ VS Code 跟他的 plugins 小夥伴們: Auto Close Tag, Auto Rename Tag, Bracket Peek, GitLens, Import Cost, Indent-Rainbow, Path Intellisense, Project Manager, Shortcut, Menu Bar, Thunder Client, Trailing Spaces, Turbo Console Log
🛠️ GitKraken: Git 的 GUI 工具
🛠️ ResponsivelyApp: 檢視在不同視窗大小時，網站的呈現會是如何
🛠️ RunJS: JavaScript 的 playground 工具
🛠️ Altair GraphQL Client: 協助除錯 GraphQL 搜尋和實作

📚 其他工具
🛠️ Moom: 視窗管理工具
🛠️ CleanShot X: 強大的截圖工具
🛠️ Sli.dev: 一個線上投影片製作與呈現工具
🛠️ Notion: 讓你紀錄任何事情的服務