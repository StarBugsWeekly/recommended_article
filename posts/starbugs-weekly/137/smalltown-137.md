---
title: 第 137 期 系統監控 推薦文章
date: 2022-06-21
author: smalltown

layout: layouts/post.njk
tags: [Monitoring]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Monitoring

<!-- summary -->
### [Grafana OnCall OSS](https://grafana.com/oss/oncall/)

Grafana 開源了 On Call 管理工具，就叫做 On Call XD 感覺滿值得一試的！ On Call 需要的功能都已經包含其中，例如整合第三方 Calendar 與通知服務 (Slack, Telegram, Voice, SMS)，Escalation 的設定，Alert 的 Grouping，一個集中化顯示 Alert 的地方...等，有興趣的人可以參考 [Get Started 文件](https://grafana.com/docs/grafana-cloud/oncall/getting-started/) 和他的 [GitHub Repository](https://github.com/grafana/oncall)

<!-- summary -->

### [What makes VictoriaMetrics the next leading choice for open-source monitoring](https://medium.com/everything-full-stack/what-makes-victoriametrics-the-new-de-facto-standard-choice-for-open-source-monitoring-5d2b66b6e292)

近幾年來談到開源的監控解決方案時，大家應該都會選擇 Prometheus Stack，其中由 Grafana, Alertmanager 和各種 Exporter 所組成，但作為一個快速成長的生態系，他有著一些問題，例如他是一個效能堪憂的單體式應用程式，從設計上就缺乏有關 HA 的考量，擴展性複雜與不足，當保存的資料超過 14 天時就會造成效能降低與擴展困難

所以作者最近在研究開源監控解決方案時，覺得監控系統應該要具備高效能，高可用，便宜，易擴展，能備份且儲存相對久時間週期的資料 ，再把 Thanos, Cortex, Grafana-Mimir 和 VictoriaMetrics 都拿出來比較過一輪之後覺得 VictoriaMetrics 應該會是最符合這些需求的贏家，想要知道為什麼的人可以參考詳細內文

### [How to Handle Terabytes of Metrics in Kubernetes Monitoring](https://medium.com/@holidu/how-to-handle-terabytes-of-metrics-in-kubernetes-monitoring-a3056adf92b)

在基礎設施中 Monitoring 當然是相當重要的一環，它能夠協助遇見事故的發生，並且避免服務產生不預期的 Downtime，在作者的公司 Holidu 因為不斷增加的客戶導致基礎設施的不斷增長，每秒所產生約 4 萬個 Metric 的樣本資料，導致監控設施不堪負荷且增加了營運的成本；在此挑戰之下，作者的公司顯然需要一個新的可擴展且穩定的監控系統，所以他們將原來使用的 Prometheus 架構透過 Thanos 重新改進，用以順利處理每秒 4 萬個 Metric 的樣本資料，想要知道詳細做法的話，可以參閱詳細內文
 