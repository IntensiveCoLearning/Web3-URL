# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   YuKirasawa，研一学生。目前的技术方向主要在密码学算法和传统的网络安全技术，最近在学习 bitcoin 底层。希望在共学中学习更多 web3 技术。 

2. **组队期待：**

   希望能参与偏底层和协议的项目。

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

- 今日学习时间：1 h
- 学习内容小结：初步了解了 web3 url，使用 wbe3curl 访问 web3 url 资源

目前，用户要访问 web3 资源通常需要依赖于 web2 应用作为代理，而这些代理是中心化且不受用户控制。Web3 url 就是一种允许使用与 web2 类似的 url 直接访问链上资源的协议。例如，web3 url `web3://0x4e1f41613c9084fdb9e34e11fae9412427480e56/tokenHTML/9352` 就可以访问一个链上 NFT 的 HTML 资源。

Web3 url 的结构如下

```
web3://<contract>[:<chainId>]/<path>
```

主要包括访问的合约地址或域名，合约所在链的 id 和路径。其中路径字段允许智能合约实现特定的接口来返回多样化的数据。

尝试使用 [wbe3curl](https://github.com/web3-protocol/web3curl-js) 访问 web3 url 资源，首先安装 web3curl

```sh
npm install web3curl
```

访问 web3 url

```sh
npx web3curl -v 'web3://w3url.eth'
```

返回结果如下

```
* Fetching URL web3://w3url.eth
* Parsing URL ...
* Host domain name resolver: ens
*   Domain name being resolved: w3url.eth
*   Resolution chain id: 1
*   Resolution type: contentContractTxt
*   contentcontract TXT record: w3q-g:0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
*   Result address: 0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
*   Result chain id: 3334
* Contract address: 0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
* Contract chain id: 3334
* Configured RPCs for chain 3334 (fallback mode) : https://galileo.web3q.io:8545
*
* Resolve mode determination... 
> 0xdd473fae
* RPC provider used: https://galileo.web3q.io:8545
< 0x6d616e75616c0000000000000000000000000000000000000000000000000000
* Resolve mode: manual
*
* Path parsing... 
* Contract call mode: calldata
* Calldata: 0x2f
* Contract return processing: decodeABIEncodedBytes
* Contract return processing: decodeABIEncodedBytes: MIME type: text/html
*
* Calling contract ...
* Contract address: 0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
> 0x2f
* RPC provider used: https://galileo.web3q.io:8545
< 0x0000000000000000000000000000000000000000000000000000000000000020...0000000000000000000000000000000000000000000000000000000000000126
*
* Decoding contract return ...
* HTTP Status code: 200
* HTTP Headers: 
*   Content-Type: text/html
<!doctype html><html lang=""><head><meta charset="utf-8"><meta http-equiv="X-UA-Compatible" content="IE=edge"><meta name="viewport" content="width=device-width,initial-scale=1"><link rel="icon" href="/favicon.svg"/><link rel="stylesheet" href="https://cdn.jsdelivr.net/simplemde/latest/simplemde.min.css"><script src="https://cdn.jsdelivr.net/simplemde/latest/simplemde.min.js"></script><script src="https://cdn.jsdelivr.net/npm/marked@4.0.12/lib/marked.umd.min.js"></script><title>Web3URL</title><script defer="defer" src="/js/chunk-vendors-00833fa6.301e5a03.js"></script><script defer="defer" src="/js/app.13edcf29.js"></script><link href="/css/app.6de1ef51.css" rel="stylesheet"></head><style>html {
    overflow-y: auto!important;
  }
  body {
    background-color: rgba(255,255,255,1);
    font-weight: 700!important;
  }</style><body><noscript><strong>We're sorry but web3-url doesn't work properly without JavaScript enabled. Please enable it to continue.</strong></noscript><div id="
```

从上面可以看出 web3curl 访问 web3 url 的过程。首先对域名进行解析得到域名对应的合约地址，然后使用 RPC 对合约进行访问。

### 07.16

- 今日学习时间：1 h
- 学习内容小结：进一步了解 web3 url 访问合约的接口

当合约没有专门实现 `web3://` 协议的接口时，`web3://` 协议的路径表示了对合约方法的调用，这种模式称为 auto mode. Auto mode 中路径的格式为

```
/<methodName>/<methodArg1>/<methodArg2>/...[?returns=(<type1>,<type2>,...)]
```

例如 `web3://0x4e1f41613c9084fdb9e34e11fae9412427480e56/tokenHTML/9352` 表示访问 `0x4e1f41613c9084fdb9e34e11fae9412427480e56` 合约的 `tokenHTML` 方法，参数为 `9352`. 使用 web3curl 也可以看出解析该地址的过程

```
* Resolve mode: auto
*
* Path parsing... 
* Contract call mode: method
* Method name: tokenHTML
* Method arguments types: [{"type":"uint256"}]
* Method arguments values: ["0x2488"]
* Contract return processing: decodeABIEncodedBytes
* Contract return processing: decodeABIEncodedBytes: MIME type: (not set)
```

对于合约方法的参数，可以使用 `[<type>!]<value>` 的方式指定参数类型，比如 `web3://0x36f379400de6c6bcdf4408b282f8b685c56adc60/getIdToSVG/uint8!42` 表示参数的类型为 `uint8`，值为 42。使用 web3curl 可以看出参数类型确实是 `uint8`

```
* Resolve mode: auto
*
* Path parsing... 
* Contract call mode: method
* Method name: getIdToSVG
* Method arguments types: [{"type":"uint8"}]
* Method arguments values: ["0x2a"]
* Contract return processing: decodeABIEncodedBytes
* Contract return processing: decodeABIEncodedBytes: MIME type: (not set)
```

默认情况下，合约方法的返回值会被解析为 bytes，如果合约方法使用了其他类型的返回值，则需要设置 `?returns=` 字段，例如 `web3://0xA5aFC9fE76a28fB12C60954Ed6e2e5f8ceF64Ff2/levelAndTile/2/50?returns=(uint256,uint256)`

合约也可以专门实现 `web3://` 协议的接口，通过 `resolveMode` 方法来声明

```
function resolveMode() external pure returns (bytes32) {
    return "manual";
}
```

这种模式就是 manual mode.

在 Manual mode 中，路径信息会传入合约的 `fallback(bytes)` 方法，从而允许合约使用自定义的方式处理请求。这种模式和 web2 的 url 路由是一致的。

### 07.17

- 今日学习时间：0.5 h
- 学习内容小结：完成 Homework 1 的前两项
- Homework 部分

1. 查询 `0x08ba8cbbefa64aaf9df25e57fe3f15ecc277af74` id 为 46 的 NFT 的所有者，调用其 ownerOf 方法即可，参数为 tokenId=46。Web3 url 为

   ```
   web3://0x08BA8CBbefa64Aaf9DF25e57fE3f15eCC277Af74/ownerOf/46?returns=(address)
   ```

   返回结果为

   ```
   ["0xEf0b29B14C735505D181eaa613909345A964927D"]
   ```

2. 查询 Bitget 地址 `0x1AB4973a48dc892Cd9971ECE8e01DcC7688f8F23 `的 USDT 持有量，调用其 balanceOf 函数即可，参数为 who=0x1AB4973a48dc892Cd9971ECE8e01DcC7688f8F23。Web3 url 为

   ```
   web3://0xdac17f958d2ee523a2206206994597c13d831ec7/balanceOf/0x1AB4973a48dc892Cd9971ECE8e01DcC7688f8F23?returns=(uint256)
   ```

   返回结果为
   
   ```
   ["0x1210389c1388"]
   ```
   
   



<!-- Content_END -->
