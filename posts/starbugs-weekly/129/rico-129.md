---
title: 第 129 期 DevOps 推薦文章
date: 2022-04-19
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Finding Vulnerable Info Using Google Dorks — Ethical Hacking](https://infosecwriteups.com/finding-vulnerable-info-using-google-dorks-ethical-hacking-23f358117ceb)

此篇撰寫了如何用 Google 搜尋引擎的特性尋找敏感的資訊，例如：鎖定檔案類型為 log 且內容含有 username 的結果，以及尋找可以直接看的公開線上鏡頭（我第一個搜尋結果可以看到塞爾維亞街頭攝影機的即時影像），其實推薦這篇不為別的，就是希望提醒大家維運系統時盡量不要把 credential 上傳到網路上啊！<!-- summary -->

### [OpenTelemetry, the standardized observability framework for everyone](https://blog.devgenius.io/opentelemetry-the-standardized-observability-framework-for-everyone-76b10c4148f7)

OpenTelemetry 算是在業界引起了一波浪潮，其提供完整的 APIs、SDKs、工具和整合讓 tracing、metrics 和 logs 可以得到更好地整合。作者分享自己整合 jaeger 和 datadog 的經驗和 demo，另外作者也有把 demo code 上傳到 Github 上，有興趣的可以照著文章的步驟做。

### [How to Generate Terraform Code with Opta](https://blog.runx.dev/how-to-generate-terraform-code-with-opta-f255f71c73d3)

作者介紹 Opta 是以 Terraform 為底層做抽象化封裝，與之相比 Terraform 太多底層的細節要注意，在建造 infrastructure 堆積木的過程中很容易有設定錯誤的情況發生。反之，向 Opta 表示意圖並且產出 Terraform files 之後也可以對 Terraform files 做細節的調整，相比之下使用 Opta 是比較人性化的。不過此專案還算早期，抽象化的封裝還不夠多而且都以 AWS 為主，但可以看得出來團隊很認真經營社群，slack channel 都還算活躍。