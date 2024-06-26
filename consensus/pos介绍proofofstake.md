**Proof-of-stake（POS)**是加密货币的区块链网络达到分布式共识的一种算法。在基于Pos的加密货币中，下一个区块的创建者是通过组合随机选择，财富值，或者是年龄等条件选择出来的。相反的是，基于Pow的加密货币(比如比特币)是通过破解hash谜题来决定区块的创建者。

## 多种区块选择机制

Proof-of-stake 必须有一种方法来定义区块链中的下一个有效的区块。如果仅仅基于账户余额会导致中心化的结果，因为如果单个最富有的成员会拥有永久的优势。相反，有几种不同的选择方法被设计出来。

### 随机区块选择

Nxt 和 BlackCoin 使用了随机的方式来预测下一个区块产生者，通过使用一个公式，这个公式选择用户股份hash值的最小值。argmin hash(stake)。 因为股份是公开的，所有的节点都可以计算出相同的值。

### 基于币龄选择

Peercoin 的 proof-of-stake 系统组合了随机选择和币龄的概念。币龄就是 币的数量乘以币的持有时间。 持有时间超过30天的币将有机会成为下一个区块的锻造者。 币龄更大的用户会有更大的机会来签署下一个区块。然而，一旦用来签署了一个区块，那么他的币龄会被清0。必须再等待30天才有可能签署下一个区块。同样，币龄最多只会累计到90天的上限就不会增加了，这是为了避免币龄非常大的用户对区块链具有绝对的作用。这个处理过程使得网络安全，而且逐渐的创造新的货币，而不会消耗非常大的计算资源。Peercoin的开发者申明在这样的网络上进行攻击会比Pow更加困难，因为没有中心化的矿池，而且获取51%的货币会比获取51%的算力更加困难。

## 优势

Proof of Work 依赖能源的消耗。 根据bitcoin矿场操作员声称，2014年没产生一个bitcoin的能源消耗达到了240kWh(相当于燃烧16加仑汽油，就碳的生产而言。)。而且能源的消费是非加密货币支付的。Proof of Stake的效率是Pow的几千倍。

区块生产者的激励方式同样不同。 在Pow模式下，区块的生产者可能并没有拥有任何的加密货币。矿工的意图是最大化的他们自己的收益，这样的不一致是否会降低货币的安全性或者提高系统的安全风险也是不清楚的。在Pos系统中，这些守护系统安全的人总是有用货币比较多的人

## 批评

一些作者认为pos不是分布式一致性协议的理想选项。其中的一个问题就是通常讲的"nothing at stake"问题，这个问题是说对于区块链的生产者来说，在两个分叉的点同时投票不会产生任何问题，而这样的可能会导致一致性难以解决。因为同时工作在多条链上面只会消耗很少的资源(根Pow不同),任何人都可以滥用这个特性，从而使得任何人都在不同的链上可以双花。

同样有很多尝试解决这个问题的办法：

- 以太坊建议使用Slasher协议允许用户惩罚作弊的人。如果有人尝试在多个不同的区块分支上创建区块，那么会被认为是作弊者。这个提案假设如果你想创建一个分叉你必须双重签名，如果你创建了一个分叉而又没有stake，那么你会被惩罚。然而Slasher从来没有被采用。以太坊开发者认为Pow是一个值得正视的问题。计划用一个不同的Pos协议CASPER来替代。
- Peercoin 采用了中心化的广播检查点的方法(使用开发者私钥签署). 区块链的重建的深度不能超过最新的检查点。折衷在于开发者是中心化的权利机构而且控制着区块链。
- Nxt 的协议仅仅允许最新的720个块重建。然而，这仅仅调整了问题。一个客户端可以跟随一个有721个区块的分叉，而不管这个分叉是不是最高的区块链，从而阻止了一致性。
- Proof of burn 和 proof of stake的混合协议。Proof of burn作为checkpoint节点存在，拥有最高的奖励，不包含交易，是最安全的。。。TODO
- pow和pos的混合。pos作为依赖pow的一个扩展，基于Proof of Activity提案，这个提案希望解决nothing-at-stake问题，使用pow矿工挖矿，而pos作为第二认证机制
- 