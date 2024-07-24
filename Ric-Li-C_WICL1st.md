---
timezone: Asia/Shanghai
---

# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为 WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ Ric Li C ]

1. **自我介绍：**

    Ric Li C, 家庭主夫，天天在家带 2 个女儿，自学了 Solidity，NextJS，TypeScript，前一段时间在 BSC 链上，发行了个人的半慈善性质的 NFT 项目：MAS Awareness (http://mas-awareness.top)。

2. **组队期待：**

    对 web3 protocol 不太了解，但是很感兴趣，暂时没有具体项目的想法；个人比较擅长后端，不太擅长前端，如果组队，希望找擅长前端的小伙伴。

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

    Yes 75%

---

## 第 1 期共学时间计划

-   **7 月 8 日 - 7 月 14 日**：

    -   自我介绍：大家按要求更新上方自我介绍，方面大家互相了解，及后续自由组队方向。

    -   [Web3 URL 残酷共学频道](https://t.me/LXDAO/8748)报道：大家可以自由在残酷共学群里交流分享，互动答疑，根据自身学习阶段情况随时开启自由组队。

    -   课前学习：了解残酷共学流程，GitHub 协作共学基础；Web3:// 协议课前学习。

-   **7 月 15 日 - 7 月 21 日**：

    -   **7 月 15 日 周一晚 8 点- 9 点（北京时间）：** 第 1 次公开课分享
    -   **本周共学内容：** 涉及 Web3:// 的背景和演进历史；支持 Web3:// 协议的访问方式 (gateway 和 EVM browser)来浏览以太坊上面的数据；熟悉使用 Web3:// 和 EthStorage 早期测试网来部署简单的去中心化网站。
    -   **Homework1：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

-   **7 月 22 日 - 7 月 28 日**

    -   **7 月 22 日 周一晚 8 点- 9 点（北京时间）：** 第 2 次公开课分享

    -   **本周共学内容：** 涉及 Web3:// 高级开发工具，包括：在命令行通过 web3curl 来通过 Web3:// 协议下载数据，通过 ethfs-uploader 批量上传网页数据，通过 manual 模式来搭建去中心化多人交互全链网站；及深入理解以太坊的存储模型和 gas 开销等。
    -   **边学边用实战开发：** 根据组队情况自由安排。
    -   **Homework2：** 见[课程 PPT](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11)。

-   **7 月 29 日 - 8 月 4 日**
    -   **7 月 29 日 周一晚 8 点- 9 点（北京时间）：** 第 3 次公开课分享
    -   **本周共学内容：** 涉及实际应用案例分享及未来以太坊基础设施在 Web3:// 的重要作用及开发方向等。
    -   **边学边用实战开发：** 根据组队情况自由安排。
    -   **结营分享：** 具体时间及详情另在「Web3 URL 残酷共学频道」通知。

---

## 笔记证明 Notes Proof

<!-- Content_START -->

### 07.15

-   今日学习时间：1 小时（公开课）+ 半小时（看 Telegram 群内消息并提问）
-   学习内容小结：参加 2100-2200 的公开课，对 web3:// 有基础的了解
-   Homework 部分：待完成
-   Question and Ideas：存储的费用必须降下来，否则没有实用价值。

### 07.16

-   今日学习时间：1 小时（看 Telegram 群内消息并提问，查看资料，完成部分作业）
-   学习内容小结：学习资料，了解 Auto Mode 和 Manual Mode
-   Homework 部分：

        Find the ownership of an your favor NFT
            web3://0x7bc5d353663c4c94fd022d3df0642b56c174b45c/ownerOf/1?returns=(uint256)
            http://0x7bc5d353663c4c94fd022d3df0642b56c174b45c.w3eth.io/ownerOf/1?returns=(uint256)

-   Question and Ideas：Manual Mode 的合约怎么写

### 07.17

-   今日学习时间：1 小时（看 Telegram 群内消息，查看资料，完成部分作业）
-   学习内容小结：加深对于 web 3 URL 的理解
-   Homework 部分：

        Find the balance of ERC-20 contract (USDC / USDT)
            web3://0xdAC17F958D2ee523a2206206994597C13D831ec7/balanceOf/0xdAC17F958D2ee523a2206206994597C13D831ec7?returns=(uint256)

            http://0xdAC17F958D2ee523a2206206994597C13D831ec7.w3eth.io/balanceOf/0xdAC17F958D2ee523a2206206994597C13D831ec7?returns=(uint256)

            https://www.rapidtables.com/convert/number/hex-to-decimal.html?x=2481C9890F

-   Question and Ideas：得到的结果需要解码，能不能直接得到解码之后的结果

### 07.18

-   今日学习时间：1.5 小时（看 Telegram 群内消息并提问，查看资料，完成部分作业）
-   学习内容小结：Auto Mode 的 ?returns= 怎么写
-   Homework 部分：

        Deploy a contract in auto mode and say “hello world”
            web3://0x117f7b2C45FD86b69268e067654a559B13EcB6Ff:11155111/Hello
            https://0x117f7b2C45FD86b69268e067654a559B13EcB6Ff.11155111.w3link.io/Hello

-   Question and Ideas：Nil

### 07.19

-   今日学习时间：1 小时（看 Telegram 群内消息，查看资料，完成部分作业）
-   学习内容小结：学习如何写 Manual Mode 的智能合约
-   Homework 部分：

        Deploy a contract in manual mode and say “hello world”
            web3://0xE6BD29A25A15367C2D58D638e50cdea581299ACf:97/
            https://0xE6BD29A25A15367C2D58D638e50cdea581299ACf.97.w3link.io/

-   Question and Ideas：evm browser 无法打开 ChainId > 65k 的网络链接

### 07.20

-   今日学习时间：1 小时（看 Telegram 群内消息，查看资料）
-   学习内容小结：研究写 Manual Mode 的智能合约时，怎么写 html 代码
-   Homework 部分：Nil
-   Question and Ideas：写 Manual Mode 的智能合约时，怎么写 html 代码

### 07.21

-   今日学习时间：1 小时（看 Telegram 群内消息，查看其他同学笔记和 Medium 资料）
-   学习内容小结：学习 EIP-4804; 研究写 Manual Mode 的智能合约时，怎么写 html 代码
-   Homework 部分：Nil
-   Question and Ideas：看不懂 EIP-4804，很多疑问

### 07.22

-   今日学习时间：3 小时

        1 小时看 Telegram 群内消息并求 w3q 测试币，查看 EthStorage 资料；
        1 小时参加会议；
        1 小时尝试写含 html 代码的 Manual Mode 的智能合约。

-   学习内容小结：学习 EthStorage 相关
-   Homework 部分：

        Deploy a contract in manual mode (containing HTML codes)
            web3://0x6eecc8c147eb21a83c5f9e4956fbd4575d3ff942:11155111/
            https://0x6eecc8c147eb21a83c5f9e4956fbd4575d3ff942.11155111.w3link.io/
            (The javascript button does not seem to be working, need to look into this)

-   Question and Ideas：尝试把自己的 react project 用 ethfs 上传到 web3url

### 07.23

-   今日学习时间：1 小时（看 Telegram 群内消息并提问，查看资料）
-   学习内容小结：学习 ERC-6944
-   Homework 部分：Nil
-   Question and Ideas：搞清楚 EIP-4804， EIP-5219 和 ERC-6944

### 07.24

-   今日学习时间：1 小时（看 Telegram 群内消息并提问，查看资料）
-   学习内容小结：学习 EthStorage 相关资料
-   Homework 部分：

        Claim EthStorage Testnet tokens - done

-   Question and Ideas：搞清楚如何按照 ERC-6944 写智能合约

<!-- Content_END -->
