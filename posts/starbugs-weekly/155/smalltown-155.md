---
title: 第 155 期 OpenSource 推薦文章
date: 2022-10-25
author: smalltown

layout: layouts/post.njk
tags: [OpenSource]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## OpenSource

<!-- summary -->
### [Postgres WASM](https://github.com/snaplet/postgres-wasm)

Postgres WASM 是一個運行於瀏覽器的 PostgreSQL Server，聽起來也太酷了，只要把該專案 `git clone` 下來之後執行 `cd packages/runtime && npx serve`，就可以使用瀏覽器拜訪 http://localhost:3000 來使用了！

<!-- summary -->

### [cidr](https://github.com/bschaatsbergen/cidr)

身為一位 SRE 其實還滿常接觸到 IP Address 的，尤其是在設定防火牆規則的時候，對於 IP 的 CIDR 總是不像坐在旁邊的同事可以一眼就看出來他的範圍嗎？這時候就可以使用這個 cidr CLI 工具來偷作弊了，他可以幫你快速的計算出 CIDR 的範圍，告訴你這個 IP Address 是屬於哪個 CIDR 的！

### [Revup](https://github.com/Skydio/revup)

想要成為 10 倍速工程師嗎？那可以考慮看看使用這個 Revup 小工具，他可以協助開發人員平行處理 Git Pull Request，透過對於 Commit Message 動手腳讓開發人員可以在本機端就同時建立多個 Git Pull Request，並且一樣也可以透過 Commit Message 來對於特定的 Pull Requet 去做後續操作，除此之外還有很多跟 Git 相關的功能，可以讓開發人員更有效率的開發。
