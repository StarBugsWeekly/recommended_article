---
title: 第 147 期 DevOps 推薦文章
date: 2022-08-30
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Why is Kafka fast?](https://blog.bytebytego.com/p/why-is-kafka-fast)

為什麼 Kafka 這麼快？在進入正文前務必[搭配影片](https://youtu.be/UNUz1-msbOM)一起看可以幫助理解。Kafka 之所以快主要有兩個原因，Kafka 在讀寫硬碟資料時 I/O 的操作是連續性的，可以在使用 HDD 硬碟減少成本的情況下依然有不錯的速度，以及在從硬碟讀取資料要給 consumer 時靠 zero-copy 也就是靠直接記憶體存取 （Direct Memory Access，DMA）減少 system calls。文章只有說減少 system calls 而已，歡迎觀看影片。<!-- summary -->

### [Orchestration and choreography](https://blog.bytebytego.com/p/orchestration-and-choreography)

微服務之間合作時可以分為 Orchestration 和 Choreography 兩種方式。Orchestration 如常見的交響樂一般，不同樂器的音樂家都看指揮的指示；Choreography 如舞蹈表演，各個舞者跳舞的時候是沒有專門的指揮，要看整體成員的狀況而怎麼跳舞。兩種服務的合作模式各有優缺點，在規劃架構時可以考慮考慮。

### [Black Friday flash sale](https://blog.bytebytego.com/p/black-friday-flash-sale)

當黑色星期五時系統應該要做什麼準備？從前端一路到後端我們都要設法加裝各種關卡來處理真正的交易，畢竟網路上機器人太多，像是 reCaptcha、CDN、rate limit 和 lock 機制。另外也得注意處理各個交易時不要因為系統設計造成超賣，甚至可以把服務和快取做獨立，專為黑色星期五的流量做準備。
