---
title: 第 116 期 DevOps 推薦文章
date: 2022-01-18
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [My jq Cheatsheet](https://medium.com/geekculture/my-jq-cheatsheet-34054df5b650)

身為一位 SRE 或是 DevOps 應該都有使用過 jq 這個強大的 CLI 工具，透過他可以很輕鬆地在 Terminal 環境處理 JSON 格式的資料，這篇文章的作者分享了他使用 jq 來處理由 kubectl 所獲的 JSON 資料 (可以下 flag `-o json` 獲取)，去過濾自己真的需要且重要的資訊來使用

<!-- summary -->

### [Postman Now Supports gRPC](https://blog.postman.com/postman-now-supports-grpc/)

相信應該有不少人都會使用 Postman 來測試線上服務，他在最新的版本 v9.7.1 宣布支援 gRPC 協定，一旦上傳 API 的 Protobuf 定義檔案 (.proto)，Postman 就可以自動得知所有的 Service 與 Method，並且會為每一個 Method 產生對應的範例 Payload，具體的功能支援內容與使用方式，請參考內文

### [5 Best Online Tools to Check DNS Records](https://geekflare.com/online-tools-to-check-dns-records/)

當 DNS Record 設定錯誤時，將會導致你提供的服務無法正常使用，而在查詢 DNS Record 是哪邊出問題時，首先要做的當然就是先把 DNS Record 的詳細設定給撈出來好好地檢查一番，但要如何快速的檢查任何網站的 DNS Record 呢？這篇文章推薦了五個線上工具供大家使用，趕快加入到最愛書籤內，下次有需要時就可以馬上拿出來使用