---
title: 第 124 期 後端開發 推薦文章
date: 2022-03-15
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [Rapid Event Notification System at Netflix](https://netflixtechblog.com/rapid-event-notification-system-at-netflix-6deb1d2b57d1)

Netflix 擁有超過 2.2 億活躍用戶，他們必須確保用戶在不同的裝置間進行的任何動作 (修改 Profile, 觀看電影標題...等) 保持體驗的一致性，考量到支援的眾多裝置種類和使用者可以執行的動作之多，其實這不是一件容易達成的事情，因此 Netflix 開發了一個快速事件通知系統，用來支援任何需要 Server 與裝置間溝通的使用情境，而在這篇文章中將會介紹這套系統的大致樣貌，而且分享 Netflix 在構築它時所學到的事情

<!-- summary -->

### [Code Verify: An open source browser extension for verifying code authenticity on the web](https://engineering.fb.com/2022/03/10/security/code-verify/)

自從去年 WhatsApp 推出多裝置功能之後，Meta 這邊看到越來越多人直接使用瀏覽器拜訪 WhatsApp Web，考慮到此一使用者行為轉變， Meta 這邊開始想要增加 WhatsApp Web 的安全性，所以最近推出了一個開源的瀏覽器 Extension - Code Verify，他可以自動驗證使用者拜訪的 WhatsApp Web 程式碼沒有被其他人竄改，文章內進一步 Code Verify 的運作機制與使用方式

### [Modern application load balancing with a centralized control plane](https://www.cncf.io/blog/2022/03/10/modern-application-load-balancing-with-a-centralized-control-plane-2/)

一個服務或是系統，一般來說可以分成 Control Plane 和 Data Plane，將兩者分開可以實現 Software-Defined Everything 和 Infrastructure as Code，這樣的做法可以將應用程式跟其運行的基礎設施解耦合，好處有增加執行效率，增加部署彈性，執行成本最佳化；而傳統的 Load Balancer 和 Web Application Firewalls 通常都沒有將 Control Plane 和 Data Plane 拆開來，當你處在數千個應用服務的環境中時，這樣的模式將會成為 Wordload 的瓶頸，所以文章中提到對於這類型的系統或是服務要如何將 Control Plane 集中化，並將 Data Plane 拆分開來，以及其帶來的好處