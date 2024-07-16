# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

昵称：Kero
职业/擅长：区块链底层开发、区块链基础设施开发
残酷共学 Web3 URL 的原因和期待：Web3 领域需要一个对用户友好的 access protocol 来规范访问链上物品、调用链上合约等行为。这样的协议要足够通用又足够简单和对用户友好，这就需要协议设计者对业界的公链和应用有深刻的理解，并提炼出一套通用的框架。我很想学习 "web3://" 是如何设计协议的。


2. **组队期待：**

我想把这套协议适配到非 EVM 兼容的链，比如 StarkNet、Sui、Aptos、Nervos CKB 等。


3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

Maybe 80%

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

- 今日学习时间：XXXX
- 学习内容小结：XXXX
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）



### 07.16

- 今日学习时间：0.5 hour
- 学习内容小结：What/Why/How to web3://

#### Question and Ideas

  - web3:// scheme 没有包含 gateway 信息，也就是说 gateway 是固定的，这引出了几个疑问：
    - 能够粗浅地理解 gateway service 为一个用于翻译 `web2<->web3` 的 HTTP middleware service？Gateway 需要做到去中心化吗？如果要做到去中心化，web3:// scheme 不包含 gateway 的信息的话要怎么样做到去中心化呢？
    - 用户能否自建 web3:// gateway 呢？如果可以，那 web3 url 应该如何指向自建的 gateway？
    - Web2 世界里有没有类似 web3:// gateway service 这样的存在呢？
  - 对于 render，web3:// 想要扮演什么角色呢？

#### Note

ETHStorage 主要带来了两个产品，ETHStorage 和 Web3-URL。暂时不知道二者之间的联系，比如 Web3-URL 能否不基于 ETHStorage 来使用？

ETHStorage 是一个 L2，Proof of Storage 是 Dynamic Sharding with Proof of Random Access.

Web3-URL is an Access Protocol, defines URL to EVM Call Message Translation - an IANA registered URI scheme, also defines how to render Web objects hosted by smart contracts.

### 07.17

XXX
<!-- Content_END -->
