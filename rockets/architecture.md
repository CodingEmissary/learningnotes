#  【译】RocketMQ Architecture

![image-20191106225144768](https://tva1.sinaimg.cn/large/006y8mN6ly1g8opidy0q5j30kx08vdgz.jpg)

> http://rocketmq.apache.org/docs/rmq-arc/

# 概览

Apache RocketMQ是一个具有低延迟、高性能和可靠性、万亿级容量和灵活可扩展性的分布式消息和流式(流式数据处理？？)平台。它由四部分组成：name server、broker、producer和consumer。如上图所示，它们中的每一个都可以水平扩展，而不会出现单点故障点。

**NameServer Cluster**

Name Server提供轻量级服务发现和路由。每个Name Server 记录完整的路由信息，提供相应的读写服务，支持快速的存储扩展。

**Broker Cluster**

Broker通过提供轻量级Tpoic和Queue机制来处理消息存储。它们支持push和pull模型，包含容错机制（2个或3个拷贝），并提供强大的峰值填充和随着时间积累的数千亿条消息的能力。此外，broker还提供故障恢复、丰富的指标统计数据和警报机制，所有这些都是传统消息传递所缺少的。

**Producer Cluster**

Producer支持分布式部署，分布式生产者通过多种负载平衡模式向broker集群发送消息。Producer支持快速失败和具有低延迟。

**Consumer**

Consumer支持Push和Pull模型的分布式部署。它还支持集群消费和消息广播。它提供了实时消息订阅机制，能够满足大多数用户的需求。RocketMQ的网站为感兴趣的用户提供了一个简单的快速入门指南。

# NameServer



# Broker Server