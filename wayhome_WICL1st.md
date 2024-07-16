# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   wayhome, IT 老兵一枚，什么都懂一点儿，对 Web3 一直略有了解，但没有特意学习过，希望能借这个机会系统学习下

2. **组队期待：**


   对 Defi 方向的项目比较感兴趣


3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   Maybe 60%

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

- 今日学习时间：1h
- 学习内容小结：
  * 阅读 eip-4804 和 web3 url docs
    - web3 url 为以太坊上的资源定义唯一标识，类似亚马逊的 arn 定义唯一标识 aws 资源
    - 提供 http 的兼容，以方便现有 web2 用户最低成本迁移，类似于一种 web 2.5 的方案
    - 缺乏对安全性的考虑
    - 工作原理
      ![img](https://web3url.io/img/work.e14cc70c.png)
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）



### 07.16

- 今日学习时间：1h
- 学习内容小结:
  *  阅读 eip-6860 和 web3 url docs
    - web3 url 的基本形式 `web3URL         = schema "://" [ userinfo "@" ] contractName [ ":" chainid ] pathQuery`
        - userinfo 表示调用 EVM 的用户，即 EVM 调用消息中的“From”字段
        - contractName 表示要调用的合约，即 EVM 调用消息中的“To”字段
            - 如果是一个地址，则将其用于“To”字段
            - 否则则是来自域名服务的域名，必须解析为一个地址才能用于“To”字段
        - chainid 指示要解析 contractName 并调用消息的链
        - 自动模式下的 path 格式:  `/<methodName>/<methodArg1>/<methodArg2>/...[?returns=(<type1>,<type2>,...)]`
            - `<methodName>` 是要调用的函数方法的名称
            - `methodArg` 是具有 `[<type>!]<value>` 语法的方法的一个参数
            - `?returns=` 指定方法返回签名
    - web3 客户端
        - https 网关
        - evm 浏览器
        - chrome 插件
        - web3 沙箱
        - web3curl 类似 curl 的命令行

### 07.17

XXX
<!-- Content_END -->
