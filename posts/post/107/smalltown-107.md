---
title: 第107期 DevOps 推薦文章
date: 2021-11-16
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

### [Announcing Grafana OnCall, the easiest way to do on-call management](https://grafana.com/blog/2021/11/09/announcing-grafana-oncall/)

在維運服務時，系統總是會有遇到問題需要求救的時候，設定一個彈性又有效的 On Call 輪值方式是相當重要的一件事情，很多既有的工具使用起來要嘛很麻煩，要嘛對於開發者來說很不友善，所以 Grafana 宣布推出簡單易用的 Grafana On Call 管理工具，用來降低管理 On Call 輪值所需要的功夫，目前在 Grafana Cloud 為 Beta 公測階段；Grafana On Call 主要是透過今年所收購 Amixr Inc 所開發出來的，而他主要有以下三個特點：

- 簡單建立跟管理 On-Call 時程
- 利用自動逐步升級 (Escalation)且彈性的引導方式 (Routing) 確保找到人協助系統問題
- 讓 On-Call 與 Incidnet 的狀態在同一個 UI 中顯現管理

### [Terraform Cloud Variable Sets Beta Now Available](https://www.hashicorp.com/blog/terraform-cloud-variable-sets-beta-now-available)

Terraform 的 Module 引用方式讓使用者可以一直重複利用既有的程式碼，而不需要重新造輪子，而現在 Terraform Cloud 針對變數也推出一樣的功能 - `variable sets`，他讓使用者可以重複使用 Terraform 所定義或是環境變數，而且不止是從 Root 到 Child Module，還可以橫跨某些 Workspaces 甚至是 Organization；自己發現 Terragrunt 也有類似的功能，看來 Terraform 這邊也跟上來了

### [Flux Security Audit has concluded](https://www.cncf.io/blog/2021/11/11/flux-security-audit-has-concluded/)

CNCF 最近對旗下 Incubation Project 進行 Security Audit，做完馬上發現一個 CVE: CVE-2021-41254，可以讓有心人士可以在 Multi-Tenant Flux 提權成 Cluster Admin (有使用 Flux 的人要記得升級)，而整個詳細的[稽核報告](https://fluxcd.io/FluxFinalReport-v1.1.pdf)已經被公開在網路上，找到將近 22 條涵括各種不同的 Risk Level 的問題，目前 43% 的 Issue 在 TODO 階段，21% WIP，36% 已經修完，詳細的進度可以參考 [GitHub Project](https://github.com/orgs/fluxcd/projects/5)，看起來 Flux 從另外一個面向投入資源，試圖跟其他的 GitOps 競爭工具做出差異化

