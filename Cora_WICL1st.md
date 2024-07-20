# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为 WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   Cora, 前端技术经理，研发 tiktok 数据分析平台。

   参加的主要目的是学习 Web3 相关知识。

2. **组队期待：**

   感兴趣一起组队的可以拉我~

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   YES

---

## 第 1 期共学时间计划

- **7 月 8 日 - 7 月 14 日**：

  - 自我介绍：大家按要求更新上方自我介绍，方面大家互相了解，及后续自由组队方向。

  - [Web3 URL 残酷共学频道](https://t.me/LXDAO/8748)报道：大家可以自由在残酷共学群里交流分享，互动答疑，根据自身学习阶段情况随时开启自由组队。

  - 课前学习：了解残酷共学流程，GitHub 协作共学基础；Web3:// 协议课前学习。

- **7 月 15 日 - 7 月 21 日**：

  - **7 月 15 日 周一晚 8 点- 9 点（北京时间）：** 第 1 次公开课分享
  - **本周共学内容：** 涉及 Web3:// 的背景和演进历史；支持 Web3:// 协议的访问方式 (gateway 和 EVM browser)来浏览以太坊上面的数据；熟悉使用 Web3:// 和 EthStorage 早期测试网来部署简单的去中心化网站。
  - **Homework1：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

- **7 月 22 日 - 7 月 28 日**

  - **7 月 22 日 周一晚 8 点- 9 点（北京时间）：** 第 2 次公开课分享

  - **本周共学内容：** 涉及 Web3:// 高级开发工具，包括：在命令行通过 web3curl 来通过 Web3:// 协议下载数据，通过 ethfs-uploader 批量上传网页数据，通过 manual 模式来搭建去中心化多人交互全链网站；及深入理解以太坊的存储模型和 gas 开销等。
  - **边学边用实战开发：** 根据组队情况自由安排。
  - **Homework2：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

- **7 月 29 日 - 8 月 4 日**
  - **7 月 29 日 周一晚 8 点- 9 点（北京时间）：** 第 3 次公开课分享
  - **本周共学内容：** 涉及实际应用案例分享及未来以太坊基础设施在 Web3:// 的重要作用及开发方向等。
  - **边学边用实战开发：** 根据组队情况自由安排。
  - **结营分享：** 具体时间及详情另在「Web3 URL 残酷共学频道」通知。

---

## 笔记证明 Notes Proof

<!-- Content_START -->

### 07.15

今日学习时间：2h

- 学习内容小结：了解 ppt 内容 Introduction to Web3:// Access Protocol (CoLearning 2024)

### 07.16

今日学习时间：2h

- 学习内容小结：学习[Web3URL 文档](https://docs.web3url.io)部分章节，介绍，背景等。
- web3:// 是一种新协议，用于访问与 EVM 兼容的区块链中智能合约返回的内容。

### 07.17

今日学习时间：2h

- 学习内容小结：学习[Web3URL 文档](https://docs.web3url.io)部分章节，问题，解决方案，例子。
- 问题：dApp 服务器/NSP 是中心化的！这意味着去中心化区块链的好处可以很容易地被打破。
- 解决方案：端到端完全无需信任的去中心化网络。
- 例子：1、完全去中心化的交易所；2、完全去中心化的社交网络。

- 【从生态村到 Web3，乡村为何上 DAO？】分享会学习

### 07.18

今日学习时间：2h

- 学习内容小结：学习[Web3URL 文档](https://docs.web3url.io)部分章节，URL 结构，域名解析，解析模式。
- URL 结构：

```
web3://<contract>[:<chainId>]/<path>
```

    <contract> 可以是合约地址也可以是域名。
    chainId 是可选的，并指示区块链的链 ID，用于查询智能合约的位置。
    path 遵循与传统 HTTP URL 类似的结构

- 域名解析：了解域名解析方式 [web3curl 应用程序](https://github.com/web3-protocol/web3curl-js)
- 解析模式：自动模式；手动模式；资源请求模式。

### 07.19

今日学习时间：2h

- 学习内容小结：学习[Web3URL 文档](https://docs.web3url.io)部分章节，HTTPS 网关，EVM 浏览器，Chrome 扩展程序，Web3:// Sandbox，Web3curl ，Librairies。
- HTTPS 网关：w3eth.io 由 EthStorage 团队提供，是以太坊主网和 ENS 的单区块链公共网关。
- EVM 浏览器：EVM 浏览器是基于 electron/chromium 的基本 Web 浏览器，它通过 web3protocol 库支持 web3:// 该协议。它包括对 Frame.sh 钱包的支持。
- Chrome 扩展程序：尚不安全，无法提供在 Chrome 网上应用店，可手动编译用于项目演示。
- Web3:// Sandbox
- Web3curl：调试
- Librairies

### 07.20

今日学习时间：2h

- 学习内容小结：学习[Web3URL 文档](https://docs.web3url.io)部分章节
- 使用 ethfs-uploader 上传您的第一个文件/文件夹 (失败了)

- 参加 LXDAO 中文社区周会

- <!-- Content_END -->
