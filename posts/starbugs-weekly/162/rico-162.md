---
title: 第 162 期 DevOps 推薦文章
date: 2022-12-13
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Serverless vs. Kubernetes: The People’s Vote](https://thenewstack.io/serverless-vs-kubernetes-the-peoples-vote/)

AWS Re:Invent 活動上舉辦了 Serverless vs Kubernetes 架構比賽，會依據多個分類角度做票選，分類的項目有：<!-- summary -->
1. 維護性 - Serverless 勝
2. 成本 - Serverless 勝
3. 擴展性 - Serverless 勝
4. 開發友善度 - 雙方平手
5. 生態系 - Kubernetes 勝
6. 監控與日誌 - Kubernetes 勝
7. 資安 - Kubernetes 勝

### [BuildRock: A Build Platform at Slack](https://slack.engineering/buildrock-a-build-platform-at-slack/)

Slack 一開始的 Jenkins 就和大家的 Jenkins 一樣隨心所欲導致愈來愈多技術債，經過一連串的考量後決定繼續使用 Jenkins，並且開始做左移的測試，在 Kubernetes 上使用臨時的 Jenkins agent，並且用外掛硬碟保存狀態，標準和抽象化讓使用 Jenkins 的體驗好一點，另外也引入 GitOps 概念禁止人們手動改動，改善設定管理，以及放權 ownership 讓 service owner 參與建置 pipeline。

### [Looking to the Future of Developer Experience](https://devops.com/looking-to-the-future-of-developer-experience/)

開發體驗就跟使用者體驗一樣非常重要，減輕開發人員精神上的打擊讓生產力能夠提升。打從一開始入職開始、開發、部署時和維護就要時時刻刻注意開發體驗，像是在入職時創帳號時會自動生產需要的密鑰，使用開發工具如 [Fig](https://fig.io/)、[Github Copilot](https://github.com/features/copilot)、low-code 的軟體或者一些自動化工具如 [Githube Action](https://github.com/features/actions)，而維護需要注意的是 dependencies 要能夠自動檢查。