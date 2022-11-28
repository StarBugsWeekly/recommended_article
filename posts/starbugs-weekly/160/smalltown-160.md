---
title: 第 160 期 Container 推薦文章
date: 2022-11-29
author: smalltown

layout: layouts/post.njk
tags: [Container]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## Container
### [7 Design Principals for Containers](https://hemantjain.medium.com/7-design-principals-for-containers-a6135ef13182)

此篇文章跟大家詳細介紹七個運行在 Cloud Native 所必須具備的 Container 設計準則，讀完突然發現這不就是使用 K8s 的最佳守則嗎？！

- Single Concern Principle: 一個 Container 只做一件事
- High Observability Principle: 讓 Container 滿足各種被監控的需求
- Life-Cycle Conformance Principle: 根據從平台收到的事件來管理 Container 的生命週期
- Image Immutability Principle: 一旦 Container Image 被建立，就不要再修改它
- Process Disposability Principle: 運行的 Container 要可以隨時被替換掉
- Self-Containment Principle: Container 自己本身要能夠獨立運行
- Runtime Confinement Principle: Container 要能夠建議自己執行所需要的資源

<!-- summary -->

### [9 Docker Extensions Every Developer Must Try](https://dev.to/docker/9-docker-extensions-every-developer-must-try-1no2)

還有在使用 Docker Desktop 的人，可以參考這篇文章，讓你知道 Docker Desktop 有哪些 Extension 可以讓開發更加方便

- Drone CI: 無縫與 Drone CI 整合
- Disk Usage: 分析硬碟被 Container 使用的狀況
- vcluster: 建立輕量化的虛擬 K8s 叢集
- Microcks: 整合 Microcks 在本地端 Mock 和測試 API
- OpenShift: 快速將本地端的 Image 部署到遠端的 OpenShift
- Portainer: 透過 Portainer 方便管理本地端的 Container
- Snyk: 協助開發者快速發現 Container Image 的安全問題
- JFrog Xray Scan: 協助開發者快速發現 Container Image 的安全問題
- okteto: 透過 okteto 快速建立本地端所需要的開發環境 

### [finch](https://github.com/runfinch/finch)

Finch 是一個新的開源專案，他提供一個 CLI Client 來建置，運行和發佈 Linux Container，而且可以很簡單的就安裝在 macOS 系統上，白話來說就是用來取代 Docker Desktop 的工具！看了範例使用起來跟 Docker CLI 有 87% 像，提供給大家一個 Docker Desktop 的替代方案。