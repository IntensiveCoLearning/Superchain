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

在这里遇到了虚拟机打不开终端的情况，解决：https://blog.csdn.net/m0_59724528/article/details/128395442


### 2025.04.07
在虚拟机中尝试部署。  

一、
1.打开虚拟机终端，切换到root:  
更新系统并安装一些必备工具：
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl wget git build-essential lsb-release ca-certificates software-properties-common
```

2.安装nvm
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.2/install.sh | bash      # 从nvm的github获取
source ~/.bashrc       # 刷新终端环境
nvm --version     # 验证安装
```

3.安装当前最新的长期支持（LTS）版本的 Node.js
```bash
nvm install --lts
```

4.使用已安装的 LTS 版本
```bash
nvm use --lts
```

5.确认安装成功
```bash
node -v
npm -v
```

二、安装 Docker 和 Docker Compose   

参考文档：https://yeasy.gitbook.io/docker_practice/install/ubuntu

1.安装一些基础软件包，确保系统支持 HTTPS 源和密钥管理
```bash
sudo apt install -y apt-transport-https ca-certificates gnupg
```

2.下载 Docker 官方的 GPG 密钥并转换为二进制格式，存放到 /usr/share/keyrings/
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

3.动态生成 Docker 的 APT 源配置，基于当前系统的架构（如 amd64）和 Ubuntu 版本（如 focal、jammy）
```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://mirrors.aliyun.com/docker-ce/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

4.更新 apt 软件包缓存，并安装 docker-ce
```bash
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
```

6.将当前用户添加到 docker 组，允许非 root 用户运行 Docker 命令
```bash
$ sudo groupadd docker
$ sudo usermod -aG docker $USER    # $USER 是当前登录的用户名
```
直接退出当前终端再重新登录或者执行：
```bash
newgrp docker

```

三、~~修改 Ubuntu 虚拟机中的 DNS 设置，配置 8.8.8.8 和 1.1.1.1。使 Docker 就能更顺畅地联网。~~ 这种方法失败了！见四

1.~~打开终端，先检查一下当前 DNS 设置~~
```bash
cat /etc/resolv.conf
```
看看输出中有没有 nameserver 的设置，比如：
```bash 
nginx
nameserver 127.0.0.53
```
这说明系统用的是 systemd-resolved，我们可以暂时覆盖它。

2.~~编辑 resolv.conf 文件~~
```bash
sudo nano /etc/resolv.conf
```
在打开的编辑器中，删除原来的内容，然后粘贴以下两行
```bash
nameserver 8.8.8.8
nameserver 1.1.1.1
```
按下：

Ctrl + O 保存

Enter 确认文件名

Ctrl + X 退出编辑器


3.防止系统自动还原 /etc/resolv.conf
```bash
sudo chattr +i /etc/resolv.conf
```
如果这步报错，更改输入：
```bash
# 1. 删除原来的符号链接
sudo rm /etc/resolv.conf

# 2. 新建 resolv.conf 并写入 DNS 配置
echo -e "nameserver 8.8.8.8\nnameserver 1.1.1.1" | sudo tee /etc/resolv.conf

# 3. 上锁防止被覆盖
sudo chattr +i /etc/resolv.conf
```

四、通过代理（我使用的是 Clash Verge ）让 Ubuntu 虚拟机联网

1.确认 Clash Verge 配置




查看 Clash Verge 的系统托盘图标或界面，找到 HTTP 端口（我是7899）。打开“局域网连接”选项。

2.virtualbox网络选择NAT。

3.在 Ubuntu 内部配置代理  
可参考这篇文档：https://yeasy.gitbook.io/docker_practice/advanced_network/http_https_proxy  
为 dockerd 创建配置文件夹
```bash
sudo mkdir -p /etc/systemd/system/docker.service.d
```
为 dockerd 创建 HTTP/HTTPS 网络代理的配置文件，文件路径是 /etc/systemd/system/docker.service.d/http-proxy.conf 。
```bash
sudo mkdir /etc/systemd/system/docker.service.d/http-proxy.conf
```
并在该文件中添加相关环境变量。需要注意，此处：192.168.234.1要用主机IPV4地址代替；7899：看1.中 clash verge 的 http 代理地址。
```bash
[Service]
Environment="HTTP_PROXY=http://192.168.234.1:7899/"
Environment="HTTPS_PROXY=http://192.168.234.1:7899/"
Environment="NO_PROXY=localhost,127.0.0.1"
```
按下：

Ctrl + O 保存

Enter 确认文件名

Ctrl + X 退出编辑器


4.刷新配置并重启 docker 服务
```bash
sudo systemctl daemon-reload
sudo systemctl restart docker
```

5.测试 Docker 是否安装正确
```bash
docker run --rm hello-world
```
如果出现下面的内容，则成功：
```bash
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
b8dfde127a29: Pull complete
Digest: sha256:308866a43596e83578c7dfa15e27a73011bdd402185a84c5cd7f32a88b501a24
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```


### 2025.07.12
<!-- Content_END -->
