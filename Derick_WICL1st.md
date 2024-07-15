---
timezone: Asia/Shanghai
---



# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

- Hi, I'm Derick, a software development engineer specializing in backend architecture design and project management. In my work, I primarily code in Golang and C#. I'm also familiar with Solidity and can develop simple smart contracts.
- I'm participating in this Web3 URL collaborative learning activity to deepen my understanding of Web3 technologies. My goal is to apply what I learn here to create a demo project.
- I'm looking forward to expanding my knowledge and skills in the Web3 space, and I'm excited about the opportunity to collaborate with fellow learners on practical applications of these cutting-edge technologies.

2. **组队期待：**

   XXX [ 包括你想预计的项目参与或开发方向、需要什么角色的小伙伴、其它你想在这里分享的想法，具体组队可在电报频道群沟通 ]

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   XXX [ Yes 100% or Maybe xx% ]

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

#### EIP-4804
- ERC-4804, also known as "Web3 URL to EVM Call Message Translation," is an Ethereum Improvement Proposal that defines a standard for a new type of URL specifically designed for the Ethereum network. It's important to clarify that ERC-4804 has actually been merged into the EIPs as EIP-4804.

- Here's a breakdown of EIP-4804:

**Goal**: Create a decentralized equivalent to the familiar HTTP protocol used on the web. EIP-4804 aims to enable users to directly access content stored on the Ethereum blockchain and compatible blockchains (like Polygon) through user-friendly URLs.
**Web3 URLs**: EIP-4804 introduces the concept of Web3 URLs. These URLs follow a similar format to standard web URLs (http://) but use the prefix "web3://". They can also leverage readable names from ENS (Ethereum Name Service) instead of complex wallet addresses for improved readability.
**Translation to EVM Calls**: The core function of EIP-4804 is to translate a Web3 URL into an EVM call message. This message specifies the smart contract address and the function (method) to be called on the blockchain to retrieve the desired content.
**Benefits**: EIP-4804 offers several advantages:
**Direct Interaction**: Users can directly interact with on-chain content without relying on centralized servers or proxies.
Improved User Experience: Web3 URLs provide a familiar and user-friendly way to access blockchain data.
**Interoperability**: The standard is designed to work with other URI-compatible technologies like SVG.
Decentralized Presentation Layer: EIP-4804 lays the groundwork for a decentralized presentation layer on Ethereum. This could allow for on-chain rendering of web content in the future.
Current Status:

- EIP-4804 is still under development, but it has been merged into the official EIPs.  While not yet fully implemented in all wallets and applications, it represents a significant step towards a more user-friendly and accessible Ethereum ecosystem.
#### EIP-6860

- EIP-6860, or ERC-6860, is an Ethereum Improvement Proposal that aims to introduce a decentralized presentation layer for the Ethereum Virtual Machine (EVM) Base 4804. This essentially means it creates a way to show human-readable content on the blockchain.

- Here's how it works:

**Web3 URLs**: ERC-6860 utilizes Web3 URLs, which are similar to regular web URLs (like http://) but specifically designed for the Ethereum network. These URLs can use readable names from naming services instead of complex wallet addresses for better user experience.
**EVM as a backend**: With ERC-6860, any web content, including HTML, CSS, images, and more, can be translated into EVM (Ethereum Virtual Machine) compatible messages. This allows the EVM to act as a decentralized backend for web applications.
**Decentralized Presentation**: By enabling on-chain rendering of web content, ERC-6860 facilitates a decentralized presentation layer. This means the content isn't reliant on any centralized servers and can potentially be more resistant to censorship.

- 一种在http/https协议之外的一种新的协议，web3://协议，这个协议是为了让用户可以直接访问以太坊区块链上的内容，而不是通过中心化的服务器或代理。要重写dns为ens，将数据内容存储在便宜的l2，回调协议，将web3://协议转换为evm调用消息，这个消息指定了智能合约地址和要在区块链上调用的函数（方法）来检索所需的内容。
- 学习了这两个协议，就看web3://的具体实现
- 做了一个专用的浏览器，希望其他主流浏览器能兼容这个协议
- 将vb的个人博客40m上传到L2，存储费用为0.13E

[官网](https://web3url.io/#/)
[测试合约](https://etherscan.io/token/0x892848074ddea461a15f337250da3ce55580ca85#readContract)
[分享PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g26637866a4a_0_10)
[现有Demo](https://github.com/ethstorage/awesome-web3)
- 作业是进行一些技术上的探索
* 直接感觉是如果存储无法降到普通人能接受的价格，那这个将不可能推广成功
- 

### 07.16

XXX

### 07.17

XXX
<!-- Content_END -->
