---
title: 第 128 期 DevOps 推薦文章
date: 2022-04-12
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Camel K — “Containerless” Deployments on Kubernetes](https://itnext.io/camel-k-containerless-deployments-349da12bfa9d)

Camel 是一款幾乎可以整合所有系統跟服務的輕量整合框架，而 Camel K 則是專門用在 Kubernetes 上的套件，只要 developer 寫好 code 邏輯就可以直接部署上 Kubernetes 裡面，不用特別定義 container image 或寫 Kubernetes yaml，減少開發人員驗證想法的時間。<!-- summary -->雖然文章的標題寫說 containerless，但跟 serverless 的想法也很雷同，總體而言，該工具或許值得一試。

### [Version Control and Artifact Management](https://rickhw.github.io/2022/04/06/SoftwareEngineering/Artifact-Management-and-Version-Control/)

作者討論了關於 CICD 源頭的分支策略，與 CI 與 CD 中間 Artifact Management 的關係。分支策略會影響到 pipeline 複雜度，作者提到很多眉角需要去思考怎麼設計最好，打包 artifact 也建議使用 semantic versioning。萬變不離其宗的是，設計這些 pipeline 還是要給團隊使用的，必須隨時接受成員們的 feedback。

### [Mobile DevOps: Code Signing iOS Apps Automatically](https://hackernoon.com/mobile-devops-code-signing-ios-apps-automatically)

對於 Apple iOS 生態的 CICD pipeline 的設計每個團隊都不同，有些人會直接拿 Mac 直接跑，有些直接使用 SaaS 服務，而 Bitrise 是蠻不錯的平台，使用者體驗對開發人員都很好。本篇文章以大量的 gif 圖介紹 iOS code singing 的原理以及如何設定。