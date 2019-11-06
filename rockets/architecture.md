#  RocketMQ Architecture

![image-20191106225144768](https://tva1.sinaimg.cn/large/006y8mN6ly1g8opidy0q5j30kx08vdgz.jpg)

# 概览

Apache RocketMQ是一个具有低延迟、高性能和可靠性、万亿级容量和灵活可扩展性的分布式消息和流式平台。它由四部分组成：name server、broker、producer和consumer。它们中的每一个都可以水平扩展，而不会出现单点故障点，如上图所示。

**NameServer Cluster**

Name Server提供轻量级服务发现和路由。每个Name Server 记录完整的路由信息，提供相应的读写服务，支持快速的存储扩展。

**Broker Cluster**

Broker通过提供轻量级Tpoic和Queue机制来处理消息存储。它们支持Push-and-Pull模型，包含容错机制（2个或3个拷贝），并提供强大的峰值填充和按原始时间顺序累积数千亿条消息的能力。此外，broker还提供故障恢复、丰富的指标统计数据和警报机制，所有这些都是传统消息传递系统所缺少的。

**Producer Cluster**



**Consumer**



# NameServer



# Broker Server