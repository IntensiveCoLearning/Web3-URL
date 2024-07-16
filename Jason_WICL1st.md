# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   Jason：
   之前主要做人工智能AI相关的算法工作,做的算法方向比较杂，诸如自然语言处理、搜索算法（搜索建议词推荐）以及营销算法（会员转化、分发优惠劵等）。 
   主要想了解 Web3 相关的开发，参与某个全链应用或产品。

2. **组队期待：**

   感兴趣一起组队的可以拉我一个

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   Yes 100%


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

举例示范：

- 今日学习时间：20240715
- 学习内容小结：XXXX
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）



### 07.16
- 今日学习时间：20240716 11：00

- 学习内容小结：
    - On the Future of Web3 — Paving the Way to End-to-End Fully-Decentralized Web by Qi Zhou
        - State of the Art of dWeb
            - ipfs://（decentralized access protocol）：
            - libp2p（decentralized networking layer）：which to retrieve the data
            - filecoin（decentralized incentivized Storage layer）：helps to keep the data consistency
        - limitation of current solutions
            - limited storage semantics(语义学)
            - steep(陡峭的) learning cure
        - futures needed in future web3
            - rich storage semantics
            - simple user onboarding
            - end-to-end fully decentralized
        - solutions to future web3
            - proof of publication via data availability
            - ethstorage: external data retenion(保持) l2 network
                - instead of computation that most l2 work on
                - support both ethereum mainnet and our stoarge-specific sidechain
            - web3:// access protocol
                - ERC-4804: web3 url standard - an IANA Registered Scheme
                    - web3://qizhou.eth@example.eth:333/balanceOf/zuck.eth?returns=(uint256)
                    - scheme: web3
                    - userinfo: qizhou.eth
                    - contract: example.eth
                    - chainid: 333
                    - authority: qizhou.eth@example.eth:333
                    - methodId: balanceOf
                    - arg0: zuck.eth
                    - query: returns=(uint256)
        - applications
            - nft等
    - Introducing web3:// - Decentralized Access Protocol for EVM | ETHDenver 2023
        - web3:// access protocol？
        - why need web3:// access protocol?
            - more and more nfts are moving on chain
                - cyberbrokes
                - nouns
                - moonbirds
                - artbooks
            - narrative(叙事技巧): own both token and image on-chain
            - a missing part of ethereum: no way to render(提供) the object directly.
            - web3:// allows user to browse the images content directly
        - how to use web3://？
            - Inherit most features of http://
                - a decentralized authority(a contract by address or name)
                - a way to call the contract(calldata)
                - (optional) a format to return data
            - check web3url.io for more 
        - how to access evm with web3://?
            - w3eth.io is current gateway for ethereum
            - firefox extension
            - native integration(融合) with modern browsers is underway!
            - w3link.io is the current gateway for multi-chain
            - support networks
                - mainnet(1)
                - goerli
                - sepolia
                - optimism/testnet
                - arbitrum/testnet
        - application: on-chain nft images
            - on-chain nfts - cyberbrokers
        - application: personal website
            - vitalik's blog
            - use ERC5018: filesystem-like interface
            - ethfs-uploader to synchronize folder/files
        - more applications
            - dynamic website with multi-user interactions
                - decentralized blogger、dropbox、email、git、craigslist
            - checkout web3url io
        - storage issue on evm
            - storage cost is super expensive on mainnet
                - 1GB costs ~ 10M dollars 
            - solution with low cost - arbitrum nova with DAC
            - solution with lower cost - ethstorage.io
                - scaling ethereum storage to ~ PB with 1/1000x cost
        - vision on future web3
            - ethereum drives most innovations(创新)
            - omnipresent(无所不在的) to everyone 
            - fully decentralized

- Homework 部分（如果有安排需要填写证明完成）

- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）



### 07.17
- 今日学习时间：20240717 

- 学习内容小结：

- Homework 部分（如果有安排需要填写证明完成）

- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

<!-- Content_END -->
