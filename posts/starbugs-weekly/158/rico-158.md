---
title: 第 158 期 DevOps 推薦文章
date: 2022-11-15
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [17 DevOps Metrics You Should Be Tracking](https://dzone.com/articles/17-devops-metrics-you-should-be-tracking)

除了服務 metrics 之外，作者建議 17 個 DevOps 相關的 metrics 也需要被追蹤，metrics 主要的方向有：<!-- summary -->
- DORA Metrics，用於測量組織開發
- Cycle Time，另外一種測量組織開發產能的 metric
- 品質，可以整合在 CI pipeline 做測量
- 客戶的回饋
- 員工滿意度，對於文件、意見是否被聆聽到、組織是否接受失敗等等
- CI 平均所花的時間、一天跑幾次、壞掉的恢復時間、測試失敗率和成功率
- 穩定率，用來測量 CICD pipeline 是否會因不明原因失敗
- Code Coverage
- 錯誤逃逸率，測量有多少正式生產環境的錯誤是 CICD pipeline 裡沒有偵測到的
- 正常運行時間
- SLI（Service Level Indicator）
- 平均意外察覺時間，當服務發生意外時，要多久 on-call 人員才會被分配搶救任務
- 平均意外發生時間，當新的功能上線後多久才會有意外

### [Technology in the Cloud Native Maturity Model](https://www.cncf.io/blog/2022/11/09/technology-in-the-cloud-native-maturity-model/)

CNMM（Cloud Native Maturity Model）用於檢視組織 Cloud Native 轉型是否成熟，並且以 5 個面向來做分析：商業產出、人、政策、流程和技術。除了本文外，可以直接看 CNCF GitHub 有更詳細的[說明](https://github.com/cncf/cartografos/blob/main/reference/prologue.md)

### [9 Best Practices for Designing Microservice Architectures](https://traefik.io/blog/9-best-practices-for-designing-microservice-architectures/)

微服務一直都不容易駕馭，作者推薦 9 個實踐方法（但裡面只有 8 點）讓微服務架構設計更成功：
1. 嘗試事件風暴
2. 實踐情境繪製
3. 在一開始規劃好網路
4. 盡量自動化
5. 了解遷移到微服務真正的原因是什麼
6. 工具互動性保持簡單
7. 架構保持彈性
8. 考慮使用混沌工程