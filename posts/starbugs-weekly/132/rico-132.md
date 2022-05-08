---
title: 第 132 期 DevOps 推薦文章
date: 2022-05-10
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [CDNs aren't just for caching](https://jvns.ca/blog/2016/04/29/cdns-arent-just-for-caching/)

作者表示 CDN 不是只有 caching 而已，加快 TLS handshake、更好的網路 routing 和阻擋 DDoS 攻擊。作者對是不是 CDN 有更好的資安打上了一個問號，因為很多資安的設定都不是掌握在自己手裡而是交給 CDN 服務商。還有一點就是把 SSL 證書給 CDN 並且傳遞敏感的資訊，你無法知道使用者的資料是不是真的安全的，對此情況政府也有所顧慮。<!-- summary -->
最後就是 CDN 的設定和 CDN 故障這兩點都會影響網站的可靠性，作者也希望可以找到大廠 CDN 的 SLAs 是否符合的統計數據，但都沒找到。作者也推薦大家可以看看 Cloudflare 的技術文章。

### [Reasons for servers to support IPv6](https://jvns.ca/blog/2022/01/29/reasons-for-servers-to-support-ipv6/)

IPv6 可以解決 IPv4 address 不足的問題，但實現起來困難重重，很多時候是 ISP 並不支援。作者以很多的觀點解釋為什麼即使 IPv4 和 IPv6 可以切換自如但還是建議 server 支援 IPv6，最有趣的大概就是 Facebook 在他的 IPv6 裡面藏了 `face:b00c` 的彩蛋。

### [A list of new(ish) command line tools](https://jvns.ca/blog/2022/04/12/a-list-of-new-ish--command-line-tools/)

作者在 twitter 上問有什麼新潮的 command line 工具，結果大家的回覆非常多元甚至沒聽過，於是作者整理了一份工具清單，其中有替代舊工具的新選擇、完全創新的工具、JSON/YAML/CSV 資料處理工具、grep 各種東西的工具，最後作者也有推薦他喜歡的是什麼。