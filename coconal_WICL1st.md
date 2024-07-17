# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为 WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   coconal 学生 熟悉 go，solidity，React 想了解更多 Web3 技术

2. **组队期待：**

   没有想法，有 idea 可以一起

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   Yes 100%

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

举例示范：

- 今日学习时间：1h
- 学习内容小结：什么是 Web3 url 协议，简单使用 web3 url ,简单了解了 ERC-4804
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.16

- 今日学习时间：40min
- 小结 :
  时间较少，简单调用示例
  结构

```
web3://<contract>[:<chainId>]/<path>
```

自动模式

```
/<methodName>/<methodArg1>/<methodArg2>/...[?returns=(<type1>,<type2>,...)]
```

returns 指定返回

```
 npx web3curl -v "web3://0xA5aFC9fE76a28fB12C60954Ed6e2e5f8ceF64Ff2/levelAndTile/2/50?returns=(uint256,uint256)"
npm info using npm@10.2.4
npm info using node@v20.11.0
npm info ok
npm info using npm@10.2.4
npm info using node@v20.11.0
* Fetching URL web3://0xA5aFC9fE76a28fB12C60954Ed6e2e5f8ceF64Ff2/levelAndTile/2/50?returns=(uint256,uint256)
* Parsing URL ...
* Host domain name resolver: (none)
* Contract address: 0xA5aFC9fE76a28fB12C60954Ed6e2e5f8ceF64Ff2
* Contract chain id: 1
* Configured RPCs for chain 1 (fallback mode) : https://ethereum.publicnode.com https://cloudflare-eth.com
*
* Resolve mode determination...
> 0xdd473fae
* RPC provider used: https://ethereum.publicnode.com
< 0x
* Resolve mode: auto
*
* Path parsing...
* Contract call mode: method
* Method name: levelAndTile
* Method arguments types: [{"type":"uint256"},{"type":"uint256"}]
* Method arguments values: ["0x2","0x32"]
* Contract return processing: jsonEncodeValues
* Contract return processing: jsonEncodeValues: Types of values to encode: [{"type":"uint256"},{"type":"uint256"}]
*
* Calling contract ...
* Contract address: 0xA5aFC9fE76a28fB12C60954Ed6e2e5f8ceF64Ff2
> 0xd55dd04300000000000000000000000000000000000000000000000000000000...0000000000000000000000000000000000000000000000000000000000000032
* RPC provider used: https://ethereum.publicnode.com
< 0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000024
*
* Decoding contract return ...
* HTTP Status code: 200
* HTTP Headers:
*   Content-Type: application/json
["0x1","0x24"]
```

### 07.17

- 今日学习时间：30min
- Homework 1
  Find the ownership of an your favor NFT
  https:

```
https://0x60e4d786628fea6478f785a6d7e704777c86a7c6.eth.w3link.io/ownerOf/458?returns=(address)
```

web3url

```
web3://0x60e4d786628fea6478f785a6d7e704777c86a7c6/ownerOf/458?returns=(address)
```

- Find the balance of an account in an ERC-20 contract (USDC / USDT)

Vitalik 的 USDT 余额

```
https://0xdac17f958d2ee523a2206206994597c13d831ec7.eth.w3link.io/balances/0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045?returns=(uint256)
```

<!-- Content_END -->
