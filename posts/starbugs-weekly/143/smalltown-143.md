---
title: 第 143 期 Kubernetes 推薦文章
date: 2022-08-02
author: smalltown

layout: layouts/post.njk
tags: [Kubernetes]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Kubernetes

<!-- summary -->
### [ConfigMap Reloader — Automatically reload new data from ConfigMap/Secret to deployments](https://medium.com/linux-shots/configmap-secret-reloader-automatically-add-reload-data-from-configmap-secret-to-deployments-dc245e06b92c)

大家應該都會把一些應用服務要使用到的變數或是組態存放在 K8s Configmap 或是 Secret 中，而這些值一定會有需要修改的時候，不過當他們被修改時，其實滿多應用服務並不會自動去重新讀取新的值，所以這篇文章介紹了一個叫做 Reloader 的 K8s Controller，他會去監看這些 K8s Configmap 跟 Secret，當他們有改變時，他就會去幫忙 Rolling Upgrade 跟這些 Configmap 跟 Secret 有關的 Deployments, StatefulSets 或是 DaemonSets！
<!-- summary -->

### [kubebrain](https://github.com/kubewharf/kubebrain)

K8s 已經成為分散式應用服務調度的標準系統，不過他只能穩定的支援 5,000 個 Node，不管是在橫向或是縱向的擴張上，K8s 需要處理運行於其中應用服務狀態的資訊量會不斷的增加，最後造成擴展上的瓶頸，白話文就是說 Etcd 撐不住了，所以作者推出 KubeBrain 的開源專案，想要用來取代 Etcd，根據[實驗結果](https://github.com/kubewharf/kubebrain/blob/main/docs/benchmark.md)看起來讀跟寫的效能比 ETCD 來的好，但是刪除比較弱，需要再繼續最佳化，不過在 K8s Cluster 在實際運行時，需要刪除動作的情況筆記少

### [Kubernetes monitoring: leveraging 4 open-source toolsets](https://www.cncf.io/blog/2022/08/01/kubernetes-monitoring-leveraging-4-open-source-toolsets/)

使用 K8s 的人假如想要有一套綜合的監控工具該如何達成呢？CNCF 這邊建議可以使用 Prometheus 負責 Metrics and Alerting，Jaeger 負責 Tracing，OpenTelemetry 負責標準化的 Metrics, Logs, Traces，Thanos 負責多個叢集和長時間的 Metric 儲存
