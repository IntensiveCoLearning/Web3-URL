---
timezone: Asia/Shanghai
---

# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ Ziicu Tang ]

1. **自我介绍：**

   Ziicu，擅长前端和产品，目前带团队做企业内部应用，对web3比较感兴趣，这次参加是因为去年一起合作一个ordinals项目的朋友推荐的，希望能借此对web3更为了解。

2. **组队期待：**

   目前web3没有组队，暂时没有太多想法，希望能被其他团队需要。

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   目标完成70%，争取100%完成

---

## 第 1 期共学时间计划

- **7 月 8 日 - 7 月 14 日**：

  - 自我介绍：大家按要求更新上方自我介绍，方面大家互相了解，及后续自由组队方向。

  - [Web3 URL 残酷共学频道](https://t.me/LXDAO/8748)报道：大家可以自由在残酷共学群里交流分享，互动答疑，根据自身学习阶段情况随时开启自由组队。

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

- 今日学习时间：2h
- 学习内容小结：
  - 简单了解什么是web3://协议
  - web3://协议对应的ERC-4804、ERC-6860(进行中)
  - 标准格式：scheme://userinfo@contract:chainid/methodId/arg0?query
    例如：web3://qizhou.eth@xxx.eth:4804/balanceOf/zuck.eth?returns=(unit256)
  - 为什么使用web3:// ，提供一种去中心化的方式直接访问需要资源，目前还需要特定的浏览器支持，例如：[evm-broweser](https://github.com/nand2/evm-browser)。
  - 应用场景：NFT图片资源、blog

- [第一期公开课程视频](https://youtu.be/hmN77o-ex8I)

- 其他资源：
  - [web3://](https://web3url.io/#/)
  - [realtime token price](https://0xccd58c48f12dd1d08250197cb0d8b865bda02064.3333.w3link.io/index.html)
  - [web3url doc](https://docs.web3url.io/)

- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.16

- 今日学习时间：1h
- 学习内容小结：
  - 体验gateway的访问方式体验web3 url定位的资源
  - 研究Web3URL Docs中 ***Fetch an USDC balance 案例*** 中的智能合约（0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48）。

### 07.17

- 今日学习时间：1h
- 学习内容小结：
  - 阅读Web3URL Docs中 客户端部分的介绍

支持五种方式：[Https网关](https://github.com/ethstorage/web3url-gateway)、[EVM浏览器](https://github.com/nand2/evm-browser)、[Chrome插件](https://github.com/ComfyGummy/chrome-web3)、[Web3Url沙箱](https://github.com/ComfyGummy/chrome-web3)以及[web3curl](https://github.com/web3-protocol/web3curl-js)

其中个人觉得[web3curl](https://github.com/web3-protocol/web3curl-js)方便开发者调试（It can be very useful to help debugging URLs.）

#### 安装

***（我这安装时会报3个严重错误，不知道项目方是否注意到了）***

```bash
npm install -g web3curl
```

#### 使用

```bash
web3curl "web3://w3url.eth"
```

使用 -v 选项可以获取更多执行细节。 使用 -vv 和 -vvv 可以获得更多输出。 -vvv 将添加有关名称解析过程的信息，而 -vvvv 将添加智能合约发送和接收的全部字节。

```bash
web3curl -v "web3://w3url.eth"
web3curl -vv "web3://w3url.eth"
web3curl -vvv "web3://w3url.eth"
```

按官网提供的两个例子分别获取NFT信息和USDC余额时，感觉NFT这类文件信息用web3curl还是不太方便，如果调试返回的是字符串之类的资源，还是方便，自己可以试一下：

```bash
# Get a NFT
web3curl 'web3://0x4e1f41613c9084fdb9e34e11fae9412427480e56/tokenHTML/9352'

# Fetch an USDC balance
web3curl 'web3://0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48/balanceOf/nemorino.eth?returns=(uint256)'
```

### 07.18

- 今日学习时间：0.5h
- 学习内容小结：
  - 阅读Web3URL Docs中 解析模式部分的介绍

支持三种解析模式：自动模式、手动模式以及资源请求模式（其中资源请求模式和手动模式在我看来比较类似）

这里也许因为对智能合约不熟悉，只能大概明白三种不同解析模式的大致意思，对于文档中“Resolve mode determination by clients”并不是太理解，解析模式有客户端决定么？

从下面这部分内容来看，只能说可以从客户端看到智能合约的解析模式。

```bash
web3curl -v 'web3://w3url.eth'
...
* Resolve mode determination... 
> 0xdd473fae
< 0x6d616e75616c0000000000000000000000000000000000000000000000000000
* Resolve mode: manual
...
```

所以，所谓的解析模式是由访问的智能合约本身决定的？还是有文档中“Resolve mode determination by clients”？？

### 07.19

- 今日学习时间：0h
- 学习内容小结：
  - 跟明天预定1h，填充今日学习时间。

### 07.20

- 今日学习时间：0h

- 学习内容小结

### 07.21

- 今日学习时间：0h
- 学习内容小结

### 07.22

- 今日学习时间：0h
- 学习内容小结

### 07.23

- 今日学习时间：1.5h
- 学习内容小结
  - 重新观看[第二次公开课](https://www.youtube.com/watch?v=z207TQYNSdM)
  - 根据教程尝试留言墙案例代码实现。

### 07.24

- 今日学习时间：0h
- 学习内容小结

### 07.25

- 今日学习时间：1h
- 学习内容小结：
  - 根据第二次公开课教程尝试[ethfs-cli](https://github.com/ethstorage/ethfs-cli)工具的使用。

### 07.26

- 今日学习时间：0.5h
- 学习内容小结：
  - 继续尝试[ethfs-cli](https://github.com/ethstorage/ethfs-cli)工具的使用。

### 07.27

- 今日学习时间：0.5h
- 学习内容小结：
  - 继续尝试[ethfs-cli](https://github.com/ethstorage/ethfs-cli)工具的使用。

### 07.28

- 今日学习时间：0h
- 学习内容小结

### 07.29

- 今日学习时间：0h
- 学习内容小结

### 07.31

- 今日学习时间：0h
- 学习内容小结

### 08.01

- 今日学习时间：0h
- 学习内容小结

### 08.02

- 今日学习时间：0h
- 学习内容小结

### 08.03

- 今日学习时间：0h
- 学习内容小结
  
<!-- Content_END -->
