---
timezone: UTC+8
---

> 请在上边的 timezone 添加你的当地时区(UTC)，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区


# 你的名字 stephanie

1. 自我介绍
上海大学通信工程专业，对区块链感兴趣。
2. 你认为你会完成本次残酷学习吗？
会
3. 你的联系方式（推荐 Telegram）
7259563054（telegram）
J-79756537（wx）

## Notes

<!-- Content_START -->

### 2025.03.31
学习过程中不断产生疑问，笔记大多是chat gpt对疑问的回答
Season 6 介绍
1. What is a Blockspace Charter?

At a high level, a Blockspace Charter consists of three primary components: Criteria, Governing Policies, and Precommitments.

It provides a technical-focused governing document for the Superchain and defines the specific implementation details for different types of Superchain blockspace, similar to an "Operating Manual."

2. Why introduce a Blockspace Charter?

The Superchain is quickly blossoming into a robust ecosystem of OP Stack-based chains. However, these chains are not all technically equivalent:

Different chains may use different versions of the OP Stack—some projects have made modifications to the stack, and others are on outdated versions of it.

Even within chains that are on the same version, some may be configured differently — deployed with different values for various parameters, admin roles, and so on.

There is a need for:

Users and developers to easily understand what blockspace has which properties and guarantees.

Optimism Governance to understand how to make decisions about these different forms of blockspace, which may make different commitments and have different control structures.

The Law of Chains is a neutrality framework designed to provide a guiding light for the Superchain and its stakeholders to make decisions and uphold protections. However, the Law of Chains is intentionally agnostic to any specific details of the protocol, which means it can fail to provide clear guidance at the required granularity.

Blockspace Charters will act as the equivalent to the Operating Manual, providing the specific implementation details for different types of Superchain blockspace.

3. What does a Blockspace Charter include?

Criteria:

Version: The version of the OP Stack that the chain is using, as determined by commit-hash/release.

Configuration: The accepted range of parameterizations for the software in the OP Chain’s deployment, including both static (e.g., Chain ID) and dynamic variables (e.g., sequencer or upgrade keys).

Solvency: Ensuring that a chain’s history does not include any invalid withdrawals or invalid outputs that could cause the bridge to be undercollateralized.

Governing Policies:

Specific rules, procedures, and principles that stakeholders participating in the charter’s blockspace must follow.

Example: If a charter’s blockspace criteria require that upgrade keys be held by the Security Council, and allow the chain’s sequencer to be configured to be anybody, the governing policies could define:

The required behavior of the sequencer, which, if violated, would be grounds for removal.

The governance process (e.g., proposal type) by which governance could vote to remove the sequencer.

The signing procedure which would be subsequently taken by the Security Council to remove the offending sequencer.

The governing policies align with the Law of Chains principles to ensure protections for the charter’s blockspace.

Precommitments:

A commitment mechanism, outlining anticipated changes (or consistency) for future upgrades to the charter.

Precommitments help provide stakeholders with a clear understanding of the long-term vision and stability of the governance framework.

They can address critical aspects like fee split models, role separations, and technical parameters such as gas limits and fee margins.

4. How will Blockspace Charters be rolled out?

Superchain Registry:

The Superchain Registry will play a crucial role by serving as an accessible index of what chains are part of the Superchain.

It ensures that chains meet the criteria outlined in their respective Blockspace Charter before being added, ensuring consistency and security across the Superchain.

It is a public index that documents the configuration values of each chain and categorizes them under the appropriate charter.

Incremental Rollout (Beta Registry):

Some initial chains will be onboarded to the Phase 1 Security Council and Superchain Registry to test the process before the Standard Rollup Charter is ratified and scaled.

This phase is designed to help the Security Council become familiar with the end-to-end process and resolve any frictions before full implementation.

Improved Upgrade Proposal Process:

Upgrade proposals will correspond to specific Blockspace Charters.

Upgrade proposals must link to a pull request for an updated charter and provide justifications for any changes not covered in other sections.

The Impact Summary must demonstrate that all precommitments in the previous charter are preserved by the upgrade.

This ensures that the upgrade process is transparent, accountable, and stakeholder-focused, allowing the Collective to rigorously consider the impact on stakeholders.

共识机制
1. 工作量证明（Proof of Work，PoW）
工作量证明是最早用于比特币的共识机制，它的基本思想是通过计算机解决复杂的数学问题来验证交易和生成新区块。这个过程被称为“挖矿”。

原理：

矿工（节点）需要通过不断尝试不同的随机数（Nonce）来找到一个满足特定条件的哈希值（即区块的哈希）。

一旦矿工找到符合条件的哈希值，他们就会将新区块广播到网络上。

其他矿工验证新区块的有效性，确保其符合规则。如果区块合法，它就被添加到区块链中。

优点：

安全性高：因为要生成一个新区块，需要大量计算资源，所以恶意攻击者要改变区块链中的数据非常困难。

去中心化：任何人都可以参与矿工网络，只要有计算能力。

缺点：

能耗高：PoW机制要求矿工进行大量的计算，导致能源消耗巨大。

扩展性差：PoW机制的交易处理速度相对较慢，网络上的吞吐量有限。

集中化风险：虽然理论上任何人都可以参与挖矿，但实际中大规模矿池的存在导致网络算力集中，可能影响去中心化特性。

应用实例：比特币（Bitcoin）、以太坊（Ethereum，已逐步转向PoS）。

2. 权益证明（Proof of Stake，PoS）
权益证明是一种相较于PoW更加节能的共识机制。在PoS中，验证新区块的权力不再由计算能力来决定，而是由节点持有的代币数量和持有时间来决定。

原理：

节点需要持有一定数量的数字货币（例如以太坊的ETH）才能参与区块的验证。持有的代币越多，验证区块的概率越高。

节点会随机被选择为区块验证者（生成新区块），如果选中，节点需要验证交易并将新区块添加到区块链中。

验证者也需要对其行为负责，如果他们不诚实（如试图验证无效交易），他们将失去部分或全部抵押的代币。

优点：

低能耗：与PoW相比，PoS不需要大量的计算资源，因此消耗的能源较少。

高效：交易验证速度较快，能够处理更多的交易。

去中心化：理论上PoS比PoW更能防止矿池集中化，提供了更多去中心化的机会。

缺点：

“富者愈富”问题：持有更多代币的用户有更大的机会获得新区块验证权，这可能导致财富集中，造成贫富差距。

安全性问题：PoS系统可能受到“长时间攻击”的威胁，即攻击者通过拥有大量代币来控制网络的验证权。

应用实例：以太坊（Ethereum，已逐步转向PoS）、Cardano、Polkadot。

3. 委托权益证明（Delegated Proof of Stake，DPoS）
委托权益证明（DPoS）是对PoS的扩展，旨在提高网络的效率和处理能力。DPoS通过选举产生一些“代表”节点，来承担新区块的验证和网络治理的任务。

原理：

持币人将自己的代币委托给代表节点，这些代表节点将负责验证交易和生成新区块。

节点通过投票选举代表，这些代表被选中后就能进行区块验证工作。

每个用户的投票权重通常与他们持有的代币数量相关。

优点：

高效性：通过选举代表节点，可以提高验证速度和区块生成速度，处理更多的交易。

低能耗：与PoW相比，DPoS节省了大量的计算资源。

去中心化治理：代币持有者可以投票选举代表，参与治理。

缺点：

集中化风险：由于少数代表节点拥有很大的权力，可能会导致治理的集中化。

代表节点的选择问题：如果代表节点行为不当，可能导致网络不稳定或不公平。

应用实例：EOS、TRON、BitShares。

4. 拜占庭容错机制（Byzantine Fault Tolerance，BFT）
拜占庭容错机制是一种用于解决分布式网络中“拜占庭将军问题”的共识机制。它的目的是确保即使在网络中部分节点发生故障或恶意行为时，系统仍能正确工作。

原理：

节点之间通过通信达成一致意见，确保只有一部分节点出现问题（例如故障或攻击）时，网络仍能正常运作。

通过投票和消息传递机制来达成共识，确保所有诚实节点最终都同意一个相同的交易记录。

优点：

高容错性：能够容忍一定数量的节点出现故障或不诚实行为。

高效率：不需要大量的计算资源，通常能够提供更高的交易吞吐量。

缺点：

网络规模限制：BFT在节点数增加时，网络的效率可能会下降，适用于节点较少的区块链系统。

安全性问题：如果恶意节点超过一定比例（例如2/3），共识机制将失败。

应用实例：Hyperledger Fabric、Tendermint、Zilliqa。

5. 其他共识机制
除了上述主要的共识机制，还有一些其他的共识机制，它们各自有不同的特点和应用场景：

Proof of Authority（PoA）：通过信誉好的节点来进行验证，这些节点通常是经过身份认证的。适用于权限链或私有链。

Proof of Space（PoSpace）：基于存储空间的证明机制，节点通过提供存储空间参与共识，类似于硬盘挖矿。


区块链基本常识
1. 区块链的基本概念
区块（Block）：区块链中的每个“区块”包含一组经过验证的交易或数据。在区块中，除了交易数据外，还会包含：

时间戳：表示区块被创建的时间。

前一个区块的哈希值：确保区块链的连续性和链接性。

随机数（Nonce）：用于工作量证明机制。

区块的哈希值：每个区块有一个唯一的标识符，用于确保数据完整性。

链（Chain）：区块通过哈希值链接在一起，形成一个不可更改的链条。因此，任何对已确认区块的更改都会影响到后续的所有区块，从而使得篡改变得极其困难。

去中心化（Decentralization）：区块链没有中央控制点，而是由多个节点共同维护账本。每个节点都持有一个区块链副本，并通过共识机制来验证交易和数据。

2. 工作原理
分布式账本：区块链是一个分布式数据库，所有的交易和数据都存储在多个节点上，没有单一的存储位置。这意味着即使某些节点故障，数据依然可以通过其他节点进行恢复。

共识机制：为了确保所有节点的数据一致性，区块链网络采用共识机制。常见的共识机制包括：

工作量证明（Proof of Work，PoW）：矿工需要解决复杂的数学问题来获得新区块的创建权。比特币网络使用的就是这一机制。

权益证明（Proof of Stake，PoS）：基于节点持有的代币数量和时间来决定谁有权创建新区块。以太坊逐步转向PoS机制。

委托权益证明（DPoS）：通过投票选出少数的验证节点来进行区块的验证和生成。

加密技术：区块链通过加密技术来确保数据的安全性和隐私性。每个用户都有一对公钥和私钥：

公钥：用于接收交易或数据。

私钥：用于签署交易，确保交易的合法性和安全性。

3. 区块链的特点
去中心化：传统的系统通常依赖于中央机构（例如银行或政府）来管理数据和交易，而区块链通过去中心化的方式使得任何节点都有平等的权利，避免了单点故障。

透明性：区块链上的所有交易都可以公开查看，任何人都可以验证和审计区块链上的交易记录。虽然交易信息是公开的，但通过加密技术可以保护用户的隐私。

不可篡改性：一旦数据被记录到区块链上，就无法修改或删除。因为区块链是链式结构，每个区块都包含上一个区块的哈希值，篡改一个区块的数据需要重新计算所有后续区块的哈希，几乎不可能做到。

安全性：区块链的设计使得它对攻击非常有韧性。通过加密和分布式账本的技术，区块链防止了数据被恶意修改或伪造。

4. 区块链的应用
加密货币：区块链最初的应用是加密货币，如比特币和以太坊。它们利用区块链技术来创建去中心化的数字货币，允许用户在没有中央机构的情况下进行交易。

智能合约：以太坊等平台允许创建智能合约。智能合约是一种自执行的合约，其中的条款被写入代码中并自动执行。这种技术可以用于自动化金融交易、供应链管理等。

供应链管理：区块链可以用来追踪商品从生产到销售的全过程，确保供应链的透明度和真实性，防止假冒伪劣商品的流通。

身份认证：区块链可以用于数字身份验证，提供更加安全和隐私保护的身份认证方法，减少身份盗用的风险。

金融服务：区块链在银行、支付、借贷等领域的应用正在不断增加。它可以降低交易成本，提高效率，并为跨境支付提供便捷的解决方案。

5. 区块链的挑战
扩展性：随着区块链网络的用户增加，交易量激增，区块链可能面临性能瓶颈。提高交易处理速度和降低交易费用是目前的一个挑战。

能耗问题：像比特币这样的工作量证明机制需要大量的计算能力，导致高能耗，这在环保方面引起了争议。

隐私问题：虽然区块链提供了透明性和不可篡改性，但公开的交易记录可能导致用户隐私泄露。虽然可以通过加密来保护隐私，但仍然是一个挑战。

监管问题：由于区块链技术去中心化，许多国家和地区对其监管仍在探索中，可能面临法律合规性的问题。





### 2025.04.01
问题一：6个季度的进化，主要面对的问题

在 Optimism 网络中，季度（Seasons） 是通过 Optimism Collective 来组织治理和激励的重要机制。每个季度（Season）都有不同的重点和目标，以推动 Optimism 生态系统的长期增长与发展。以下是 Optimism 在过去六个季度（Season 1 到 Season 6）的详细介绍，以及每个季度之间的横向对比，阐述其主要区别和更新。

Season 1 - 启动与基础设施建设
时间：2021 年 6 月 以太坊主网启动 Optimism 主网

重点：优化以太坊的扩展性

目标：

推出 Optimism 主网，支持以太坊 dApp 迁移。

启动 OP 代币 分发计划和治理机制的初步框架。

主要关注以太坊的扩展性和低费用交易，作为 Layer 2 的解决方案，Optimism 使用 Optimistic Rollups 技术来提高交易吞吐量。

主要特点：

初步实现了 Layer 2 扩展解决方案，解决了以太坊交易高费用和低吞吐量问题。

代币 OP 的首次发行和社区的初步治理设计。

Season 2 - 生态系统资助与开发者激励
时间：2021 年下半年

重点：开发者激励和生态系统增长

目标：

启动 生态系统基金，支持在 Optimism 上开发的应用。

通过 Retroactive Public Goods Funding（回溯性公共产品资助） 机制，支持为生态系统提供公共产品的开发者。

优化和推广 开发者工具，鼓励开发者移植和构建 dApp。

主要特点：

资金支持：为 Optimism 上的开发者提供资金，支持更多的去中心化应用（dApps）和智能合约的开发。

回溯资助：引入 RetroPGF 机制，奖励在过去对生态系统有贡献的开发者和项目。

Season 3 - 去中心化与治理升级
时间：2022 年初

重点：去中心化治理，增加用户和开发者参与

目标：

引入去中心化治理机制，**治理基金（Governance Fund）**用于资助与 Optimism 生态系统相关的各类项目。

增强治理结构，例如通过 Optimism Collective 完成关键决策和政策制定。

启动 Optimism Collective 的 Collective Governance，鼓励社区成员参与决策。

主要特点：

通过 Optimism Collective 进行 去中心化治理，进一步推动生态系统的自治。

完成了初步的去中心化治理架构，优化了资源的分配和决策机制。

Season 4 - 扩展性和跨链互操作性
时间：2022 年中期

重点：扩展性和跨链互操作性

目标：

强化 Optimism 的 扩展性，包括提升交易吞吐量、降低交易费用。

引入跨链互操作性功能，确保 Optimism 网络能够与其他区块链平台（如以太坊、Polkadot 等）兼容。

完善 生态系统奖励机制，进一步激励开发者和用户参与生态系统。

主要特点：

实现了 跨链互操作性，使 Optimism 可以与其他链无缝对接。

优化了扩展性，提升了整个网络的性能。

开始引入更多的 Layer 2 解决方案，如 Arbitrum 和 zkSync，推动了更大的生态合作。

Season 5 - 完善治理与生态系统激励
时间：2023 年初

重点：更加完善的治理机制与激励措施

目标：

完善治理框架，引入 社区奖励 和 创新激励机制，增强社区成员的参与度。

增强治理透明性，通过 Grants Council 和其他治理机构，进一步提升 Optimism Collective 的自治性。

推动 公私合营，鼓励项目和企业与 Optimism 生态系统合作。

主要特点：

加强 治理透明度，所有的决策和资金分配过程都更加公开。

社区驱动的奖励机制，加强对开发者和社区成员的激励。

更加强调 创新与合作，推动与其他平台、企业的联合。

Season 6 - 支持超级链与跨链开发者
时间：2024 年

重点：支持超级链、进一步扩大开发者生态

目标：

支持 超级链（Superchain） 生态系统，多个 OP 链之间进行协作，并鼓励不同链之间的资源共享。

推动 Layer 2 生态发展，扩大 开发者支持计划，使开发者能够更加高效地构建和部署应用。

引入 跨链激励机制，促进各个 OP 链之间的资源分配和合作。

主要特点：

支持超级链，通过多个 OP 链协同工作，实现更好的扩展性和互操作性。

强调 跨链互操作性，并为开发者提供更多的支持和资源。

增强了 开发者激励机制，推动开发者跨链构建更加丰富的 dApp 生态。

问题二：layer1和layer2是什么，有什么联系
Layer 1 和 Layer 2 简介
在区块链技术中，Layer 1 和 Layer 2 是两个关键的概念，它们分别指代了不同的区块链架构层级。它们主要的区别在于处理交易和扩展能力上。

1. Layer 1：基础区块链层
Layer 1 是指区块链的基础层，即区块链的核心协议和网络结构，负责所有的交易验证和数据存储。它包括了区块链的核心共识机制、区块生成、交易确认和网络安全等基础功能。

特点：
去中心化：Layer 1 通常是去中心化的，这意味着网络中的所有节点都有权参与交易的验证和共识的达成。

共识机制：Layer 1 区块链通常会使用某种共识机制来确保区块链的安全性和一致性。常见的共识机制有：

工作量证明（PoW，Proof of Work）：如比特币（Bitcoin）。

权益证明（PoS，Proof of Stake）：如以太坊（Ethereum，当前和未来将逐步转向 PoS）。

拜占庭容错（BFT）：如 Cosmos 和 Tendermint。

链上的操作：所有的交易数据和智能合约都在 Layer 1 上进行处理和记录。所有的事务、状态变更和智能合约执行都是在主链上进行的。

典型的 Layer 1 区块链：
比特币（Bitcoin）：使用 PoW 共识机制，作为第一个区块链，它主要用于存储和转移比特币（BTC）。

以太坊（Ethereum）：一个支持智能合约的平台，最初基于 PoW（后将转向 PoS），它是构建去中心化应用（dApps）的基础设施。

Solana：一个高性能区块链，使用 Proof of History（PoH）和 Proof of Stake（PoS）结合的机制，能够提供高速和低费用的交易。

Cardano：采用 Ouroboros PoS 共识机制的智能合约平台，注重可持续性和安全性。

挑战：
扩展性问题：Layer 1 区块链通常会面临吞吐量（TPS，Transaction Per Second）的限制。在用户量增加时，交易确认时间会变长，交易费用也会增加。

交易费用：随着区块链的网络负载增加，交易费用可能会大幅上升，特别是在高需求的网络中，如以太坊。

2. Layer 2：扩展和优化层
Layer 2 是构建在 Layer 1 之上的附加层，旨在解决 Layer 1 的扩展性问题。通过将某些计算和数据存储转移到 Layer 2，交易处理速度得以提升，同时减少了 Layer 1 链上的负担。Layer 2 提供了更高效的处理方式，确保区块链能够处理更多的交易和更低的交易费用。

特点：
扩展性：Layer 2 解决了 Layer 1 上的吞吐量瓶颈。它通过处理交易、智能合约等操作，减少了主链的负担，从而提高了系统的扩展性。

低成本：通过将大部分交易处理移到 Layer 2，减少了交易的成本。用户可以享受到更低的手续费和更快的确认时间。

保持去中心化：尽管 Layer 2 增加了某些额外的处理层，但它们通常依赖于 Layer 1 的安全性和去中心化特性。Layer 2 网络的安全性和数据一致性最终会与 Layer 1 保持一致。

Layer 2 解决方案的类型：
状态通道（State Channels）：

状态通道允许用户在不直接与区块链交互的情况下进行多次交易。这些交易仅在通道关闭时才会被提交到主链。最著名的例子是 闪电网络（Lightning Network），它是比特币的 Layer 2 解决方案，允许用户在链下进行快速交易。

Rollups（汇总链）：

Rollup 将大量的交易数据“汇总”并提交到主链。通过批量处理和压缩交易数据，Rollup 提高了吞吐量和效率。Optimistic Rollups 和 ZK-Rollups 是两种主要类型：

Optimistic Rollups：假定交易是有效的，除非有人提出异议。以 Optimism 和 Arbitrum 为代表。

ZK-Rollups：使用零知识证明（Zero-Knowledge Proofs）来确保链上数据的有效性。以 zkSync 和 Loopring 为代表。

Plasma：

Plasma 是一个分层的解决方案，允许将大量的交易处理从主链上移至子链。通过该方法，可以降低主链的交易负担，同时仍然保持数据和资产的安全性。Plasma 设计用于解决以太坊的可扩展性问题，但其实现较为复杂。

Validium：

Validium 与 ZK-Rollups 类似，但数据存储不一定保存在主链上。它通过加速交易速度和降低成本来提高系统性能。

典型的 Layer 2 项目：
Optimism：基于 Optimistic Rollups 技术，旨在提高以太坊的可扩展性，降低交易费用。

Arbitrum：另一个基于 Optimistic Rollups 的 Layer 2 扩展方案，专注于提升以太坊的吞吐量。

zkSync：基于 ZK-Rollups 技术，致力于提供高效且低成本的交易，目标是为以太坊提供可扩展性。

Polygon (MATIC)：一个多链 Layer 2 解决方案，支持多个区块链的交互，并致力于提升以太坊的可扩展性。

挑战：
复杂性：Layer 2 解决方案通常比 Layer 1 更复杂，可能涉及更高的技术门槛和部署难度。

安全性：虽然 Layer 2 网络通过与 Layer 1 的互操作性来增强安全性，但仍然可能面临某些安全性问题，尤其是在没有足够去中心化的情况下。
问题3：op在web3中的地位，与op同级的概念
OP 在 Web3 中的地位
Optimism (OP) 是一个区块链扩展解决方案，属于 Web3 生态系统中的 Layer 2 解决方案之一。它的主要目的是提高以太坊的扩展性，通过将交易处理移到第二层网络（Layer 2），从而提高交易速度和降低费用。Optimism 采用了乐观 Rollup 技术，它是一种将大量交易数据打包并提交到以太坊主链上的方法，这样可以大幅度减少以太坊主链的负担。

Optimism 主要解决以太坊的可扩展性问题，使得 Web3 应用（尤其是去中心化金融 DeFi）能够在以太坊上高效运行。因此，Optimism 在 Web3 中的位置是作为一种技术基础设施，帮助 Web3 生态实现更高效、更便捷的操作。

与 OP 同级的概念
与 OP 类似的 Web3 生态系统中的项目，主要是其他 Layer 2 扩容解决方案，它们都致力于改善区块链的扩展性和交易效率。以下是与 OP 类似的项目：

Arbitrum：

Arbitrum 也是一个 Layer 2 解决方案，采用类似于 Optimism 的技术（Optimistic Rollups）。它同样旨在通过减轻以太坊主链的负担，提供快速且低成本的交易处理。

Polygon (MATIC)：

Polygon 是另一个广泛使用的 Layer 2 扩展网络，它不仅支持以太坊，还支持多种区块链。Polygon 提供了一系列工具和协议，帮助开发者轻松构建去中心化应用。

zkSync：

zkSync 是一个基于零知识证明（ZK-Rollups）技术的 Layer 2 扩展解决方案。与 Optimism 和 Arbitrum 的乐观 Rollups 技术不同，zkSync 使用 ZK-Rollups 使得以太坊的扩展性更高，且交易更加安全。

Loopring：

Loopring 也是一个基于 ZK-Rollups 的去中心化交易平台，致力于提供快速且低成本的去中心化交易服务。它通过 zkRollups 提高交易效率并降低费用。

Immutable X：

Immutable X 是一个专为 NFT 设计的 Layer 2 扩展解决方案，基于 ZK-Rollups 提供高效且无 gas 费用的 NFT 交易。


### 2025.04.02
### 2025.04.03

<!-- Content_END -->
