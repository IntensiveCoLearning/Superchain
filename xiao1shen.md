---
timezone: UTC+8
---

> 请在上边的 timezone 添加你的当地时区(UTC)，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区


# 你的名字

1. 自我介绍
来自浙江金华，上海大学计算机系人工智能专业大三学生，平时喜欢小说和游泳，希望能够在此次活动中有所收获。
2. 你认为你会完成本次残酷学习吗？
本人对区块链等方面比较感兴趣，而且不太喜欢半途而废，尽量努力坚持本次残酷共学。
3. 你的联系方式（推荐 Telegram）
4. vx：15727975092

## Notes

<!-- Content_START -->

### 2025.03.31

学习总结：Blockspace Charter与Superchain治理框架

在Optimism治理的第六季中，提出了**Blockspace Charter**（区块空间宪章）这一新的治理文件框架。本文介绍了Blockspace Charter的定义、目的和重要性，并将推出第一份草案——**Standard Rollup Charter**（标准Rollup宪章），并寻求社区的批准。这一框架的推出旨在为Superchain生态系统提供更加清晰和一致的技术治理标准。

1. **Blockspace Charter的定义**

Blockspace Charter由三个主要组成部分构成：

- **标准**：定义哪些链属于特定的宪章范围，包括协议版本（OP Stack的版本）和配置（链的参数化部署情况）。
  
- **治理政策**：定义治理过程中不同角色应遵循的规则和程序，例如如何处理违反规则的情况。
  
- **预承诺**：对未来升级的承诺，确保治理框架的长期稳定性和一致性，为Superchain的未来发展提供方向。

2. **区块链的多样性与挑战**

随着Superchain生态系统的快速发展，基于OP Stack的不同链在技术上并非完全等同。它们可能使用不同版本的OP Stack，或者在同一版本下配置不同的参数。这种生态系统碎片化问题使得用户和开发者难以理解每条链的属性与保证，需要有一个清晰的框架来解决这些问题。

3. **Blockspace Charter的作用与意义**

Blockspace Charter的引入旨在为不同类型的Superchain区块空间提供具体的治理标准，确保每个链都能在符合特定标准的基础上运行。它不仅帮助社区理解不同链的特性，还确保治理过程的一致性和透明性。此外，预承诺部分有助于稳定生态系统，减少不确定性，为创新提供保障。

4. **Superchain注册表与升级提案**

Blockspace Charter的实施将与**Superchain注册表**和**升级提案流程**相结合。Superchain注册表作为一个公共的索引，管理哪些链符合特定宪章的标准，并记录链的配置。这一透明度有助于维护Superchain的安全性和一致性。

同时，升级提案将与Blockspace Charter紧密对接，确保每次升级都考虑到相关链的特性，并对治理政策进行必要的调整和更新。这一流程将提升Superchain治理的透明性和责任感，确保每个决策都是经过深思熟虑并符合长远发展目标的。

5. **未来展望**

Blockspace Charter的引入不仅是Superchain治理框架的升级，也为优化治理机制、促进生态系统健康发展提供了强有力的支持。随着进一步的开发和更新，社区将有更多机会参与到这一治理体系的构建中，从而确保Superchain在多样化技术环境中的稳定性与创新性。

总的来说，Blockspace Charter的实施是Optimism治理的一项重要进步，它通过明确的技术标准、清晰的治理流程和预期的未来承诺，为Superchain提供了坚实的基础，使其能够应对未来的挑战和机遇。

### 2025.4.1
今天具体学了Blockspace Charter的三大组成部分
Blockspace Charter是Optimism Superchain生态系统中的一个技术治理框架，它的主要作用是明确不同区块空间（blockspace）的技术标准、治理方式及未来发展方向。
标准规定了哪些链符合特定Blockspace Charter的要求，即它们的技术标准是什么。协议版本（Version）规定某条链需要使用特定版本的OP Stack（Optimism的底层协议栈）。配置（Configuration）说明不同链在相同版本的OP Stack下可能会有不同的部署参数。安全性与偿付能力（Solvency）表明确保链的交易记录是有效的，尤其是防止无效的资产提现或错误输出导致跨链桥（Bridge）资金短缺。
治理政策部分定义了Superchain生态系统中不同利益相关方如何参与治理，以及如何保证治理过程的透明性、公正性和可执行性。如规定哪些治理角色（如Security Council、安全委员会）需要持有哪些权限，规定不同治理角色的行为标准，并确定如何处理违规行为，以及治理流程，如何提交治理提案，如何投票以及如何执行。
预承诺部分定义了Superchain生态系统的长期发展方向，确保治理框架具有稳定性和可持续性。预承诺的核心目标是提供稳定性和长期发展方向，让链的开发者、用户和治理参与者能够在明确的规则下做出合理的决策，减少治理的不确定性。

### 2025.4.2
今天具体学了超级链和区块链的区别。
1.区块链（Blockchain）
区块链是去中心化的分布式账本技术（DLT, Distributed Ledger Technology），用于记录不可篡改的交易数据。每个区块都包含一组交易，并通过密码学链接成链，从而保证数据的安全性和透明度。
区块链的核心特点：
去中心化：数据由多个节点维护，避免单点故障。
不可篡改性：数据一旦上链，无法被修改或删除。
智能合约：支持自动执行代码，如以太坊上的智能合约。
共识机制：通过PoW（工作量证明）、PoS（权益证明）等机制保障安全性。
区块链的分类：
公链（Public Blockchain）：如以太坊、比特币，任何人都可以加入和使用。
私链（Private Blockchain）：如企业级区块链，只有授权用户可访问。
联盟链（Consortium Blockchain）：由多个机构共同维护，如Hyperledger。
区块链的应用：
数字货币（如比特币） 去中心化金融（DeFi） 供应链管理 NFT和元宇宙
2. 超级链（Superchain）
超级链（Superchain）是一个由多个区块链组成的去中心化网络，旨在提升区块链的互操作性（Interoperability）、可扩展性（Scalability）和用户体验。它通常由一组兼容的区块链构成，这些链可以共享某些基础设施，例如共识机制、数据可用性层（DA Layer）、跨链通信协议等。
超级链的核心特点：
多个区块链组成的生态，不同的链可以互操作（比如在不同链上转移资产）。
共享部分基础设施，如共识机制、桥接协议、Sequencer（交易排序者）。
扩展性强，可以通过增加新的链来提高整个生态的吞吐量。
跨链通信，不同链之间可以高效、安全地传输数据和资产。

###2025.4.3
今天具体学了superchain注册
Superchain注册表（Superchain Registry）是一个公共索引（Public Index），其核心作用是管理和记录符合Blockspace Charter标准的区块链。
Superchain注册表提供了一种标准化的方式 来管理和维护生态系统内的所有链，确保它们符合统一的技术和治理框架。
升级提案流程确保Superchain的持续发展，让技术演进和治理变革更加透明和可控。
Blockspace Charter作为整个治理框架的基石，确保每一次技术升级和决策都符合Superchain的长期发展方向，避免短期利益驱动的决策破坏生态稳定性。
这种机制的最终目标是提升Superchain的安全性、互操作性和可持续发展能力，让整个生态更加稳健、可靠。

###2025.4.5
今天具体学了区块链的基本组成和核心技术
1、基本组成
区块（Block）	记录若干交易数据的容器，每个区块有时间戳、前一个区块哈希等信息
链（Chain）	所有区块按顺序连接，形成区块链
哈希（Hash）	通过加密算法生成的固定长度字符串，用于标识数据内容，确保不可篡改
共识机制	网络节点达成一致的方法，常见的有PoW、PoS、DPoS等
节点	区块链网络中的参与者，可分为全节点、轻节点等
智能合约	一种自动执行的合约代码，可在链上运行逻辑应用，如DeFi、NFT
2、核心技术
共识机制：让分布式节点就同一状态达成共识的规则。
PoW（工作量证明）：靠算力竞争（比特币）
PoS（权益证明）：根据质押代币量选择记账者（以太坊2.0）
DPoS（委托权益证明）：选出代表节点参与共识
智能合约（Smart Contract）
在区块链上自动执行的代码，无需第三方信任。
典型用途：自动发币、拍卖、投票、借贷
虚拟机（EVM等）
区块链的“运行环境”，如以太坊虚拟机（EVM），用于执行合约。
Token（代币）
基于区块链生成和流通的数字资产。ERC-20、ERC-721（NFT）是常见标准。
3、区块链技术以其去中心化、不可篡改、可追溯等特性，正在从数字货币扩展到更广泛的应用领域。在金融领域，区块链推动了去中心化金融（DeFi）的发展，提供无需中介的借贷、交易等服务；在文化产业中，非同质化代币（NFT）让数字艺术、游戏资产等具备确权和交易能力；去中心化自治组织（DAO）则实现了社群共治的新型组织方式。此外，区块链还被广泛用于供应链溯源、数字身份认证、隐私保护，以及Web3内容与社交平台，逐步构建起一个更加开放、安全、透明的数字生态系统。
今天还在搭建superchain的环境。

###2025.4.6
今天尝试搭建superchain
搭建自己的 OP Stack 链（Superchain 子链）
准备环境
一台运行 Linux 的服务器（建议 Ubuntu 20.04+）
Docker 和 Docker Compose
Git
Go 环境（1.20+）
Node.js（建议 18+）
Yarn or npm

###2025.4.8 
区块链的底层技术之一，密码学
 一、哈希函数（Hash Function）
哈希函数是一种**单向加密函数**，可以将任意长度的数据映射为固定长度的字符串（称为哈希值或摘要）。
✅ 特点：
1. **不可逆性**：无法从哈希值推导出原始输入；
2. **抗碰撞性**：几乎不可能找到两个不同的输入，输出相同的哈希值；
3. **雪崩效应**：输入信息只要发生微小变动，输出的哈希值就会有很大变化；
4. **固定长度输出**：无论输入多长，输出哈希值长度固定（如 SHA-256 输出为 256 位）。
✅ 在区块链中的作用：
**区块标识**：每个区块的哈希值作为其“身份证”；
**连接前后区块**：当前区块包含前一区块的哈希值；
**数据完整性校验**：交易信息哈希后写入链，后续可快速校验数据是否被篡改。
 二、非对称加密（Asymmetric Encryption）
非对称加密使用**一对密钥：公钥（public key）与私钥（private key）**。公钥加密的数据只能用对应私钥解密，反之亦然。
 ✅ 典型算法：
**RSA（Rivest-Shamir-Adleman）**：经典算法，安全性强但速度较慢；
**ECC（Elliptic Curve Cryptography）**：以椭圆曲线数学为基础，相同安全等级下密钥更短、效率更高（以太坊常用）。
✅ 在区块链中的应用：
**加密信息**：如在某些隐私保护链（如 Zcash）中，交易信息使用公钥加密；
**签名验证**：结合私钥生成签名，公钥验证，见下节“数字签名”。
 三、数字签名（Digital Signature）
数字签名是基于非对称加密实现的一种**身份认证机制**，可以用于验证交易数据是否来自某个特定的账户。
✅ 工作流程：
1. 交易发起者用**私钥**对交易内容生成签名；
2. 网络节点使用其**公钥**验证签名是否有效；
3. 验证通过说明：
   - 交易未被篡改（完整性）；
   - 交易确由该账户发出（不可否认性）。
✅ 在区块链中的应用：
**每一笔交易**都包含发送者的签名；
**节点拒绝未通过验证的交易**；
保证链上交易“谁干的，跑不了”。
四、Merkle 树（默克尔树）
Merkle 树是一种**哈希二叉树结构**，用于高效组织和验证大量数据的完整性。
✅ 结构图简化：
      Merkle Root
         /    \
      H1      H2
     / \     / \
   T1  T2  T3  T4
每个叶子节点（T1-T4）是交易数据的哈希；
父节点是其子节点的哈希拼接后再哈希的结果；
顶端的根节点即“Merkle Root”。
✅ 在区块链中的作用：
- 每个区块包含一个 Merkle Root，代表所有交易的摘要；
- **验证单笔交易是否存在**于区块中，只需部分路径即可，不用验证整个区块（节省计算资源）；
- 提高查询效率，尤其在轻节点（如手机钱包）中作用明显。
## 总结表格：
| 密码学技术 | 主要作用 | 应用示例 |
|------------|-----------|-----------|
| 哈希函数 | 数据完整性、抗篡改 | 区块链接、数据摘要 |
| 非对称加密 | 数据机密性、身份认证 | 加密传输、公私钥账户系统 |
| 数字签名 | 验证身份、不可抵赖 | 交易签名与验证 |
| Merkle 树 | 批量数据验证 | 验证交易是否包含在区块中 |
## 下面是密码学在以太坊中的应用
密码学技术	以太坊中的实际应用
哈希函数（Keccak-256）	地址生成、交易哈希、合约哈希、树结构
非对称加密（ECC secp256k1）	钱包地址、身份认证、公钥-私钥体系
数字签名（ECDSA）	交易签名、合约调用授权
Merkle 树（+ Patricia Trie）	快速验证交易、状态与事件日志完整性

### 2025.4.9
今天具体学习了智能合约
智能合约是一种自动化、无需中介、去中心化的合约，通常由一段代码组成，存储在区块链上，一旦满足特定条件，自动执行约定的操作。
简而言之，智能合约是一些编程代码，它们规定了某种“规则”，并且在满足这些规则时自动执行合约内容。
（1）特性：
自动执行：无需第三方介入，当预设条件满足时，合约自动执行，不可更改。
去中心化：合约运行在区块链上，由网络中的节点共同验证和执行，没有中央控制者。
透明性：合约代码公开，任何人都可以查看、审计其内容，确保合约的公正性。
不可篡改性：一旦部署到区块链上，智能合约不能更改，避免恶意修改或篡改。
（2）智能合约的工作流程
编写合约：开发者使用特定的编程语言（如 Solidity）编写合约代码。
部署合约：合约被部署到区块链上。部署时需要支付一定的 gas 费用（以太坊中是指交易费用）。
调用合约：合约一旦部署，就可以被任何人调用，只要他们满足合约中的条件。
自动执行：当合约条件满足时，合约会自动执行，无需人工干预。
例如：
假设有一个简单的智能合约，用于在某个条件下向指定地址转账。当满足条件（例如，某个用户存入足够数量的ETH）时，合约就自动将ETH转账到指定账户。
（3）智能合约的编程语言：Solidity
✅ Solidity：是最常用的智能合约编程语言，专门为以太坊平台设计。它是基于 JavaScript 和 Python 等语言的，易于理解和学习。
Solidity 的特点：
静态类型语言：在编写智能合约时，开发者需要声明每个变量的类型（如 uint、address 等）。
合约结构：Solidity 通过 contract 定义合约，合约可以包含状态变量、函数、事件等元素。
支持继承：Solidity 支持合约的继承，使得合约代码可以更易复用和扩展。
事件和日志：Solidity 可以定义事件，当某个特定操作发生时，触发事件并记录日志，供外部应用查询。
Gas费用管理：Solidity 允许开发者管理每个操作的 Gas 消耗，以避免合约执行过程中产生过高费用。

智能合约是区块链技术的重要组成部分，通过 自动化、去中心化、不可篡改 等特性，能够为多个行业带来巨大变革，特别是在 DeFi、NFT、供应链管理 等领域。智能合约不仅仅是一个自动执行协议，更是区块链去中心化应用的核心驱动力。


### 2025.4.10
# 比特币交易脚本语言

## 1. 比特币交易基础

- **交易结构**：
  - 一个比特币交易包含输入（Input）和输出（Output）。
  - 输入指明所花费的比特币来源于之前的某个交易的输出。
  - 输出指定比特币的去向，可能已经被花费（Spent）或未花费（Unspent）。
  - 示例：一个交易有1个输入，2个输出，其中一个已花费，一个未花费，交易已有23个确认（Confirmation），回滚可能性低。

- **交易元数据（Metadata）**：
  - **Hash**：交易的唯一标识符。
  - **Version**：使用的比特币协议版本号。
  - **Size**：交易数据大小。
  - **Lock Time**：交易生效时间，通常为0（立即生效），非0表示延迟生效。
  - **Block Hash**：交易所在区块的哈希值，体现挖矿难度（哈希值以多个0开头）。
  - **Confirmation**：交易确认次数。
  - **Time & Block Time**：交易和区块生成的时间戳（从某一固定起点计算的秒数）。

---

## 2. 比特币脚本语言概述

- **特性**：
  - 比特币脚本语言是一种简单的**基于栈的语言（Stack-based Language）**。
  - 唯一的内存空间是堆栈，无全局变量、局部变量或动态内存分配（如C/C++）。
  - 不支持循环，避免死循环问题（非图灵完备），对比以太坊的智能合约语言（图灵完备，需Gas机制防止死循环）。

- **功能**：
  - 专注于密码学相关操作，如签名验证。
  - 通过输入脚本（Input Script）和输出脚本（Output Script）共同验证交易合法性。

---

## 3. 输入与输出脚本

- **输入结构**：
  - 输入是一个数组，可能包含多个来源。
  - 每个输入需指定：
    - **TxID**：前一交易的哈希值。
    - **Vout**：前一交易的输出序号（从0开始）。
    - **ScriptSig**（输入脚本）：通常提供签名，证明有权花费该输出。

- **输出结构**：
  - 输出也是数组，指定比特币去向。
  - 每个输出包含：
    - **Value**：金额（单位：BTC或Satoshi，1 BTC = 10^8 Satoshi）。
    - **ScriptPubKey**（输出脚本）：定义花费条件，通常包含公钥或其哈希。
    - **N**：输出序号。
    - **Require**：所需签名数量（默认1，支持多重签名）。
    - **Type**：输出类型（如PubKey、PubKeyHash）。

- **脚本执行**：
  - 输入脚本（ScriptSig）与前一交易的输出脚本（ScriptPubKey）拼接执行。
  - 早期：直接拼接执行。
  - 现在：为安全性分开执行，先执行输入脚本，再执行输出脚本。
  - 验证通过条件：脚本顺利执行，栈顶结果为非零值（True）。

---

## 4. 常见脚本形式

### 4.1 Pay to Public Key (P2PK)
- **输出脚本**：
  ```
  <Public Key> CHECKSIG
  ```
- **输入脚本**：
  ```
  <Signature>
  ```
- **执行过程**：
  1. 输入脚本将签名压入栈。
  2. 输出脚本将公钥压入栈。
  3. `CHECKSIG`弹出栈顶签名和公钥，验证签名有效性。
- **特点**：最简单形式，直接使用公钥。

### 4.2 Pay to Public Key Hash (P2PKH)
- **输出脚本**：
  ```
  DUP HASH160 <Public Key Hash> EQUALVERIFY CHECKSIG
  ```
- **输入脚本**：
  ```
  <Signature> <Public Key>
  ```
- **执行过程**：
  1. 输入脚本将签名、公钥压入栈。
  2. `DUP`复制公钥。
  3. `HASH160`计算公钥哈希。
  4. 输出脚本将预期哈希压入栈。
  5. `EQUALVERIFY`比较两个哈希是否相等。
  6. `CHECKSIG`验证签名。
- **特点**：最常用形式，使用公钥哈希而非直接公钥。

### 4.3 Pay to Script Hash (P2SH)
- **输出脚本**：
  ```
  HASH160 <Redeem Script Hash> EQUAL
  ```
- **输入脚本**：
  ```
  <Signatures> <Serialized Redeem Script>
  ```
- **执行过程**：
  1. 输入脚本提供签名和序列化的赎回脚本（Redeem Script）。
  2. 计算赎回脚本哈希，与输出脚本中的哈希比较。
  3. 若相等，反序列化并执行赎回脚本（内容自定义，如多重签名）。
- **验证**：
  - 第一步：验证赎回脚本哈希。
  - 第二步：执行赎回脚本。
- **应用**：支持复杂逻辑，如多重签名。

### 4.4 多重签名 (Multi-Signature)
- **实现方式**：
  - 原生：通过`CHECKMULTISIG`，输出脚本指定`m`（阈值）和`n`（公钥数），输入脚本提供至少`m`个签名。
  - P2SH：将多重签名逻辑放入赎回脚本，输出脚本仅提供哈希。
- **执行**：
  ```
  <m> <PubKey1> <PubKey2> ... <PubKeyN> <n> CHECKMULTISIG
  ```
  - 需额外压入一个无用元素（红色叉），因`CHECKMULTISIG`实现Bug多弹出一个元素。
  - 签名顺序需与公钥顺序一致。
- **优点**：
  - P2SH将复杂度转移到输入脚本，简化用户操作（如电商只需公布脚本哈希）。

### 4.5 Return脚本（销毁比特币）
- **输出脚本**：
  ```
  RETURN <Arbitrary Data>
  ```
- **特点**：
  - `RETURN`无条件返回错误，输出永远无法花费。
- **应用场景**：
  1. **销毁比特币**：证明付出代价以换取其他币种（如Altcoin）。
  2. **数据存储**：将哈希值嵌入（如知识产权保护），类似Coinbase域，但无需记账权。
- **实例**：
  - Coinbase交易：一个输出为正常奖励，另一个为`RETURN`，金额为0。
  - 普通交易：输入金额全作交易费，输出为`RETURN`，未真正销毁。

---

## 5. 脚本语言的设计与优劣

- **优点**：
  - 简单、无循环，避免停机问题（Halting Problem）。
  - 密码学功能强大（如`CHECKSIG`、`CHECKMULTISIG`）。
  - 针对比特币场景优化。

- **局限**：
  - 非图灵完备，功能受限（如不支持复杂逻辑）。
  - 对比以太坊：智能合约语言更强大，但需Gas机制控制执行。

---

## 6. 其他注意事项

- **操作码**：实际脚本使用`OP_`前缀（如`OP_CHECKSIG`），PPT简化省略。
- **UTXO友好**：`RETURN`脚本无需存储于UTXO集，减轻节点负担。

---

## 总结

比特币脚本语言虽简单，却通过栈机制和密码学操作高效支持交易验证。P2PK、P2PKH、P2SH等多种形式满足不同需求，尤其是P2SH的多重签名极大提升灵活性。`RETURN`脚本则提供销毁和数据存储的独特功能。相比以太坊的复杂性，比特币脚本在安全性和效率上找到平衡，值得深入学习！

--- 

### 2025.4.11
# 比特币交易脚本语言

## 比特币交易结构

- 交易由输入(inputs)和输出(outputs)组成
- 输入指向之前交易的输出(UTXO)
- 每个输入需要提供解锁脚本(scriptSig)
- 每个输出包含金额和锁定脚本(scriptPubKey)

## 脚本执行过程

1. 将输入脚本和输出脚本拼接(实际实现中是分开执行)
2. 从前往后依次执行指令
3. 执行后栈顶结果为非零(true)则验证通过

## 主要脚本类型

### 1. Pay to Public Key (P2PK)

**输出脚本:**
```
<Public Key> 
OP_CHECKSIG
```

**输入脚本:**
```
<Signature>
```

**执行过程:**
1. 压入签名
2. 压入公钥
3. OP_CHECKSIG验证签名

### 2. Pay to Public Key Hash (P2PKH)

**输出脚本:**
```
OP_DUP 
OP_HASH160 
<Public Key Hash> 
OP_EQUALVERIFY 
OP_CHECKSIG
```

**输入脚本:**
```
<Signature> 
<Public Key>
```

**执行过程:**
1. 压入签名
2. 压入公钥
3. 复制公钥(OP_DUP)
4. 取哈希(OP_HASH160)
5. 压入输出中的公钥哈希
6. 比较两个哈希(OP_EQUALVERIFY)
7. 验证签名(OP_CHECKSIG)

### 3. Pay to Script Hash (P2SH)

**输出脚本:**
```
OP_HASH160 
<Redeem Script Hash> 
OP_EQUAL
```

**输入脚本:**
```
<Signature(s)> 
<Serialized Redeem Script>
```

**执行过程分两阶段:**
1. 验证赎回脚本哈希匹配
   - 压入签名
   - 压入序列化赎回脚本
   - 计算哈希(OP_HASH160)
   - 压入输出中的哈希
   - 比较(OP_EQUAL)

2. 执行赎回脚本
   - 反序列化赎回脚本
   - 执行脚本内容

## 多重签名(Multisig)

使用OP_CHECKMULTISIG实现m-of-n多重签名

**传统实现:**
- 输出脚本中直接包含所有公钥和阈值
- 用户需要知道所有签名规则

**P2SH实现:**
- 输出脚本只包含赎回脚本哈希
- 赎回脚本中包含公钥和阈值
- 对用户更友好

**注意:**
- OP_CHECKMULTISIG有一个bug会多弹出一个栈元素
- 需要在输入脚本开头压入一个无用元素

## OP_RETURN脚本

- 以OP_RETURN开头的输出脚本
- 无条件返回错误，资金永远无法花费
- 用途:
  - 销毁比特币(Proof of Burn)
  - 在区块链上存储数据(如哈希值)
  - 比coinbase更通用的数据存储方式

## 比特币脚本特点

1. 基于栈的简单语言
2. 无循环，避免停机问题
3. 密码学操作功能强大
4. 针对比特币场景专门优化
5. 非图灵完备

与以太坊等智能合约平台相比，比特币脚本功能有限但更安全。



### 2025.4.12
分布式账本技术是一种通过分布在多个节点上的数据库来记录交易数据的技术，所有参与节点都可以访问、共享和同步数据副本，但没有中央控制者。
简单来说，它是一种“多人共同记账”的方式——每个人都保留着一份账本，并通过共识机制保证每一份账本内容一致。

特征	说明
去中心化	没有单一的控制方，所有节点共同维护账本。
同步共享	所有节点数据保持一致性，更新实时同步。
不可篡改性	记录一旦写入账本，即不可被随意更改或删除。
共识机制	所有节点需通过一定规则达成共识后，交易才可记录。
高透明性/隐私保护（视情况）	账本内容可以公开，也可以通过加密实现隐私保护。

区块链是分布式账本技术的一种实现方式，但并非所有 DLT 都是区块链

比较维度	区块链	分布式账本技术（DLT）
是否按“区块”组织数据	是	不一定
是否按时间顺序链接	是	不一定
是否使用链式结构	是	不一定
去中心化程度	强	可定制，部分DLT为联盟链或许可链
应用场景	比特币、以太坊、NFT等	企业协作、金融清算、政务管理等

举例：
比特币、以太坊是基于区块链的分布式账本；
IBM Hyperledger Fabric 是一种非区块链结构的分布式账本（使用分布式数据库+智能合约）。

分布式账本的工作机制（以区块链为例）
交易发起：某个节点发起一笔交易（如发送代币、上传信息）。
交易广播：交易信息被广播到网络中所有节点。
交易验证：节点通过共识机制验证交易是否合法。
打包记录：将验证通过的交易写入账本（如区块链中的新区块）。
账本同步：所有节点同步更新自己的账本副本，保持数据一致性。

分布式账本的技术组件
✅ 1. 共识机制
用于在没有中心管理者的前提下，多个节点就“谁来记账”达成一致。
常见算法：
PoW（工作量证明）：比特币
PoS（权益证明）：以太坊2.0、Solana
PBFT（拜占庭容错）：联盟链如 Fabric
DPoS、PoA、Raft 等也常见于企业级应用
✅ 2. 密码学加密
保证数据安全、参与者身份验证、防止篡改。
包括：哈希函数、非对称加密、数字签名等。
✅ 3. P2P 网络
点对点通信，每个节点既是客户端也是服务器，去除单点故障风险。
✅ 4. 数据结构
有的 DLT 采用区块链结构（如 Ethereum）；
有的使用有向无环图（DAG）结构（如 IOTA、Hashgraph）；
也可以是简单的时间戳数据库结构（如部分政务链）。

分布式账本的应用场景
应用场景	应用说明
金融服务	证券清算、跨境支付、供应链金融，提升结算效率、降低风险
供应链管理	产品溯源、物流追踪、防伪认证
数字身份	基于链上记录建立分布式身份（DID）
政务治理	电子政务、公证上链、医疗档案不可篡改保存
能源管理	分布式电力交易、电网自动调配



<!-- Content_END -->
