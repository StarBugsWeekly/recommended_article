---
title: 第 158 期 Kubernetes 推薦文章
date: 2022-11-15
author: smalltown

layout: layouts/post.njk
tags: [Kubernetes]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## Kubernetes
### [Why you shouldn’t use Kubernetes](https://medium.paulbrissaud.fr/why-you-shouldnt-use-kubernetes-6004493259ae)

其實每過一段時間就會有人提出不一定需要使用 Kubernetes 的想法，這次看到這篇文所提出的論點為 1) 太複雜，因為一座嶄新的 K8s Cluster 其實是無法使用的，你必須要安裝適合自己的 Ingress Controller，或是 Storage Provider 給 Persistent Volume 使用，同理可證，為了監控，安全性或是其他的功能，你就需要再安裝更多的套件，這些額外安裝的東西都會需要有人熟悉且去維護它，除此之外也耗費了不少的 CPU 與 Memory 資源
<!-- summary -->

再來是太昂貴，因為 K8s Cluster 就跟其他的分散式系統一樣，會需要更多額外的資源來確保可用性與擴展性，如同前一點所述，你為了讓 K8s 變得堪用，你必須要安裝超多額外的東西，後面當然就是更多反應在帳單的雲端資源，除此之外應用服務的部屬方式也必須要改變，所以作者建議大家可以考慮看看先使用其他的 PaaS 或是 FaaS 平台來滿足需求，而不一定要在一開始就選擇使用 K8s 這麼龐大的解決方案

### [Selenium Grid Using K8S](https://medium.com/@mohdjeeshan007/selenium-grid-using-k8s-fe01e1f84456)

對於瀏覽器自動化測試有經驗的人，應該或多或少都會聽過 Selenium，而 Selenium Grid 是可以讓自動化測試平行運行在多台機器中的方式，這篇文章便是要分享如何將 Selenium Grid 整合到 K8s Cluster 中，讓自動化測試可以平行化第運行在 K8s Cluster 中，讓測試人員可以事半功倍！

### [How to validate Kubernetes YAML files](https://www.cncf.io/blog/2022/11/11/how-to-validate-kubernetes-yaml-files/)

活在當年的 IT 領域中應該很難避免去使用 YAML 檔案，甚至有人都會戲謔地稱自以為 YAML 工程師，而這篇發布到 Cloud Native 部落格的文章便想要跟大家分享如何去驗證準備要給 Kubernetes 使用的 YAML 檔案，文中提到驗證的方式可以從幾個面向來看，分別是結構，語義和安全性；而在驗證時的最佳準則就是確保 Shift Left 的精神落實，讓 DevOps 往 DevSecOps 邁進，對於此議題有興趣的朋友可以參閱內文