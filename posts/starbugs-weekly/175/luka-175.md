---
title: 第 175 期 Backend 推薦文章
date: 2023-05-31
author: luka
layout: layouts/post.njk
tags: [Backend]
---

## Backend

### [PostgreSQL 技術筆記: 跟疾管署沒有關係的 CDC](https://medium.com/dcardlab/218e27eb363d)

本文介紹了 Dcard 中使用 PostgreSQL CDC（Change Data Capture）的運作原理。Dcard 的系統架構中，許多服務元件使用 PostgreSQL 進行資料儲存。為了避免直接使用生產資料庫對效能和安全性造成影響，Dcard 採用了 Microservices 架構，將不同服務獨立部署在各自的 PostgreSQL 資料庫中。

為了方便管理和查詢，Dcard 的開發團隊開發了一個 OfflineDB Proxy 服務，通過該服務可以使用特定的 on-demand 服務來存取和管理 PostgreSQL 複本資料庫。在此基礎上，開發了 PostgreSQL CDC 技術，使複本資料庫能夠提供近乎即時的資料。通過 CDC 服務，許多其他服務元件可以通過數據流的方式獲取資料庫的異動資料，從而保證了服務間的流程設計的完整性，提供更可靠和穩定的 Dcard 服務。

文章介紹了各個模組間的設計概念，包括 OfflineDB Proxy、Snapshot Rotate Job、Postgres Protocol Handle 和 Resource Controller 等。此外，還介紹了使用 PostgreSQL Replication 機制來獲取異動資料，以及使用 Apache Pulsar 作為儲存 Change Data 的消息隊列服務。文章還提到了 pg2pulsar 和 pulsar2pg 兩個程序，用於處理 Change Data 的儲存和同步。最後，介紹了 CDC Stream Gateway，通過這個服務可以簡化應用程式與消息隊列之間的處理，提供給各種不同的流式應用程式使用。

整個系統的架構和流程如圖所示，包括 OfflineDB Proxy、CDC、和 Stream Gateway。通過這些模塊的搭建和運作，可以實現 Dcard 的即時性和異動資料的同步更新，並提供給各種不同的應用程式使用。

文章最後提到，目前 Dcard 已經在數十個 CDC Stream 應用中使用了這些技術，並且不斷進行優化和探索。同時，Dcard 還在計劃和開發其他類型資料庫的 CDC 服務，如 MongoDB 等。

（文章中有多張圖片，請參閱原文瞭解詳細內容）


### [課程筆記 - 即使通訊與傳輸（realtime、streaming、websocket）](https://pjchender.dev/webdev/course-fem-realtime/)

本篇摘要整理自 Frontend Masters 的 "Complete Intro to Real-Time" 課程。

簡介了以下主題：Long Polling（輪詢）、使用 setTimeout、requestAnimationFrame、Backoff and Retry（放棄或重試）、HTTP/2 Push、WebSocket、以及 Socket.IO。

在 Long Polling（輪詢）中，透過 AJAX 方式持續向服務器發送請求。使用 setTimeout 而非 setInterval 來進行輪詢，避免在 API 回應慢時打多次 API 請求。另外，也介紹了 requestAnimationFrame 來替代 setTimeout，以達到更好的性能和節能效果。

在 Backoff and Retry（放棄或重試）中，介紹了當 API 請求失敗時的處理機制，建議使用 backoff and retry 的方式，即在每次失敗後延遲一段時間再重試，並逐漸增加延遲時間。

在 HTTP/2 Push 中，說明了建立 WebSocket 連線的過程，包括使用 self-signed 的憑證、回傳特定的 headers 等。並介紹了如何在後端和前端進行相應的程式碼實現，以及如何處理資料的傳遞。

在自己實作 WebSocket 部分，提到了使用 WebSocket 和 HTTP 之間的協定升級過程，以及如何在後端和前端進行程式碼的實現。還提到了 WebSocket 中資料交換的格式和解析方法。

最後，介紹了使用 Socket.IO 來進行即時通訊的方式，並且提到了 Socket.IO 相對於 WebSocket 和 ws 套件的優勢，包括自動重新連線、兼容性等。

以上是本篇摘要的內容概要。詳細內容可參考相應的課程和資料來源。


