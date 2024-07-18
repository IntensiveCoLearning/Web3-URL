# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ Oscar ]

1. **自我介绍：**
   Oscar，a eco-lifelong learner，懂点技术的产品或运营角色。
   - 非常喜欢以开源的方式残酷共学，和更多的 LXer 学习交流。
   - 之前有深入学习过 Nostr 协议，想认真学一下以太坊里的 Web3:// 协议，了解协议背后设计的思路，及基于协议如何更好构建围绕 EVM 具体的生活 dApps。
   
2. **组队期待：**
   预计参与：产品设计，写 PRD ，配合 coding，具体 idea 还在构建中，和聊的来的小伙伴看看做一个有意思的基于 Web3:// 的实用项目，Just do it。
   
3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**
   100%

---

## 第 1 期共学时间计划

- **7 月 8 日 - 7 月 14 日**：

  - 自我介绍：大家按要求更新上方自我介绍，方面大家互相了解，及后续自由组队方向。
  -  [Web3 URL 残酷共学频道](https://t.me/LXDAO/8748)报道：大家可以自由在残酷共学群里交流分享，互动答疑，根据自身学习阶段情况随时开启自由组队。
  - 课前学习：了解残酷共学流程，GitHub 协作共学基础；Web3:// 协议课前学习。

- **7 月 15 日 - 7 月 21 日**：

  - **7 月 15 日 周一晚 8 点- 9 点（北京时间）：** 第 1 次公开课分享
  - **本周共学内容：** 涉及 Web3://  的背景和演进历史；支持 Web3://  协议的访问方式 (gateway 和 EVM browser)来浏览以太坊上面的数据；熟悉使用 Web3://  和 EthStorage 早期测试网来部署简单的去中心化网站。
  - **Homework1：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

- **7 月 22 日 - 7 月 28 日**
  - **7 月 22 日 周一晚 8 点- 9 点（北京时间）：** 第 2 次公开课分享
  - **本周共学内容：** 涉及 Web3://  高级开发工具，包括：在命令行通过 web3curl 来通过 Web3://  协议下载数据，通过 ethfs-uploader 批量上传网页数据，通过 manual 模式来搭建去中心化多人交互全链网站；及深入理解以太坊的存储模型和 gas 开销等。
  - **边学边用实战开发：** 根据组队情况自由安排。
  - **Homework2：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

- **7 月 29 日 - 8 月 4 日**
  - **7 月 29 日 周一晚 8 点- 9 点（北京时间）：** 第 3 次公开课分享
  - **本周共学内容：** 涉及实际应用案例分享及未来以太坊基础设施在 Web3://  的重要作用及开发方向等。
  - **边学边用实战开发：** 根据组队情况自由安排。
  - **结营分享：** 具体时间及详情另在「Web3 URL 残酷共学频道」通知。

---

## 笔记证明 Notes Proof

<!-- Content_START --> 

### 07.15
- 今日学习时间：2 小时
- 学习内容小结：
  - Web3://  的[背景和历史](https://docs.web3url.io/vision/background)学习：尽管在协议层面向去中心化转变，但许多去中心化应用（dApps）仍依赖于中心化组件，如服务器或网络服务提供商（NSP）。
  - [解决方案](https://docs.web3url.io/vision/our-solution)旨在取代 Web2 集中化瓶颈：设计思路学习
    ![web3url_design](img/web3url_design.png)
    - 专用的以太坊侧链，支持 EVM 和高效的二进制大对象（BLOB）存储，将取代传统的客户端/服务器模型。
    - 采用 Web3 风格的 URL 标准，替代传统的 DNS/URL 方案。
    - 作为轻客户端的 Web 浏览器扩展，通过 web3 URL 执行 EVM 调用，将成为去中心化的 HTTP 。
  
- 第一次公开课部分
  - 对什么是 "web3://" 访问协议？Why  "web3://“？How to Use web3: //? How to Access EVM with web3:// ？ 有了初步的认识和理解。
  - 目前安装火狐浏览器下载了 [Firefox extension]( https://addons.mozilla.org/en-US/firefox/addon/web3url/) 进行体验，使用 Native browser support 体验，具体背后调用逻辑还待学习。
- Homework 部分 
  - 暂无

- Question and Ideas
  - 在想基于web3:// 哪些应用场景是当前最需要的或频率最高的？

### 07.16

- 今日学习时间：2 小时

- 学习内容小结：
  - 学习了解以太坊改进提案 [EIP-4804](https://eips.ethereum.org/EIPS/eip-4804) 和  [EIP-6860](https://eips.ethereum.org/EIPS/eip-6860)：
    - ERC-4804，也称为“Web3 URL到EVM调用消息转换”，旨在为以太坊网络定义一种新的 URL 类型的标准。
    -  EIP-6860，旨在为以太坊虚拟机（EVM）Base 4804 引入一个去中心化的呈现层。
    
  - 通过访问 `web3://cyberbrokers-meta.eth/renderBroker/5`跳转 https://cyberbrokers-meta.w3eth.io/renderBroker/5 学习了解背后数据是如何被调用及被呈现。
  
    - 根据请求的网络对象位置（如以太坊或其他区块链）将请求分发到不同的 Gateway
  
    - Gateway 通过调用 ENS 把 cyberbrokers 所映射的合约地址来去定位。🤔
  
      ![cyberbrokers](img/cyberbrokers.png)
  
  - 回顾 [公开课](https://www.youtube.com/watch?v=hmN77o-ex8I) 学习，尤其是 QA 环节。我们需要一个协议保证「去中心定位去中心化的资源」。一个是如何定位的问题，一个是如何访问的问题。
  
  - 对目前具体的 Application 方向进行了了解，面临一些具体问题：目前很多浏览器不兼容，存储费用过高等。
  
- Homework 部分 
  - 暂无
  
- Question and Ideas
  - 并不是所有的东西都需要去中心化，去中心和中心化如何平衡？

### 07.17

- 今日学习时间：1 小时
- 学习内容小结：
- Homework 部分 完成前 2 个
  - Find the ownership of an your favor NFT
    - 使用Firefox Extension访问：web3://moon-birds-xyz.eth/render/108
      - 跳转到：https://moon-birds-xyz.w3eth.io/render/108
        - web3-chain-id: 1
        - web3-cname: moon-birds-xyz.w3eth.io
        - web3-contract-address：0x56B9308EFd014f10423B42B3aDE7eeCFe128B1BD
          - ENS Name Tag：[web3url.eth](https://etherscan.io/address/0xbff45643d3af697a178ac671212e284a7f86cdae)
          - Contract Source Code (Solidity):  查看 render 方法
  - Find the balance of an account in an ERC-20 contract (USDC / USDT)
    - 使用Firefox Extension访问：web3://usdc.eth/balanceOf/vitalik.eth?returns=(uint256)
      - 跳转到：https://usdc.w3eth.io/balanceOf/vitalik.eth?returns=(uint256)
        - web3-chain-id：1
        - web3-cname：usdc.w3eth.io.
        - web3-contract-address：0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
        - web3-host-domain-name-resolver：ens
        - web3-mode-auto-method：balanceOf
        - ![web3-mode-auto-method](/Users/luffythinker/Web3-URL/img/web3-mode-auto-method.png)


- Question and Ideas
  - token-address：`0x52284158e02425290f6b627aeb5fff65edf058ad` 和contract-address：`0x56B9308EFd014f10423B42B3aDE7eeCFe128B1BD` 之间的连接关系🤔



<!-- Content_END -->
