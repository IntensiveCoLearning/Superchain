---
timezone: UTC+8
---

# Marshal Orange

1. 自我介绍：五年Web3经历，某银行数据分析在职，Arweave中文社区贡献者、Web3Caff研究员。个人投研合集：https://button-balloon-2f0.notion.site/Marshal-Orange-s-Article-f938362d19094a3faedd6af5de0935f4?pvs=4
2. 你认为你会完成本次残酷学习吗？ 会
3. 你的联系方式（推荐 Telegram）：@dashuaiff

## Notes

<!-- Content_START -->

### 2025.03.31
总结：今天学习了 Superchain 的定义，并用 AI 总结了 Superchain 的特点。之前对 Rollup 进行过学习，但是对于 Optimism 生态的超级链没有概念，重点在于理解 OP Stack，容易陷入直觉陷阱，OP Stack 之前认为是默认基于 Optimism 的共识的，结果学习才发现是还是基于 ETH 共识的，Optimism 只是 OP Stack 生态中的一个链，等于用 OP Stack 框架可以在开发出一个 Optimistic Rollup 的 L2 链，而这样就知道之前了解的 Optimism 架构其实是 OP stack 了。

定义：超级链是 Optimism 生态系统内的 一组共享安全性、技术架构和治理机制的区块链。它建立在 OP Stack 之上，使多个 L2（Layer 2）区块链能够协同工作，同时共享 Optimism 生态的治理、流动性和技术优势。
特点：超级链的核心特点
1.基于 OP Stack
OP Stack 是一个模块化、开源的区块链架构，允许不同的 Rollup 使用相同的底层技术。超级链中的所有链都运行在 OP Stack 之上，可以使用相同的升级方案和安全机制。
2.共享安全性 & 统一治理
超级链中的不同 L2 链可以共用 Optimism 生态的安全机制（如 Security Council），降低单独部署 L2 的成本和风险。采用 Optimism Collective 的治理体系，确保链与链之间的规则和治理方式保持一致。（目前可能尚未实现）
3.促进跨链互操作性 & 生态整合
超级链中的链可以共享流动性，降低孤立性，提高资金利用率。通过统一的升级机制（Blockspace Charter），确保链之间的兼容性，减少生态碎片化。
4.允许定制化，但保持核心一致
虽然所有链都运行在 OP Stack 上，但它们可以根据自己的需求修改配置，例如：选择中心化 Sequencer 还是去中心化排序器。设定不同的治理方式（例如哪些地址可以升级合约）。Blockspace Charter 确保不同链之间仍有一定的标准化，避免过度分裂。

### 2025.04.01
学习了 Blockspace Charters 标准，包含 Criteria, Governing Policies, 和 Precommitments，是 Superchain 的一套技术治理框架，用于管理不同 OP Stack L2 的区块空间。它的作用是定义哪些 L2 符合特定的技术和治理标准，并提供相应的规则来指导 L2 的运行、治理和升级。
简单理解：Blockspace Charters 就是超级链的“区块空间管理规则”，类似于宪法 + 运营手册，确保不同 L2 之间的协调和安全性。
而如果要纳入超级链管理，这些 L2 必须使用特定版本的 OP Stack，需要满足特定的治理和安全要求必须接受升级管理规则，不过这样的君子协议也有好处，纳入管理后让超级链成为一个标准化的 L2 生态系统，让 L2 之间的治理和升级更加透明，确保 L2 更去中心化、安全性更高。但是貌似最大问题是现有治理机制不够细化，Optimism 目前的 Law of Chains 只是一个高层的指导原则，没有具体细节：它不会规定 L2 具体如何运作，它不会规定哪些 L2 可以升级，升级流程如何执行，治理缺乏技术细节，导致 L2 之间可能规则混乱。

### 2025.04.02
制作了一个 optimism 每日数据看板，了解目前 optimism 网络运行状况与通用指标，看板：https://flipsidecrypto.xyz/MarshalOrange/optimism-wang-luo-shu-ju-mei-ri-kan-ban-mgTsC3
对比22年23年刚接触optimism的时候，对于Layer2的概念才刚刚了解，当时 optimism 可谓是eth亲儿子链，现在距离巅峰时刻确实还有些差距，主要原因除了ETH大盘不好，其次是layer2严重吸血eth主网，各自为政，而OP stack开启了互操作性的口子，除此之外可能还需要寻找一个解决ETH流动性问题的方案，能让各个Layer2流动性也共享起来才是关键，而超级链目前初具规模，也是最先有希望实现此问题的。

### 2025.04.03
学习如何搭建一个超级链，因为性能问题可能我这边本地真实搭建不了，于是只想了解下流程。
首先申请加入 Superchain Registry，其次需要符合超级链标准，且支持跨 L2 互操作，集成 Optimism Bridge 或第三方跨链协议。
后续需要参与 Security Council 治理，超级链中的 L2 需要接受 Security Council 的管理，以确保升级安全。升级前需要投票通过。恶意行为可以导致 L2 被移除超级链（如 Sequencer 作恶）。
搭建一个链核心点是 OP Stack L2 Rollups 的性能，其吞吐量一般有这几个因素影响：Sequencer 处理速度（交易排序和执行能力）、L1 结算速率（打包 L2 数据到 L1 的时间）、DA 方案。这些可能还是受项目方自身实力的影响。

### 2025.04.04
今天学习一下超级链生态的Base链，目前Base链应该是超级链生态最强之链了，目前Base也称为ETH生态最活跃的Layer2
https://app.artemisanalytics.com/flows?tab=flow
背靠Coinbase，架构也是采用OP Stack，基本与Optimism技术架构一致，唯一不同的是，Base更为中心化，虽然大家都是中心化排序器，但是Base没有采用Fault Proof，而Base由于受监管约束，无发币计划，从去中心化社区角度也就没有共识.
在我看来，目前base能表现出如此高的活跃度和繁荣度，离不开政治风向和rwa赛道的推进，Coinbase跟特朗普团队关系不一般，而且已经拿到了证券代币化凭证，而rwa方面，Coinbase计划2025年推出“BASE Securities Hub”，让股票、债券这些传统资产也能变成代币交易，预计还能拉来千亿美元的机构资金。

### 2025.04.05


### 2025.04.06


### 2025.04.07

### 2025.04.08


### 2025.04.09
做了一个Base看板：https://flipsidecrypto.xyz/MarshalOrange/base-wang-luo-shu-ju-mei-ri-kan-ban-0_UaxK
数据对比Layer2确实属于碾压。


### 2025.04.10
学习下Velodrome，功能：
AMM（自动做市商）支持稳定币池和波动性资产池。
veNFT 锁仓投票机制（治理+奖励引导）。
Bribe 机制，用于激励投票。

官网：https://velodrome.finance
核心点是veVELO 用户可以将 $VELO 锁仓，获得 veVELO，锁仓时间越长，获得的 veVELO 越多（最长 4 年）。
veVELO 不能转移，但拥有投票权和激励权。投票激励机制：veVELO 持有者每周投票决定哪个流动性池能获得交易手续费奖励和 $VELO 通胀。
简单来说就是各项目方可以向投票者提供Bribe激励，而velodrome 用 ve(3,3) 机制把流动性提供者、治理者和项目方的激励整合到了一起。


### 2025.04.11
今天学习下Pendle，之前也了解过，因为参与过Pendle的再质押的活动，他的核心设计就是将收益资产拆分为两个部分，PT和YT
PT（Principal Token）本金代币	代表原始资产的价值（不计收益）
YT（Yield Token）	收益代币	代表未来某段时间的收益权利
到期后，PT 可以 1:1 兑换回原资产，YT 代表的收益会逐渐减少直至归零。

这里用AI举个例子：
用户将 stETH 存入 Pendle，获得：
PT-stETH（到期可赎回 stETH 本金）和 YT-stETH（未来一段时间内的质押收益）

用户可以选择：
1.保留两者，持有完整收益。
2.卖出 YT，提前锁定收益。
3.买入 YT，押注未来收益率上涨。
这种结构允许用户对收益进行套保、投机或收益优化。

而他的 AMM 机制并没有使用传统的 Uniswap v2/v3 式 AMM，而是设计了支持「到期资产」的专属 AMM，专门用于交易 PT 和 YT。

因为随着时间流逝，YT 的价值趋近于 0，价格曲线考虑了收益率、时间价值。然后 LP 提供 YT-Token/Stablecoin 的流动性。


### 2025.04.12
今天学习Redstone，我关注这个项目比较早，最开始是Arweave生态项目之一，主做预言机。
竞品分析：
Chainlink：主要针对 EVM、OG DeFi，主要采用 push model，通过桥接使用 CCIP 和昂贵的集成设置提供可靠数据，仅支持少量区块链；
Pyth：主要针对非 EVM，Perps 市场，主要采用 pull model，使用 Wormhole 作为跨链中继器，专注于数据推送质量；
RedStone：任意链、任意市场，提 push model 和 pull model，使用 eigenlayer AVS 进行具成本效益的链上验证，具有 wrapped BTC 资产的储备证明等。

预言机最重要是安全性，RedStone 可以通过使用 EigenLayer AVS 框架来验证价格反馈数据的准确性和有效性，从而实现更高效的 Gas 花费和可扩展性。
AVS 为 Actively Validated Service，是 Eigenlayer 生态里最重要的概念，AVS 简单地说就是一个需要抵押以验证"任务"的协议、服务或系统。AVS 服务本身承担了获取价格、上报价格的工作，同时 AVS 还对应着它的服务管理合约——Service Manager，该合约与 Eigenlayer 合约通信，其中包含与服务功能相关的状态，例如运行服务的操作者以及用于保护服务的押金数量。
传统的 oracle 价格推送模型通过从各种来源收集数据并通过 DDL（数据定义语言）和数据消费模块对其进行验证来工作。由于链上验证过程需要大量的 Gas 费，使其变得相当昂贵。借助 RedStone 的 AVS，RedStone 可以通过链下处理数据来提供高度优化的验证 Gas。
RedStone流程如下：AVS 运营商通过数据源模块获取市场价格和 TWAP 费率，验证其准确性，然后将验证结果反馈到链上。
由于大多数计算工作都是在链下执行的，同时通过 AVS 保持可信任和验证，相比竞品，RedStone 提供了成本更低的方案。

<!-- Content_END -->
