---
timezone: UTC+8
---

> 请在上边的 timezone 添加你的当地时区(UTC)，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区


# MRzzz-cyber

1. 自我介绍
2. 你认为你会完成本次残酷学习吗？当然，必须
3. @marcuszheng

## Notes

<!-- Content_START -->

### 2025.03.31

今天整理 Superchain 笔记的时候发现了一个有趣的新闻，USDT0 加入超级链生态网络了
![image](https://github.com/user-attachments/assets/6f95362b-44c2-4225-949d-bd29a2a8090e)
目前 USDT 可以在 Ink 和 Optimism 网络使用，泰达在某个网络发行稳定币一直都是生态比较活跃的象征之一，Ink 作为 Karken 支持的公链，这次联合 Optimism 推出基于 OP 和 Ink 网络的泰达币，对于未来 DeFi 稳定币生态来说，是一个非常好的布局
同时，USDT0 将很快受益于超级链互操作：区块最终性、零滑点和统一安全性。结果 = 为超级链上的 DeFi 奠定更坚实的基础（超级链始终占所有 L2 交易的 50% 以上）。


### 2025.04.01
今天学习的内容为超级链的技术宪章

超级链（Superchain）的核心概念
定义：超级链是由基于OP Stack构建的多个区块链组成的生态系统，旨在实现互操作性和共享治理。

当前挑战：

技术碎片化：不同链可能使用不同版本的OP Stack，或自定义配置（如参数、管理员角色等）。

用户体验：开发者和用户需要清晰理解不同区块空间（blockspace）的特性和保证。

治理复杂性：Optimism治理需针对不同链的配置和承诺制定决策。

2. 区块空间宪章（Blockspace Charter）
动机
补充《链法》（Law of Chains）：
《链法》是超级链的中立性框架（类似宪法），但缺乏协议细节的指导。区块空间宪章则类似“操作手册”，提供具体的技术实现规则。

三大核心组件
标准（Criteria）

版本：链必须使用特定版本的OP Stack（通过提交哈希/发布确定）。

配置：链的部署参数范围（如Chain ID、排序器（sequencer）或升级密钥的配置）。

偿付能力（Solvency）：确保链历史中无无效提款或输出，避免桥接抵押不足。

治理政策（Governing Policies）

定义参与区块空间的角色（如排序器、安全委员会）的行为规则和强制执行机制。

示例：

排序器的违规行为及移除流程。

治理投票和安全委员会签名的具体步骤。

需与《链法》的保护原则直接映射。

预承诺（Precommitments）

对未来协议升级的承诺，减少不确定性。

可能涉及：费用分配模型、角色分离、技术参数（如Gas限制）等。

形式：从具体代码变更到经济原则的抽象指导。

3. 宪章的落地与支持工具
超级链注册表（Superchain Registry）
作用：

作为超级链的公开索引，记录哪些链符合特定宪章的标准。

自动化测试套件验证链是否满足宪章条件。

分类系统：明确链所属的宪章（或未归类），区分超级链的不同“部分”。

分阶段 rollout（Beta阶段）
目的：在宪章正式批准前，通过“Beta注册表”让部分链先行接入，测试流程并收集反馈。

参与方：安全委员会、链治理者（Chain Governors）和服务商（Servicers）。

升级提案流程改进
关键变更：

提案需指定目标宪章，并链接到宪章的更新版本（GitHub PR）。

必须说明：

宪章变更的合理性。

如何保留旧宪章的所有预承诺。

目标：确保升级透明、可追溯，且符合Optimism Collective的长期愿景。



### 2025.04.02
今天学习了不同超级链之间的分类，目前整个 Optimism 对于超级链是有不同的支持意向的，首先是支持率先达到 Stage 1 阶段的链，然后像支持 Karken 交易所背景的 ink，支持交易类型的 unichain，然后日本 Ip 向的 Soneium，超级链支持的每条链都有各自的特点


### 2025.04.03
今天系统学习了 Velodrome, 这个 Optimism 上最大的 Dex，是如何运作的
Velodrome Finance 是一个建立在 Optimism 上的原生 DEX，主要是通过 VE 模型来提供高额的质押 Apy，从而吸引很多人进行质押，从而产生流动性和 TVL
这里其实我产生了一个疑问，VE模型以前就出现了很多，为什么 Velodrome 还能成功

在传统的 veToken 模型（如 Curve） 中，流动性提供者（LP）和治理参与者（veToken 持有者）的利益确实存在潜在的冲突，主要体现在以下几个方面：

1. 激励目标的分歧
流动性提供者（LP）的目标：

追求短期收益最大化，如交易手续费、流动性挖矿奖励（CRV 代币）。

倾向于选择高收益的池子，即使这些池子对协议长期发展未必有利（例如低效或低需求的池子）。

veToken 持有者的目标：

通过锁定 CRV 获得 veCRV，长期持有以获取协议治理权和额外收益（如交易费分成）。

希望引导流动性到 对协议长期价值有利的池子（例如稳定币核心池，提高协议整体交易量和收入）。

冲突点：
LP 可能更关注短期高收益的“挖提卖”行为，而 veCRV 持有者希望优化协议长期健康，两者的利益并不完全一致。

2. 代币释放与抛压问题
LP 的抛压：

Curve 的 LP 通过提供流动性获得 CRV 奖励，但这些 CRV 通常被立即卖出（短期行为），导致代币价格承压。

即使 LP 锁定 CRV 成为 veCRV 持有者，比例通常较低（因为锁定意味着流动性丧失）。

veCRV 持有者的抑制抛压：

veCRV 需要长期锁定 CRV（最长 4 年），减少了市场流通量，但这也限制了 LP 参与治理的动力（因为 LP 更倾向于灵活性）。

冲突点：
协议需要 CRV 释放来激励流动性，但过多的释放会导致抛压，损害 veCRV 持有者的利益（他们希望代币稀缺且增值）。

3. 投票权与流动性引导
Curve 的“投票权重”机制：

veCRV 持有者通过投票决定哪些池子能获得更高的 CRV 释放奖励（即“流动性引导”）。

理论上，veCRV 持有者应投票给对协议最有价值的池子（如高交易量、低滑点的池子）。

现实中的博弈：

许多 veCRV 持有者是 其他协议（如 Frax、Convex），他们可能为了自身利益（而非 Curve 协议的利益）投票。

例如，Frax 会引导 CRV 奖励到自己的 FRAX 稳定币池，即使该池对 Curve 整体贡献有限。

冲突点：
veCRV 持有者的投票可能偏离协议最优解，导致流动性分配低效，而 LP 仍会追逐高 CRV 释放的池子（无论是否合理）。

4. 收益分配的不平衡
交易手续费分配：

Curve 的 LP 获得 50% 的交易手续费，另外 50% 分配给 veCRV 持有者。

如果 veCRV 持有者主导投票降低某些池子的 CRV 奖励，LP 可能因收益下降而撤出流动性。

冲突点：
veCRV 持有者希望最大化协议收入（通过优化池子），但 LP 需要即时回报，两者对收益分配的优先级不同。

Velodrome 如何解决这些冲突？
Velodrome 在 ve 模型基础上进行了优化，减少 LP 和 veToken 持有者的对立：

贿赂机制（Bribes）：

项目方直接贿赂 veVELO 持有者，激励他们投票支持自己的池子，而 LP 无需依赖 CRV 释放，转向更直接的收益（贿赂+交易费）。

协议收入 100% 给 veVELO：

所有交易费和贿赂收益归 veVELO 持有者，绑定长期利益，避免短期 LP 的抛压问题。

L2 低门槛：

在 Optimism 上，LP 和投票者交互成本低，更多人愿意参与治理（而非仅巨鲸或协议）。



为什么能成为 Optimism 最大 DEX？
激励效率高：通过 ve 模型和贿赂机制，将 Optimism 的 OP 激励精准分配给深度流动性池。

生态协同：成为 Optimism 官方合作的流动性平台，吸引大量项目方入驻（如 Synthetix、Thales）。

用户粘性：长期锁定的 veVELO 持有者既是治理者也是协议收益的分享者，形成强社区共识。

潜在风险
过度依赖贿赂：若外部激励（如 OP 代币）减少，可能影响流动性。

跨链竞争：其他 L2（如 Arbitrum）的类似协议（如 Solidly 分叉）可能分流用户


### 2025.04.04
Velodrome 和 Aelodrome 有什么不同
Velodrome 和 Aerodrome 都是基于 Solidly ve(3,3) 模型 的 DEX，并且都部署在 Optimism 上，但它们由不同的团队运营，并且在代币经济、治理和发展方向上存在一些关键区别。以下是它们的详细对比：

1. 背景与团队

![image](https://github.com/user-attachments/assets/56badfa8-8ce2-4abb-9a90-5736f89fc0c2)


2. 代币经济学（veToken 模型）
![image](https://github.com/user-attachments/assets/45f9d1ab-1e83-4d63-b73b-033b8616a578)

3. 流动性与激励
![image](https://github.com/user-attachments/assets/1e368101-139f-4ee0-82d5-635f149a960c)
4. 治理与发展方向
![image](https://github.com/user-attachments/assets/85015b80-373a-42ba-bb87-65d5d56d4966)
5. 哪个更有优势？
![image](https://github.com/user-attachments/assets/9fc62efd-409f-4e27-a46b-74cfb64d4bf2)

总结
Velodrome 和 Aerodrome 的核心机制几乎相同，但 Aerodrome 凭借 Base 链的官方背景和 Coinbase 的资源，正在迅速抢占市场份额。未来，Aerodrome 可能成为 ve(3,3) 模型的主导者，而 Velodrome 需要依靠 Optimism 生态的持续支持来保持竞争力。

### 2025.04.05
Velodrome 的一些标志事件
Velodrome 作为 Optimism 生态的核心 DEX，自 2022 年上线以来获得了多项重要的生态资助和合作支持，同时也经历了多个标志性事件。以下是其关键历史节点和生态资助情况：

1. Optimism 官方资助（OP 代币激励）
2022 年 6 月：Velodrome 上线 Optimism，并成为首批获得 OP 代币激励 的协议之一。

通过 Optimism 的流动性挖矿计划，Velodrome 分发了大量 OP 代币奖励给流动性提供者（LP），迅速吸引 TVL 增长。

标志事件：2022 年 8 月，Velodrome 的 TVL 突破 2 亿美元，成为 Optimism 上最大的 DEX。

2023 年：持续获得 OP 激励，并在多轮 Optimism Governance Fund（治理基金） 中获批资金，用于协议开发和生态扩展。

2. 与 Synthetix 的战略合作
2022 年 7 月：Velodrome 与 Synthetix（Optimism 生态头部衍生品协议）达成深度合作。

Synthetix 将其流动性池（如 sUSD、SNX）迁移至 Velodrome，并为其提供额外激励。

标志事件：Synthetix 创始人 Kain Warwick 公开支持 Velodrome，称其为“Optimism 流动性中枢”。

3. Curve Wars 的延伸：Velodrome 成为 Optimism 的“贿赂中心”
2022-2023 年：Velodrome 继承了 Curve Wars 的玩法，成为 Optimism 生态的“贿赂市场”。

项目方（如 Thales、Beethoven X）通过 贿赂 veVELO 持有者 来引导流动性，推动自身代币池的激励权重。

标志事件：2023 年 Q1，Velodrome 单月贿赂金额突破 100 万美元，显示其治理代币的强需求。

4. 与 Optimism 生态项目的深度整合
2023 年：Velodrome 与多个 Optimism 原生协议合作，包括：

Thales（期权协议）：通过 veVELO 投票激励其流动性池。

Beethoven X（Balancer 分叉）：在 Velodrome 上建立稳定币池。

Kwenta（合成资产交易平台）：集成 Velodrome 流动性。

标志事件：2023 年 5 月，Velodrome 的稳定币交易量占比 Optimism 生态 超 60%。

5. Velodrome V2 升级（2023 年 3 月）
关键改进：

引入 “自动复合贿赂收益” 功能，提升 veVELO 持有者的收益效率。

优化 Gas 费用，降低用户参与成本。

标志事件：升级后 TVL 单月增长 40%，突破 3 亿美元。

6. 应对 Aerodrome 的竞争（2023 年 8 月后）
2023 年 8 月：Coinbase 支持的 Aerodrome 上线 Base 链，并随后扩展至 Optimism，直接挑战 Velodrome。

Velodrome 通过 提高贿赂奖励 和 优化代币释放 应对竞争。

标志事件：2024 年 Q1，Velodrome 在 Optimism 上仍保持 ~50% 的稳定币交易份额，但 TVL 被 Aerodrome 部分分流。

7. 其他生态资助与里程碑
Gitcoin 资助：Velodrome 团队曾获得 Gitcoin 社区捐赠，用于开发工具和文档。

Chainlink 预言机支持：2023 年集成 Chainlink 数据源，提升价格喂价安全性。

跨链流动性尝试：2024 年探索与其他 L2（如 Arbitrum）的桥接合作，但尚未大规模推进。

总结：Velodrome 的关键成功因素
Optimism 官方支持：早期 OP 代币激励使其快速崛起。

ve(3,3) 模型优化：贿赂机制和资本效率高于传统 DEX。

生态整合：与 Synthetix、Thales 等头部协议合作，成为流动性枢纽。

应对竞争：在 Aerodrome 的冲击下仍保持 Optimism 的重要地位。


### 2025.04.06
1. Optimism 生态的流动性中心

Velodrome 仍是 Optimism 上最大的 ve(3,3) DEX，但 Aerodrome 正在 Optimism 上扩张，竞争加剧。

核心优势：

深度整合 Optimism 生态（如 Synthetix、Kwenta）。

稳定币交易对（如 USDC/DAI）仍占据主导地位。

2. 与 Aerodrome 的竞争
Aerodrome（Base 链官方 DEX） 在 2023 年 8 月上线后，TVL 迅速增长，并扩展到 Optimism，分流了部分 Velodrome 的流动性。

Velodrome 的应对策略：

提高 贿赂激励（如项目方给 veVELO 持有者的额外奖励）。

优化 交易手续费分配（100% 给 veVELO 持有者）。

3. 代币经济与治理
（1）VELO 代币现状
流通市值：~5000 万美元

通胀控制：通过 veVELO 锁定机制（1-4 年）减少抛压。

主要用途：

流动性挖矿奖励（LP 获得 VELO）。

治理投票（锁定 VELO 获得 veVELO）。

（2）veVELO 持有者收益
收入来源：

交易手续费（0.02%-0.05%）。

贿赂收入（项目方支付激励）。

年化收益率（APR）：约 10%-30%（取决于市场活跃度）。

4. 最新动态与未来计划
（1）近期重要事件
2024 年 Q2：

与 Mode Network（OP Stack L2） 合作，探索跨链流动性。

集成 Chainlink 低延迟预言机，提升交易安全性。

2024 年 Q3 路线图：

优化 跨链交易体验（可能支持 Arbitrum）。

推出 新的激励计划 应对 Aerodrome 竞争。

（2）潜在挑战
Aerodrome 的强势增长：Coinbase 支持的 Base 链生态更具资源优势。

Optimism 生态增长放缓：相比 Base 和 Blast，Optimism 近期新项目较少。

5. 结论：Velodrome 的未来展望
✅ 优势：

仍是 Optimism 流动性核心枢纽，尤其适合稳定币交易。

ve(3,3) 模型成熟，贿赂机制仍具吸引力。

⚠️ 风险：

Aerodrome 的多链扩张 可能进一步挤压市场份额。

VELO 代币价格疲软，需更多用例支撑价值。

未来关键点：

能否在 Optimism 生态 保持不可替代性？

是否会扩展至 其他 L2（如 Arbitrum、Mode） 以寻求新增长？

目前，Velodrome 仍是 Optimism 上最重要的 DEX 之一，但需持续创新以应对竞争。

### 2025.04.07

<!-- Content_END -->
