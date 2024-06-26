# 2_ArbOS

## ArbOS: Arbitrum操作系统
ArbOS是L2上可信赖的『操作系统』，它负责将各个不受信任的合约分隔开，追踪并限制其资源使用，管理着从用户收集资金以给支付验证者的经济模型。在Arbitrum中，那些原本需要在昂贵的L1上进行的作业都在ArbOS中完成了，享受着L2的速度和低成本且无需信任。

在L2可信的软件中支持这些功能，而非将其构建在L1强加的以太坊式的架构上，对节省成本有重大意义。因为我们不在L1 EthBridge合约中管理这些资源，而是将其放入了计算和存储更便宜的L2上。在L2构建一套可信赖的操作系统同样对灵活性有重大意义，因为L2与L1强制的VM架构相比，其代码更容易迭代也更容易定制。

使用L2可信赖的操作系统确实需要有VM指令集的支持，例如，允许OS限制并追踪合约使用的资源。

客户端、EthBridge和ArbOS之间的通信信息格式，请见[ArbOS信息与log格式](../8_规范/ArbOS信息与log格式.md)。

←[1_聚合器](1_聚合器.md)
→[3_TxCall生命周期](3_TxCall生命周期.md)