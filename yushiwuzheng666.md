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





<!-- Content_END -->
