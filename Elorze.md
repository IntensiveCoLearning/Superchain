---
timezone: UTC+8
---

> 请在上边的 timezone 添加你的当地时区(UTC)，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区


# 舒云展

1. 自我介绍
  大三计算机学院智能科学与技术专业在读学生，于今年两月在南塘接触Web3，看到南塘的伙伴转发本次活动，很有兴趣。
2. 你认为你会完成本次残酷学习吗？
   会，很有信心。
3. 你的联系方式（推荐 Telegram）
  telegram:Id: 7851916301
  微信号：Elorze_2270938474

## Notes

<!-- Content_START -->

### 2025.03.31

OP链：基于Optimism技术构建的一个二层扩容链，旨在提高以太坊的交易速度和降低费用。OP链通过“乐观假设”机制，默认交易室有效的，只有在有人挑战时才进行验证，从而大幅提升了效率。它通过将大部分计算和数据存储移到链外（L2），并将最终结果提交到以太坊主链（L1）上，达到扩展性和去中心化的平衡。

超级链：是一个由多个OP链组成的去中心化网络，它们共享一个统一的技术基础。目标是通过互联互通的链网络，提高效率、可扩展性和灵活性，同时保持去中心化和用户保护。超级链可以让不同链之间无缝协作，形成一个更加广阔和互联的生态系统。

链法v0.1是一套旨在确保超级链生态系统中各方参与者的公平性、保护和经济自主性的指导框架。它不是一个具有法律约束力的合同，而是针对生态系统内不同角色（如用户、链治理者和链服务者）应遵循的行为准则。

所有OP链必须共同升级，且升级必须向下兼容。

OP Stack：是Optimism提供的一个模块化技术框架，用于构建和部署Optimistic Rollups(OP链）。它包含一系列可重复使用的组件，用于处理交易、数据存储和共识等功能。

### 2025.04.01

阅读了Optimism社区的治理指南。
1、治理结构： Optimism有个特别的双层治理体系，分为“代币之家”(Token House)和“公民之家”(Citizens' House)。

代币之家：由持有OP代币的人组成，他们可以直接投票或者委托别人帮他们投票，决定一些治理提案，比如系统升级或者资金分配。

公民之家：由一些被选出来的“公民”组成，他们通过“追溯性公共物品资助”（Retro Funding）来奖励那些为社区做出贡献的人，比如开发公共工具或服务。

2、运作工具和流程：
用智能合约投票；在Optimism治理门户网站上操作；在论坛和Discord上讨论想法。

------------

以太坊：
去中心化的区块链平台。
1、核心功能：
加密货币：以太币，ETH，用来支付交易费用。
智能合约：可以写代码放到以太坊上，这些代码会自动运行。
2、每笔交易或代码都要记录在一个区块链上，靠“共识机制”，全世界节点一起验证。以前用“工作量证明”（PoW,矿工挖矿），现在改成了“权益证明”（PoS，用ETH质押来验证）。

常见的Layer2类型：（即昨天学的L2）
1、Rollups（卷叠）：把很多交易卷成一个包，一次性提交到以太坊。
Optimistic Rollups(乐观卷叠）：假设交易全对，有问题再查。
ZK-Rollups(零知识卷叠）：用数学证明（零知识证明）直接验证交易，效率更高，比如zkSync。
2、状态通道：两个人私下交易，最后把结果上链，像闪电网络。
3、侧链：独立的小区块链，偶尔跟以太坊同步，比如Polygon。



### 2025.04.02
尝试搭建测试链。
————————————————————————————————————————
环境准备：
一、设置MetaMask钱包：用于管理加密货币和区块链应用程序交互的工具。主要功能：
1、数字资产管理：MetaMask允许创建和管理以太坊钱包地址，存储ETH和其他兼容的代币。可以通过它查看余额、发送和接受加密货币。
2、连接去中心化应用：它可以充当用户和以太坊区块链之间的桥梁。可以直接在浏览器中访问去中心化金融、NFT市场、区块链游戏等应用，无需运行完整 的区块链节点。
3、交易签名：当使用DApps时，MetaMask会提示签署交易，确保交易安全且经过授权。
4、私钥管理：MetaMask生成并加密存储私钥。

二、在alchemy获取一个Sepolia的URL
https://dashboard.alchemy.com/apps/pyufo040qhtoluul/networks

三、在MetaMask中添加Sepolia测试网络：
以太坊的一个公共测试网络。可以隔离主网资产，确保真是ETH和资产不会被意外用于测试，避免误操作导致资金损失。
网络名称：Sepolia 
RPC URL：https://eth-sepolia.g.alchemy.com/v2/2yl2tmjTsINyYC34saJo0BYbn_ytz9t-（ALCHEMY）
链 ID：11155111
货币符号：ETH
区块浏览器 URL：https://sepolia.etherscan.io

四、使用Sepolia测试网水龙头（Faucet）获取SepoliaETH，我选择的是alchemy
https://www.alchemy.com/faucets/ethereum-sepolia

五、安装Git



### 2025.04.03
了解了一下Avalanche技术和它现在的应用场景。



### 2025.04.04
继续尝试搭建测试链。
六、安装go
通过官网下载windows安装包

七、安装just
先安装scoop:
我把scoop安装在了D盘，所以先在终端中设置了环境变量：
PS C:\Users\U> $env:SCOOP='D:\Scoop'                                                                                    PS C:\Users\U> [environment]::SetEnvironmentVariable('SCOOP', $env:SCOOP, 'User')  
用国内镜像安装scoop:
 iwr -useb https://gitee.com/glsnames/scoop-installer/raw/master/bin/install.ps1 | iex

 用scoop安装just:终端：
 scoop install just

--------------------------------

1、在D盘新建文件夹，专门用来跑Optimism链。

2、在终端跑： F:\programming\OptimismTest> git clone https://github.com/ethereum-optimism/optimism.git：
下载代码，这里我下载得很慢且老是失败，找到的加速方法：
根据科学上网工具端口（我是clash）配置git代理：
查看端口，我的：HTTP/HTTPS 代理端口：7899
终端：
# 设置全局 HTTP/HTTPS 代理
git config --global http.proxy http://127.0.0.1:7899
git config --global https.proxy https://127.0.0.1:7899

验证代理是否生效
git config --global --get http.proxy  # 查看 HTTP 代理
git config --global --get https.proxy # 查看 HTTPS 代理
正常会返回 http://127.0.0.1:7899 等配置信息。

git clone https://github.com/ethereum-optimism/optimism.git

取消代理（如需恢复）
git config --global --unset http.proxy
git config --global --unset https.proxy


3、GIT BASH：cd optimism

问题：npm install这步没成功，明天再看看。


### 2025.04.05
继续配置环境：
<del>
1.克隆op-deployer仓库
**在终端中运行：**
```bash
# Clone the repository
$git clone https://github.com/ethereum-optimism/op-deployer.git
# Change directory
$cd op-deployer
```
直接运行失败了。
</del>


~~2.报错：GitHub 取消了密码方式的 HTTPS 认证支持
解决方法：使用 SSH 克隆~~
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
~~一路回车即可（直接安装在C盘，建议不要换盘，因为GIT会去C盘找；可以不设密码），生成 .ssh/id_ed25519 和 .ssh/id_ed25519.pub
打开公钥文件 .ssh/id_ed25519.pub，复制里面内容。
登录 GitHub，打开：
👉 https://github.com/settings/keys
点击 “New SSH key”，粘贴进去保存。
然后使用 SSH 地址来克隆：~~
```bash
git clone git@github.com:ethereum-optimism/optimism.git
```

做到这一步发现op-deployer是包含在optimism里面的，也就是说两天前我已经下载过一次了……但既然写都写了……于是就把上面的步骤都划线划掉了……-_-||


1.进入到op-deployer
```bash
cd op-deployer
```

2.安装依赖
```bash
go env -w GOPROXY=https://goproxy.cn,direct # 将 Go 模块（Go Modules）的下载代理设置为国内镜像源（七牛云 goproxy.cn），以加速依赖下载并避免因网络问题导致的失败
go mod tidy
```

3.进入具体程序目录
```bash
cd cmd/op-deployer
```

4.编译程序
```bash
go build
```
成功后，可以在目录中看到一个名为op-deployer.exe的可执行文件

5.查看帮助：
```bash
./op-deployer --help
```
输出：
```bash
NAME:
   op-deployer - Tool to configure and deploy OP Chains.

USAGE:
   op-deployer [global options] command [command options]

VERSION:
   v0.0.0-dev

COMMANDS:
   init       initializes a chain intent and state file
   apply      applies a chain intent to the chain
   upgrade    upgrades contracts by sending tx to OPCM.upgrade function
   bootstrap  bootstraps global contract instances
   inspect    inspects the state of a deployment
   clean      cleans up various things
   verify     verifies deployed contracts on Etherscan
   help, h    Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --cache-dir value   Cache directory. If set, the deployer will attempt to cache downloaded artifacts in the specified directory. (default: "C:\\Users\\U/.op-deployer/cache") [%DEPLOYER_CACHE_DIR%]
   --log.level value   The lowest log level that will be output (default: INFO) [%DEPLOYER_LOG_LEVEL%]
   --log.format value  Format the log output. Supported formats: 'text', 'terminal', 'logfmt', 'json', 'json-pretty', (default: text) [%DEPLOYER_LOG_FORMAT%]
   --log.color         Color the log output if in terminal mode (default: false) [%DEPLOYER_LOG_COLOR%]
   --log.pid           Show pid in the log (default: false) [%DEPLOYER_LOG_PID%]
   --help, -h          show help
   --version, -v       print the version
```
------------------------------------------

实验：
一、准备L1网络：
op-deployer 需要连接到一个 L1 网络（例如 Ethereum 测试网或本地模拟网络）。
为了学习，我们可以使用一个本地 Ethereum 节点（我选择了Hardhat）：

1.安装Hardhat:
```bash
npm install -g hardhat
```

2.将npm切换为国内镜像
```bash
npm config set registry https://registry.npmmirror.com
```

3.在 op-deployer 目录中集成 Hardhat：
按提示安装依赖
```bash
 npm install hardhat @nomicfoundation/hardhat-toolbox
```

4.初始化 Hardhat 项目
```bash
npx hardhat init
```
选择 Create a JavaScript project

5.启动本地网络
```bash
npx hardhat node
```
这会启动一个本地开发链，默认地址为 http://127.0.0.1:8545，并输出 20 个测试账户和私钥。
Hardhat 默认配置使用 127.0.0.1（本地地址）作为主机，8545 作为以太坊节点的常用端口。这是为了在本地开发环境中提供一个快速且私有的区块链节点。



### 2025.04.06
今天得知op stack本地部署最好不要用windows系统，而应该用unix虚拟机……  

一、下载virtualbox和ubuntu。  
虚拟电脑内存12288MB，硬盘30GB，显存64。














### 2025.07.12
<!-- Content_END -->
