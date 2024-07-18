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
- 学习时间：1h
- 学习内容小结：看[文档](https://docs.web3url.io/web3-url-structure/resolve-mode)
- 总结
#### 总结 Web3 URL 结构中的解析模式

##### 概述

Web3 URL 的解析模式（Resolve Mode）是 Web3 URL 结构的一部分，用于确定如何解析和访问资源。解析模式定义了在不同环境下如何处理和解释 Web3 URL，以确保资源的正确定位和访问。

###### 解析模式的定义

解析模式主要包括以下几种：

1. **自动模式（Auto Mode）**：
   - **描述**：自动模式根据上下文环境自动选择最合适的解析方法。
   - **应用场景**：适用于用户不需要或不希望手动选择解析方法的情况。

2. **手动模式（Manual Mode）**：
   - **描述**：手动模式允许用户明确指定解析方法。
   - **应用场景**：适用于高级用户或特定应用场景，需要精确控制解析过程。

3. **特定模式（Specific Mode）**：
   - **描述**：特定模式根据特定的协议或标准进行解析。
   - **应用场景**：适用于需要遵循特定协议或标准的应用场景。

##### 解析模式的选择依据

选择解析模式时，需要考虑以下因素：

1. **用户需求**：
   - 自动模式适合一般用户，提供简化和自动化的体验。
   - 手动模式适合高级用户，提供更高的控制和灵活性。

2. **应用场景**：
   - 在需要遵循特定协议或标准的场景下，特定模式是最佳选择。
   - 在不确定的环境或需要灵活应对的场景下，自动模式更为适用。

3. **技术环境**：
   - 不同的技术环境可能对解析模式有不同的要求，选择适合当前环境的解析模式可以提高效率和准确性。

##### 解析模式的实现

解析模式的实现需要考虑以下技术细节：

1. **上下文感知**：
   - 自动模式需要具备上下文感知能力，能够根据环境自动调整解析方法。
   - 这需要对环境信息进行实时分析和判断。

2. **用户交互**：
   - 手动模式需要提供用户友好的界面，允许用户方便地选择和切换解析方法。
   - 这需要设计直观的用户界面和交互流程。

3. **协议支持**：
   - 特定模式需要支持多种协议和标准，确保在不同协议下都能正确解析和访问资源。
   - 这需要对各种协议的深入理解和实现。

##### 结论
Web3 URL 结构中的解析模式提供了灵活和多样的资源解析方法，满足了不同用户和应用场景的需求。通过合理选择和实现解析模式，可以确保资源的正确定位和高效访问。自动模式适合一般用户和不确定环境，手动模式适合高级用户和特定需求，特定模式适合遵循特定协议的应用场景。理解和应用这些解析模式，可以提升 Web3 应用的用户体验和技术性能。

### 07.17
今天学习了协议的基本组成结构
1. Web3 URL的基本结构：
   Web3 URL由三个主要部分组成：协议、域名和路径。

2. 协议部分：
   - 使用"w3://"作为Web3 URL的协议标识符。
   - 也支持使用"https://"作为替代，以便与传统Web浏览器兼容。

3. 域名部分：
   - 可以使用传统域名（如example.com）或去中心化域名（如example.eth）。
   - 支持多种去中心化域名系统，包括ENS、Unstoppable Domains等。

4. 路径部分：
   - 用于指定具体的资源位置。
   - 可以包含子目录、文件名等信息。

5. 查询参数：
   - 使用"?"后跟键值对来添加额外的参数信息。
   - 多个参数之间用"&"分隔。

6. 片段标识符：
   - 使用"#"后跟标识符来指向文档的特定部分。

7. 示例：
   文档提供了几个Web3 URL的示例，展示了不同组件的组合使用。

8. 兼容性：
   - Web3 URL设计考虑了与现有Web基础设施的兼容性。
   - 支持使用"https://"协议，便于在传统浏览器中使用。

9. 灵活性：
   Web3 URL结构设计灵活，可以适应各种去中心化网络和应用场景。

总的来说，Web3 URL结构保留了传统URL的基本形式，同时引入了对去中心化网络的支持，为Web3应用提供了一个统一的资源定位方式。这种设计既考虑了新技术的需求，又保持了与现有Web生态系统的兼容性。
### 07.18

<!-- Content_END -->
