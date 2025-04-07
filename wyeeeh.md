---
timezone: UTC+8
---


# Ye

1. 自我介绍
    清华-南加大 Communication Data Science 25'硕士在读，链上数据分析2年经验，Dune [@wyeeeh](https://dune.com/wyeeeh)，X [@wyeeeeh](https://x.com/wyeeeh)，Optimism NumbaNERDs 分析师，入选Optimism RetroPGF Round 3 & Round 6 头部贡献者。

2. 你认为你会完成本次残酷学习吗？
   有激励就有野心，之前完成过Sixdegree Lab和BuidlerDAO发起的Dune Analytics共学计划，DeFiHackLabs发起的[Solidity残酷共学计划](https://basescan.org/token/0xb05d424943350adfadec4731cd54f12cc45e8c5c?a=0x7935D3A4beC9Dfe119bA2f7a1e977C406687Ac9C)，以及LXDAO发起的[第一期Optimism残酷共学计划](https://github.com/wyeeeh/Optimism)，有了这些积累，我认为我会完成这次学习。

3. 你的联系方式
   Telegram: [@wyeeeh](https://t.me/wyeeeh)


## Notes

<!-- Content_START -->

### 2025.03.31
**阅读文章：[Blockspace Charters: Superchain-first Governance](https://gov.optimism.io/t/season-6-introducing-blockspace-charters-superchain-first-governance/8133)**

#### 关键概念
1. [Law of Chains](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md)
   - 类似于Optimism Collective的[Operating Manual](https://github.com/ethereum-optimism/OPerating-manual/blob/main/manual.md)。
   - 它定义了集体治理的指导原则，为不同类型的超级链区块空间提供具体的实施细节。
   - 但没有定义投票周期、法定人数等具体机制。
2. Superchain Registry 注册表
   - 在 Blockspace 宪章框架中发挥关键作用，作为超级链组成部分的可访问索引。
   - 充当根据特定宪章接受哪些链的真相来源，并记录为每条链选择的特定配置值。用于存储和管理链的注册信息。
   - 纳入超级链注册表仅意味着纳入超级链。 超级链注册表实施了一个可扩展的分类系统，以清楚地划分哪些链属于哪些标准（因此属于哪个区块空间章程）
3. Incremental Rollout (Beta Registry) 增量测试版注册表
   -  (这部分没太看懂，明天继续研究)允许将一些初始链加入第一阶段安全理事会和超级链注册表

### 2025.04.01
**重读OP Stack及OP Superchain文档**
#### OP Stack
**文章：[Getting started with the OP Stack](https://docs.optimism.io/stack/getting-started)**
- 定义：OP Stack 是一个标准化、共享和开源的开发堆栈，为 Optimism 提供支持，由 Optimism Collective 维护。OP Stack 是支持 Optimism 的所有软件。随着 Optimism 的发展，OP Stack 也将不断发展。
- OP Stack 可以被视为软件组件，它既可以帮助定义 Optimism 生态系统的特定层，也可以在现有层中充当模块的角色。 尽管 OP Stack 目前的核心是运行 L2 区块链的基础设施，但 OP Stack 理论上可以扩展到底层区块链之上的层，包括区块浏览器、消息传递机制、治理系统等工具。
- 可以理解OP Stack是包含所有OP相关的开发组件，而Superchain是其中一部分。

#### Superchain
**文章：[Superchain Explainer](https://docs.optimism.io/superchain/superchain-explainer)**
- 继 Bedrock 之后，OP Stack 的下一个重大可扩展性改进是引入**超级链(Superchain)的概念**：共享Bridge、DAO、Upgrade、通信层等的链网络，所有这些都构建在 OP Stack 上。Superchain可以实现将把 OP 主网和其他链合并到一个统一的 OP 链网络（即超级链内的链）中。
- 超级链是一个 L2 链网络，称为 OP 链，共享安全性、通信层和开源技术堆栈（OP Stack）。然而，与多链设计不同，这些链是标准化的，旨在用作可互换的资源。这使得开发人员能够构建以整个超级链为目标的应用程序，并抽象出应用程序运行的底层链。互操作性和标准化使工具和钱包能够同等对待各个链。

- (4.1 备注：未完待续)

### 2025.04.02
- 继续阅读**文章：[Superchain Explainer](https://docs.optimism.io/superchain/superchain-explainer)**

- 为什么要引入Superchain？
   - 区块链的横向可扩展性从根本上需要多个链。这是因为同步链的硬件要求随着链执行的计算量而线性增加。因此，为了实现水平扩展，我们必须并行运行链。（这里有点类似SQL数据库服务器有处理能力上限一样，当数据量和查询量增加时，单服务器的 CPU、内存等硬件资源会成为瓶颈。解决方案是使用分片（Sharding）或主从复制，将数据和负载分散到多个服务器，这里的分片就是多个链）
- 多链的问题
   - 每条链都会引入一种新的安全模型，这会增加系统性风险和开发的复杂性。
   - 每条链都有对应的验证者和区块生产者，成本又增加了。
- 超级链的解决方案
   - 由一个单一共享区块链（“L1”链），它可以作为多链系统中所有链（“L2”链）的共享事实来源。实现：
      - 在所有链上实施标准安全模型； 
      - 删除链部署需要一组新验证器的要求，因为每个 L2 链都使用 L1 共识。
   - Bedrock引入了L1链衍生的L2链，所有链数据都可以基于L1区块进行同步。
   - Bedrock引入了SystemConfig合约，开始直接用L1智能合约定义一些L2链。这可以扩展为将定义 L2 的所有信息放在 L1 上。包括生成唯一的链ID、区块gas limit等关键配置值等。随着 L1 链工厂扩展此功能以将所有配置放在链上，乐观节点应该可以在给定单个 L1 地址和到 L1 的连接的情况下确定性地同步任何OP 链。
   - 当OP链同步时，链状态在本地计算。这意味着确定 OP 链的状态是完全无需许可且安全的。链推导不需要证明系统，因为所有无效交易都会被节点执行的本地计算过程忽略。然而，仍然需要一个证明系统来启用超级链提款。
- 无须许可的提款
   - 提款声明（又名无许可提案）——允许任何人提交提款（又名提案），而不仅仅是指定的提案者。这将从系统中删除许可角色，使用户能够提交自己的提款消息。
   - 无提交间隔的按需提案——仅当用户需要撤回时才提出撤回声明。这消除了部署新 OP 链时产生的开销。
   - 在设想的故障证明系统中，任何人都可以提交提款索赔，并且这些提款索赔可以随时提交。当索赔附带债券时，提交提款索赔可能无需许可，因为如果索赔被证明无效，这些债券将充当抵押品。如果挑战者成功挑战该声明，则会向挑战者支付保证金，以奖励他们参与保护系统的安全，从而即使在这个无需许可的系统中也可以防止spam

### 2025.04.03
1. 阅读**文章：[The Superchain Registry 超级链注册表](https://docs.optimism.io/superchain/superchain-registry)**
   - 定义：The Superchain Registry serves as the source of truth for who's in the Superchain Ecosystem and what modifications they've made. 
   - 解释：Superchain Registry就是一个**共享的事实来源**索引，用于存储和管理链的注册信息，以及链对应的配置。
   - 托管 Superchain 配置数据，并包括主网和测试网 Superchain 目标及其各自的成员链。其他配置，例如合约权限和 SystemConfig 参数，都在链上托管和管理。超级链生态系统成员： 已达成协议，将sequencer收入返还给 Optimism Collective 的链。
2. 操作手册：[**添加一条链到registery**](https://github.com/ethereum-optimism/superchain-registry/blob/main/docs/ops.md#adding-a-chain)
   - 从2025年3月开始，必须使用[`op-deployer`](https://docs.optimism.io/operators/chain-operators/tools/op-deployer)部署
   - 另一个[`op-deployer`开发者文档](https://devdocs.optimism.io/op-deployer/)
3. Superchain Registery的[主github仓库](https://github.com/ethereum-optimism/superchain-registry)
   - 从仓库里找到的一些有意思的文档，比如[目前的主要chain](https://raw.githubusercontent.com/ethereum-optimism/superchain-registry/refs/heads/main/CHAINS.md)：

      **1. mainnet**
      | Chain Name | OP Governed[^1] | Superchain Hardforks[^2] | Explorer | Public RPC | Sequencer RPC
      |---|---|---|---|---|---|
      | Automata Mainnet | ❌ | ❌ | https://explorer.ata.network | `https://rpc.ata.network` | `https://automata-mainnet.alt.technology/` |
      | BOB | ❌ | ✅ | https://explorer.gobob.xyz | `https://rpc.gobob.xyz` | `https://rpc.gobob.xyz` |
      | Base | ❌ | ✅ | https://explorer.base.org | `https://mainnet.base.org` | `https://mainnet-sequencer.base.org` |
      | Binary Mainnet | ❌ | ✅ | https://explorer.thebinaryholdings.com | `https://rpc.zero.thebinaryholdings.com` | `https://sequencer.bnry.mainnet.zeeve.net` |
      | Cyber Mainnet | ❌ | ❌ | https://cyberscan.co/ | `https://rpc.cyber.co` | `https://cyber.alt.technology/` |
      | Ethernity | ❌ | ✅ | https://ernscan.io | `https://mainnet.ethernitychain.io` | `https://mainnet.ethernitychain.io` |
      | Funki | ❌ | ❌ | https://funki.superscan.network | `https://rpc-mainnet.funkichain.com` | `https://rpc-mainnet.funkichain.com` |
      | HashKey Chain | ❌ | ❌ | https://explorer.hsk.xyz | `https://mainnet.hsk.xyz` | `https://hashkeychain-mainnet.alt.technology` |
      | Ink | ✅ | ✅ | https://explorer.inkonchain.com | `https://rpc-gel.inkonchain.com` | `https://rpc-gel.inkonchain.com` |
      | Lisk | ❌ | ✅ | https://blockscout.lisk.com | `https://rpc.api.lisk.com` | `https://rpc.api.lisk.com` |
      | Lyra Chain | ❌ | ✅ | https://explorer.lyra.finance | `https://rpc.lyra.finance` | `https://rpc.lyra.finance` |
      | Metal L2 | ✅ | ✅ | https://explorer.metall2.com | `https://rpc.metall2.com` | `https://rpc.metall2.com` |
      | Mint Mainnet | ❌ | ✅ | https://explorer.mintchain.io | `https://rpc.mintchain.io` | `https://rpc.mintchain.io` |
      | Mode | ✅ | ✅ | https://explorer.mode.network | `https://mainnet.mode.network` | `https://mainnet-sequencer.mode.network` |
      | OP Mainnet | ✅ | ✅ | https://explorer.optimism.io | `https://mainnet.optimism.io` | `https://mainnet-sequencer.optimism.io` |
      | Orderly Mainnet | ❌ | ✅ | https://explorer.orderly.network | `https://rpc.orderly.network` | `https://rpc.orderly.network` |
      | Polynomial | ❌ | ✅ | https://polynomialscan.io | `https://rpc.polynomial.fi` | `https://rpc.polynomial.fi` |
      | RACE Mainnet | ❌ | ❌ | https://racescan.io/ | `https://racemainnet.io` | `https://racemainnet.io` |
      | Redstone | ❌ | ❌ | https://explorer.redstone.xyz | `https://rpc.redstonechain.com` | `https://rpc.redstonechain.com` |
      | Settlus Mainnet | ❌ | ❌ | mainnet.settlus.network | `https://settlus-mainnet.g.alchemy.com/public` | `https://settlus-mainnet-sequencer.g.alchemy.com/` |
      | Shape | ❌ | ❌ | https://shape-mainnet.explorer.alchemy.com/ | `https://mainnet.shape.network/` | `https://shape-mainnet-sequencer.g.alchemy.com` |
      | SnaxChain | ❌ | ✅ | https://explorer.snaxchain.io | `https://mainnet.snaxchain.io` | `https://mainnet.snaxchain.io` |
      | Soneium | ✅ | ✅ | https://soneium.blockscout.com/ | `https://rpc.soneium.org` | `https://rpc.soneium.org` |
      | Superseed | ❌ | ❌ | https://explorer.superseed.xyz | `https://mainnet.superseed.xyz` | `https://mainnet.superseed.xyz` |
      | Swan Chain Mainnet | ❌ | ❌ | https://swanscan.io | `https://mainnet-rpc.swanchain.org` | `https://sequencer-mainnet.swanchain.org` |
      | Swellchain | ✅ | ❌ | https://explorer.swellnetwork.io | `https://swell-mainnet.alt.technology` | `https://swell-mainnet.alt.technology` |
      | Unichain | ✅ | ✅ | https://explorer.unichain.org | `https://mainnet.unichain.org` | `https://mainnet-sequencer.unichain.org` |
      | World Chain | ❌ | ❌ | https://worldchain-mainnet.explorer.alchemy.com/ | `https://worldchain-mainnet.g.alchemy.com/public` | `https://worldchain-mainnet-sequencer.g.alchemy.com` |
      | Xterio Chain (ETH) | ❌ | ❌ | https://eth.xterscan.io/ | `https://xterio-eth.alt.technology/` | `https://xterio-eth.alt.technology/` |
      | Zora | ✅ | ✅ | https://explorer.zora.energy | `https://rpc.zora.energy` | `https://rpc.zora.energy` |
      | arena-z | ✅ | ✅ | https://explorer.arena-z.gg | `https://rpc.arena-z.gg` | `https://rpc.arena-z.gg` |
      
      **2. sepolia**

      | Chain Name | OP Governed[^1] | Superchain Hardforks[^2] | Explorer | Public RPC | Sequencer RPC
      |---|---|---|---|---|---|
      | Base Sepolia Testnet | ❌ | ✅ | https://sepolia-explorer.base.org | `https://sepolia.base.org` | `https://sepolia-sequencer.base.org` |
      | Binary Sepolia | ❌ | ❌ | https://explorer.sepolia.thebinaryholdings.com | `https://rpc.testnet.thebinaryholdings.com` | `https://sequencer.rpc.bnry.testnet.zeeve.net` |
      | Creator Chain Testnet | ❌ | ✅ | https://explorer.creatorchain.io | `https://rpc.creatorchain.io` | `https://rpc.creatorchain.io` |
      | Cyber Testnet | ❌ | ❌ | https://testnet.cyberscan.co/ | `https://rpc.testnet.cyber.co` | `https://cyber.alt.technology/` |
      | Ethernity Testnet | ❌ | ✅ | https://testnet.ernscan.io | `https://testnet.ethernitychain.io` | `https://testnet.ethernitychain.io` |
      | Funki Sepolia Testnet | ❌ | ❌ | https://sepolia-sandbox.funkichain.com/ | `https://funki-testnet.alt.technology` | `https://funki-testnet.alt.technology` |
      | Ink Sepolia | ✅ | ✅ | https://explorer-sepolia.inkonchain.com | `https://rpc-gel-sepolia.inkonchain.com` | `https://rpc-gel-sepolia.inkonchain.com` |
      | Lisk Sepolia Testnet | ❌ | ✅ | https://sepolia-blockscout.lisk.com | `https://rpc.sepolia-api.lisk.com` | `https://rpc.sepolia-api.lisk.com` |
      | Metal L2 Testnet | ✅ | ✅ | https://testnet.explorer.metall2.com | `https://testnet.rpc.metall2.com` | `https://testnet.rpc.metall2.com` |
      | Mode Testnet | ✅ | ✅ | https://sepolia.explorer.mode.network | `https://sepolia.mode.network` | `https://sepolia.mode.network` |
      | OP Sepolia Testnet | ✅ | ✅ | https://sepolia-optimistic.etherscan.io | `https://sepolia.optimism.io` | `https://sepolia-sequencer.optimism.io` |
      | Pivotal Sepolia | ❌ | ❌ | https://sepolia.pivotalscan.org/ | `https://sepolia.pivotalprotocol.com/` | `https://sepolia.pivotalprotocol.com/` |
      | RACE Testnet | ❌ | ❌ | https://testnet.racescan.io/ | `https://racetestnet.io` | `https://racetestnet.io` |
      | Settlus Sepolia | ❌ | ❌ | sepolia.settlus.network | `https://settlus-septestnet.g.alchemy.com/public` | `https://settlus-sep-testnet-sequencer.g.alchemy.com/` |
      | Shape Sepolia Testnet | ❌ | ❌ | https://shape-sepolia.explorer.alchemy.com/ | `https://sepolia.shape.network/` | `https://shape-sepolia-sequencer.g.alchemy.com` |
      | Soneium Testnet Minato | ✅ | ✅ | https://soneium-minato.blockscout.com/ | `https://rpc.minato.soneium.org` | `https://rpc.minato.soneium.org` |
      | Unichain Sepolia Testnet | ✅ | ✅ | https://sepolia.uniscan.xyz | `https://sepolia.unichain.org` | `https://sepolia-sequencer.unichain.org` |
      | World Chain Sepolia Testnet | ❌ | ❌ | https://worldchain-sepolia.explorer.alchemy.com/ | `https://worldchain-sepolia.g.alchemy.com/public` | `https://worldchain-sepolia-sequencer.g.alchemy.com` |
      | Zora Sepolia Testnet | ✅ | ✅ | https://sepolia.explorer.zora.energy | `https://sepolia.rpc.zora.energy` | `https://sepolia.rpc.zora.energy` |
      | arena-z-testnet | ❌ | ❌ | https://arena-z.blockscout.com | `https://rpc.arena-z.t.raas.gelato.cloud` | `https://rpc.arena-z.t.raas.gelato.cloud` |

      **3. sepolia-dev-0**
      | Chain Name | OP Governed[^1] | Superchain Hardforks[^2] | Explorer | Public RPC | Sequencer RPC
      |---|---|---|---|---|---|
      | Base devnet 0 | ❌ | ✅ |  | `` | `` |
      | OP Labs Sepolia devnet 0 | ✅ | ✅ |  | `` | `` |


      [^1]: Chains are governed by Optimism if their `L1ProxyAdminOwner` is set to the value specified by the standard config and [configurability.md](https://github.com/ethereum-optimism/specs/blob/main/specs/protocol/configurability.md#l1-proxyadmin-owner).
      [^2]: Chains receive Superchain hardforks if they've specified a `superchain_time`. This means that they have opted-into Superchain-wide upgrades.

### 2025.04.04
阅读**文章：[Superchain upgrades 超级链升级](https://docs.optimism.io/superchain/superchain-upgrades)**
**Superchain Upgrade的架构设计**
Superchain 通过协调一致的硬分叉机制实现多链同步升级，这种设计确保了整个生态系统的一致性和安全性
- 类似于传统数据库的主从架构，主库（L1）的变更会同步到所有从库（L2）
- 通过统一的升级机制降低了多链管理的复杂性，也可以避免不同链之间的版本差异导致的兼容性问题

**升级机制**
1. `Superchain Target`超级链目标
   - L1 智能合约的变更必须与最新激活的 L2 功能兼容，并通过 L1 合约升级来执行。
   - A Superchain Target定义了一组在 OP-Stack 链之间共享的激活规则和 L1 合约升级，以便集体升级链。

2. `ProtocolVersion`  L1合约作为中心化的版本管理系统，统筹整个 Superchain 的协议版本演进
   - 合约充当类似于 Git 仓库的角色，记录和管理所有链的版本信息。
   - 通过链上信号机制实现版本同步，确保所有节点的一致性，避免不同链之间的不一致
   - 版本不兼容时自动触发节点暂停，防止链分叉
      - 区块高度触发：确保网络达到特定状态才进行升级
      - 时间戳触发：提供时间维度的协调，便于各方提前准备
      - 自动继承机制降低了链维护的操作复杂度
   - 激活规则设计采用双重保障机制，确保升级的平稳过渡。通过激活规则，L2 状态转换函数的改变在所有节点上确定性地转换。
**安全保障措施**
- `rollup.halt` 标志系统在执行层和共识层实现双重保护，确保升级过程的安全性，通过强制停止机制允许节点在遇到不兼容的协议版本时停止（这种设计类似于传统分布式系统中的熔断机制，保护系统稳定性）
  - 执行层 (op-geth) 的版本控制类似于软件的语义化版本管理
  - 共识层 (op-node) 的保护机制确保节点网络的一致性

### 2025.04.05
阅读**文章：[The Blockspace and Standard Rollup charters](https://docs.optimism.io/superchain/blockspace-charter)**
Blockspace Charters (区块空间宪章)为超级链生态系统提供了必要的技术和治理框架。Standard Rollup Charter(标准 Rollup宪章) 是几个具有不同定制和安全保障的区块空间宪章中的第一个。
- 区块空间宪章： 一种框架，为 Optimism 生态系统中的区块空间建立标准、管理政策和预先承诺，确保安全性、正常运行时间并符合链的法则。
- 标准 Rollup 宪章：第一个区块空间章程，定义了最高安全性区块空间的技术和治理要求。通过遵守标准 Rollup 章程，链可以达到“标准”状态，确保一致性、高安全性和操作可靠性。
- 超级链注册表是链的索引，可作为超级链生态系统中成员和链配置的真实来源。注册表检查是否符合标准汇总章程。superchain_level superchain_level = 2 的链满足被归类为标准汇总的所有标准。

### 2025.04.06
继续阅读**文章：[The Blockspace and Standard Rollup charters](https://docs.optimism.io/superchain/blockspace-charter)**
区块空间宪章 Blockspace Charters是一种框架，为 Optimism 生态系统中的区块空间建立标准、管理政策和预先承诺，确保安全性、正常运行时间并符合链的法则。
Blockspace Charters的三个组成部分
1. Criteria：预先定义的技术参数
   - Version 版本控制：确保OP Stack的一致性
   - Configuration 配置参数：涵盖静态和动态变量，确保部署的规范性
   - Solvency：通过偿付能力验证确保链历史中的所有状态转换都是有效的
2. Governing policies：行为规范和管理机制
   - 明确界定sequencers and upgrade key holders等各角色的职责和行为准则
   - 建立违规处理机制，保障生态系统的健康运行
   - 确保与Law of Chains的一致性，保护用户权益
3. Commitments：预先承诺
   - 明确承诺链的安全性、正常运行时间和合规性
   - 比如fee模式或链上出块角色分离的未来更新。


### 2025.04.07
继续阅读**文章：[The Blockspace and Standard Rollup charters](https://docs.optimism.io/superchain/blockspace-charter)**

Blockspace Charters 的标准以两种方式设定：通过治理投票或由乐观基金会 (Optimism Foundation) 制定。
- 通过治理投票：章程中引用的三个 TOML 文件（标准配置参数、标准配置角色和标准版本 standard config params(opens in a new tab), standard config roles(opens in a new tab), and standard versions(opens in a new tab)）需要治理投票才能更改。
- 由乐观基金会制定：除上述三个 TOML 文件之外，对验证的更改仍由基金会酌情决定。这包括但不限于对 BHIC 、其他配置检查和 RPC 可用性的更改。

<!-- Content_END -->
