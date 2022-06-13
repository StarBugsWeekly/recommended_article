---
title: 第 136 期 DevOps 推薦文章
date: 2022-06-14
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Multi-cloud architecture: pros and cons](https://www.cncf.io/blog/2022/06/01/multi-cloud-architecture-pros-and-cons/)

相信大家不論在商業或者技術考量上有想過多雲供應商的架構，每個雲供應商有各自的優勢外，大家最常討論的不外乎還是減少服務停機時間。不過相對地，缺點可說是非常多，成本管理、資安和維運複雜度都會變得十分困難。有鑑於此，文章有列出哪些商業考量的點才需要考慮多雲架構。<!-- summary -->

### [Service Mesh Gets Boring and That’s a Good Thing](https://thenewstack.io/service-mesh-gets-boring-and-thats-a-good-thing/)

近期 Cloud Native Computing Foundation 調查指出 service mesh 對於組織在 microservice 和 Kubernetes 上至關重要，與此同時，寫這篇文章的 The New Stack 媒體也發現 service mesh 相關文章的讀者越來越少了，顯示出大家對這議題開始感到無聊，也代表 service mesh 漸漸變成主流的 solution。

### [Terraform 1.2 Improves Exception Handling and Updates to the CLI-driven Workflow](https://www.hashicorp.com/blog/terraform-1-2-improves-exception-handling-and-updates-to-the-cli-driven-workflow)

Terraform 1.2 新增了三大功能，Preconditions & Postconditions 的功能讓 Terraform module 可以驗證動態的 variable input，讓 module 可以更快地跳出 error 給使用者，甚至還有提供[教學](https://learn.hashicorp.com/tutorials/terraform/custom-conditions)。也新增了一些與 Terraform Cloud 相關的環境變數讓設定更彈性，另外 Terraform Cloud Run Tasks 正式 Generally Available，其功能為在 Terraform Cloud workflow 使用第三方的工具。
