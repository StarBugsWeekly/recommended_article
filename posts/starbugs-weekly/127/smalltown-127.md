---
title: 第 127 期 後端開發 推薦文章
date: 2022-04-05
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [WhatsApp System Architecture](https://medium.com/interviewnoodle/whatsapp-system-architecture-8df0250d572f)

WhatsApp 是在歐美相當普遍的即時通訊軟體，幾乎人人都會使用到，假如要設計這麼樣的一個即時通訊軟體服務要怎麼做呢？首先類似的聊天系統其實分成兩大類，一類是像 Facebook Messenger 會永遠儲存所有的聊天訊息，另外一類是像 WhatApp 一旦訊息被使用者接收後，就會從系統端被移除掉，知道這個最主要的不同點之後，作者開始做主要功能需求分析，例如：支援 1 對 1 聊天，支援離線傳送訊息，支援傳送訊息給離線使用者，支援群組聊天...等
<!-- summary -->

並且根據這些需求將約略的系統元件架構圖給勾勒出來，緊接著開始最精彩的部分，針對每一個系統元件去做分析，從 Profile 資料庫與服務，負責 Mapping 的資料庫，Group 服務，訊息儲存的機器跟資料庫，多媒體訊息的處理機制，然後在不同的前端平台與後端各自需要哪一些語言或是作業系統，都條列出來，最後再繪製出更完整詳細的系統架構圖，整篇文章是一個很完整的系統逆向工程，感覺是要成為一個架構師的必備技能！

### [How to Become a Blockchain Developer](https://python.plainenglish.io/how-to-become-a-blockchain-developer-1b5090e56420)

最近讀到不少新聞指出矽谷很多大企業員工都紛紛跳槽到跟 Web 3.0 相關的產業，畢竟這可能是下一個網路世界變革的前哨戰，其中的區塊鏈產業或是部門也在各大企業挖角中，薪水也都開得不錯，不過假如想要成為一名區塊鏈工程師一起往 Web 3.0 的世界前進的話， 會需要具備什麼樣的能力呢？

其實區塊鏈工程師還可以分成兩類，一類是區塊鏈核心開發人員，負責研究，設計和開發架構面，安全面和底層協議，或是其他與區塊鏈相關的技術，基本上會是負責監督整個區塊鏈網路的角色；另外一類是區塊鏈軟體開發人員，他們負責開發去中心化應用程式 (DApps)，網路應用服務和智能合約，所以建議需要從幾個特定領域開始著手學習起，包含 Blockchain 架構，資料結構，密碼學，智能合約和網路應用程式，對於成為區塊鏈工程師有興趣的話，可以參閱詳細文章內容

### [How to Use SSH Config File to Boost Your Productivity](https://betterprogramming.pub/use-ssh-config-file-to-boost-your-productivity-b3867ce8cbfe)

現今的工作環境避不掉需要連接很多的遠端機器，有可能是要部署，管理或是為程式碼除錯，而隨著連接機器數量的上升，越來越不可能將所有的 IP, Port 跟 Credential 存放位置給通通記住，這時候就需要依靠 SSH Config File 來解決這個問題。一般來說要透過 SSH 登入某一台機器時的指令會類似底下這樣：

```
ssh -i ~/.ssh/smalltown.pem ubuntu@10.1.2.3.4
```

不過透過妥善設置的 SSH Config File 可以讓你的登入指令更加簡單，使用者就不再需要去記得要使用什麼 IP, Port, Credential 等等，而只要輸入目標名稱就可以了

```
#  登入指令
ssh smalltown
```

```
# SSH Config File
Host smalltown
  HostName 10.1.2.3.4
  User ubuntu
  IdentityFile ~/.ssh/smalltown.pem
```

而 SSH Config File 還可以透過類似正規表示式來設定，例如使用 * 來代表多個字元，？ 來代表單一字元，！代表不符合的字元，例如可以設定 Alpha 的機器要使用什麼樣的使用者名稱與 Credential，Production 的 Log Level 要是什麼...等，隨自己的需求組合出適合自己的 SSH Config File，讓自己事半功倍，更多詳細的資訊可以參閱內文