---
title: 第 152 期 OpenSource 推薦文章
date: 2022-10-04
author: smalltown

layout: layouts/post.njk
tags: [OpenSource]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## OpenSource

<!-- summary -->
### [workerd](https://github.com/cloudflare/workerd)

[workers](https://workers.cloudflare.com/) 是 CloudFlare 所推出的 serverless runtime 解決方案，當初看到時覺得 CDN 這樣算不算撈過界了XD 而官方在最近宣布將其開源了，所以大家可以在自己的環境中使用 workderd 來架設 serverless 服務，不過現在還在 beta 階段，所以還是要小心使用！

<!-- summary -->

### [whisper](https://github.com/openai/whisper)

Whisper 是最近由 OpenAI 所發表的自動語音辨識（ASR）系統，他透過大量的語音資料所訓練而來，而且他的模型也是開源的，所以大家可以自己來訓練一個模型，或是直接使用他來做一些有趣的事情，例如我就看到馬上有人利用他來[將 youtube 影片變成文字版](https://github.com/sensahin/YouWhisper)！

### [mixctl](https://github.com/inlets/mixctl)

mixctl 是一個使用 golang 所開發的小巧 TCP Load Balancer，他主要是希望可以幫助使用者將架設於不同地方的多個服務透過單一個 TCP Tunnel 給串接起來，使用起來滿簡單的，只需要透過 yaml 格式將 routing 設定好，然後就可以透過 mixctl 來啟動這個 TCP Tunnel 了，感覺是本地端開發的好幫手！