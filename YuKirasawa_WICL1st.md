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
   

### 07.18

- 今日学习时间：1 h

- 学习内容小结：学习了合约的基本编写和部署流程。完成 Homework 1 的第三项

- Homework 部分

  我使用 [remix](https://remix.ethereum.org) 和 Sepolia 测试链进行合约部署，Sepolia 的链 id 为 11155111，web3url 访问时需要指定

  对于 auto mode，只需要编写 sayHello 方法再使用 web3url 调用即可

  编写合约如下

  ```
  // SPDX-License-Identifier: GPL-3.0
  
  pragma solidity >=0.7.0 <0.9.0;
  
  contract SayHello_auto {
      function sayHello() public pure returns (string memory) {
          return "Hello World";
      }
  }
  ```

  合约地址为 `0xae3a76c0fd59c8af8e183931794c959fcba0baf4`，

  使用 web3curl 访问 url `web3://0xae3a76c0fd59c8af8e183931794c959fcba0baf4:11155111/sayHello`
  
  可以得到响应 Hello World

### 07.19

- 今日学习时间：1 h
- 学习内容小结：学习了 fallback 方法的机制和编写方法。尝试部署 manual mode 的 web3url 合约。暂时还未成功。

### 07.20

- 今日学习时间：1 h

- 学习内容小结：完成 Homework 1 的第四项

- Homework 部分

  部署 manual mode 的合约，需要先通过 `resolveMode` 方法声明，再编写 `fallback` 处理请求。

  ```
  // SPDX-License-Identifier: GPL-3.0
  
  pragma solidity ^0.8.18;
  
  contract Hello {
      function resolveMode() external pure returns (bytes32) {
          return "manual";
      }
  
      function sayHello() public pure returns (string memory) {
          return "Hello World";
      }
  
      fallback(bytes calldata cdata) external returns (bytes memory) {
          if(cdata.length == 0) {
              return bytes("");
          }
          if(cdata[0] != 0x2f) {
              return abi.encode("Incorrect path");
          }
  
          if (cdata.length == 1) {
              return abi.encode(sayHello());
          }
  
          // Default
          return abi.encode("Not found");
      }
  }
  ```

  合约地址为 `0x35ffD0786ae4F845C7473A1f25C6BFd200585806`

  使用 web3curl 访问 url `web3://0x35ffD0786ae4F845C7473A1f25C6BFd200585806:11155111` 可以得到响应 Hello World

### 07.21

- 今日学习时间：0.5 h

- 学习内容小结：学习了一些以太坊合约的基础知识。

以太坊合约的访问方式有两种，一种是只读访问，一种是读写访问。其中只读访问只读取链上数据，而不对链上数据进行修改，因此不需要链上的交易操作，也不需要使用钱包签名。而读写访问可以对链上数据进行修改，因此需要通过向以太坊网络发送交易实现，也需要使用钱包对要进行的交易进行签名。在前面对 web3url 进行访问的时候，我们并没有使用钱包，因此上面的 web3url 访问操作都是只读访问。

### 07.22

- 今日学习时间：1 h

- 学习内容小结：学习了一些 ENS 的基础知识。

ENS (Ethereum name service) 是一个与 DNS 类似的 web3 网络的域名服务系统。比如当访问 `web3://w3url.eth`，域名 w3url.eth 就会先被 ENS 解析为实际的合约地址，再进行合约的访问。

在 web3curl 中，可以看到一部分 ens 解析的流程

```
* Host domain name resolver: ens
*   Domain name being resolved: w3url.eth
*   Resolution chain id: 1
*   Resolution type: contentContractTxt
*   contentcontract TXT record: w3q-g:0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
*   Result address: 0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
*   Result chain id: 3334
* Contract address: 0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6
* Contract chain id: 3334
```

由于没有指定 chainId，默认使用 eth 主网进行 ens 解析。解析过程中查询到了 contentContractTxt 记录，这是 ERC-6821 定义的适用于 web3url 的解析记录。这个记录可以包含由 ERC-3770 定义的包含链信息的地址，正如上面解析过程中得到的 `w3q-g:0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6`，这样的记录可以使客户端自动确定这个域名对应的合约所在的 chainId。

### 07.23

- 今日学习时间：1 h

- 学习内容小结：完成 Homework 2 的第一项，并对 web3box 的结构进行一些分析。

- Homework 部分

  在 web3box 上上传文件非常简单，只需要在浏览器上访问 `https://w3-box.w3eth.io/#/`，连接钱包，选择上传文件并使用钱包签名即可。上传成功后网页会给出访问文件的 url `https://galileo.web3q.io/file.w3q/0xdf33654b75055f14d0af487efc52744a0d89ef49/ico.jpg`. 使用浏览器访问即可查看该文件。

  web3box  主要由三个合约组成：`0x1499a319278e81390d2f32afa3ab08617d5e8c0d` (即 w3-box.eth 或 w3box.w3q) 是存储和展示网页前端的合约，`0x731cd5311e9bad1e99e7f1081a91a38c02b5f47d` 是 web3box 的后端，也就是 [SimpleW3box.sol](https://github.com/ethstorage/w3box/blob/main/contracts/SimpleW3box.sol) 所部署的合约，实现了一些用户接口并调用文件存储合约完成相关操作，`0x37926Ea3020C114B4042F0ca86Ee5587A2b20D11` (即 file.w3q) 是最终的文件存储合约，实现了文件存储并使用 manual mode 解析和处理文件访问请求。

  下面尝试使用 web3url 访问上述合约的一些方法。

  访问 `web3://0x731cd5311e9bad1e99e7f1081a91a38c02b5f47d:3334/getAuthorFiles/0xdf33654b75055f14d0af487efc52744a0d89ef49?returns=(uint256[],bytes[],bytes[],string[])` 可以得到该地址在合约上存储的文件列表。返回的结果为 

  ````
  [["0x669f9038"],["0x69636f2e6a7067"],["0x696d6167652f6a706567"],["https://galileo.web3q.io/file.w3q/0xdf33654b75055f14d0af487efc52744a0d89ef49/ico.jpg"]]
  ````

  访问 `web3://0x37926Ea3020C114B4042F0ca86Ee5587A2b20D11:3334/0xdf33654b75055f14d0af487efc52744a0d89ef49/ico.jpg` 可以得到上面上传的图片。

### 07.24

- 今日学习时间：0.5 h

- 学习内容小结：了解了网站连接钱包的方法。

在浏览器网页上 web3box 的操作过程中，通过浏览器可以看到通过 web3url 网关与 `w3-box.eth` 和 `file.w3q` 的交互过程，但看不到与 `0x731cd5311e9bad1e99e7f1081a91a38c02b5f47d` 合约的交互过程。原因是这个合约是通过连接钱包与用户交互的，而不是通过 web3url 网关。因此今天了解了一下合约是如何连接钱包交互的。

### 07.25

- 今日学习时间：0.5 h

- 学习内容小结：使用 web3box 上传了简单的网页。

由于 web3box 对上传的文件提供的 url 是在以地址命名的文件夹内，且文件不会进行重命名，就可以使用在 web3box 中的 html 等文件中使用相对路径访问。编写了简单的 html 文件进行验证。web3url 为 `web3://0x37926Ea3020C114B4042F0ca86Ee5587A2b20D11:3334/0xdf33654b75055f14d0af487efc52744a0d89ef49/index.html`。使用浏览器访问，可以发现确实可以加载出 html 中引用的相对路径图片。

<!-- Content_END -->
