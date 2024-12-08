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

### 07.26

- 今日学习时间：0.5 h

- 学习内容小结：简单了解了在网页前端通过 javascript 连接 metamask 的方法。

### 07.27

- 今日学习时间：1 h

- 学习内容小结：了解了 ens 的相关的合约调用过程。

与 dns 类似，ens 同样需要域名解析服务将域名转换为地址，在 ens 中这个过程是由合约完成的。目前最常用的公共解析合约是 `0x231b0Ee14048e9dCcD1d247744d114a4EB5E8E63`. 大多数情况下，ens 合约处理的域名是经过 namehash 后的定长散列值。域名的 namehash 作为合约参数时常称为 node，例如查询域名对应地址的接口定义就会接收 node 参数。

```
function addr(
    bytes32 node,
    uint256 coinType
) external view returns (bytes memory);
```

对于 web3url 使用的域名，一般会涉及 ETH 主网之外的链 (比如 EthStorage)。 为了支持在 ens 中查询出不同链上的地址，ens 陆续提出了多种解决方案。[ENSIP-7](https://docs.ens.domains/ensip/7) 提出了将多个信息条目编码在 `contenthash` 函数的返回值中。EIP-2304 定义的 `addr` 函数 (接口如上面所示) 允许使用 `coinType` 参数指定查询的地址的所在链，这个设计包含在[ENSIP-9](https://docs.ens.domains/ensip/9)中。

此外，[ERC-6821](https://eips.ethereum.org/EIPS/eip-6821)提出了另一种基于[ENSIP-5](https://docs.ens.domains/ensip/5)文本记录 (Text Records) 的字段 `contentcontract` 使用[ERC-3770](https://eips.ethereum.org/EIPS/eip-3770)表示包含所在链信息的地址。通过访问解析合约的 `text` 函数，并将 `key` 参数设置为 `contentcontract` 就可以获取到相应的地址。

### 07.28

- 今日学习时间：0.5 h

- 学习内容小结：读了一下 [web3drive](https://github.com/ethstorage/w3drive/tree/master) 的代码，大概理解了如何在 EthStorage 上存储私有数据。

### 07.29

- 今日学习时间：1 h
- 学习内容小结：使用 ethfs-cli 上传了一个文件夹。

首先创建一个合约

```
npx ethfs-cli create -c 3334 -p 0x...
chainId = 3334
providerUrl = https://galileo.web3q.io:8545
FlatDirectory Address: 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4
```

这个合约地址就是后面可以用 web3url 访问的地址

上传指定文件夹，这里尝试上传一个开源的工具网站 CyberChef

```
npx ethfs-cli upload -f ../to_upload/CyberChef_v9.21.0  -a 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4 -c 3334 -p 0x...
```

由于错误估计了上传需要的测试币，快把测试币用完也没有完全传上去

设置默认路径，即直接访问 `/` 时响应的文件

```
npx ethfs-cli default -f CyberChef_v9.21.0.html  -a 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4 -c 3334 -p 0x...
providerUrl = https://galileo.web3q.io:8545
chainId = 3334
address: 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4

Transaction Id: 0x3a006d25c1f8096d9c5f33a046df21d2cb80cd5e631e8f7c5a880a0a4d03ca71
Set succeeds
```

这样就可以直接通过合约地址访问网站首页

```
web3://0xae3a76c0fd59c8af8e183931794c959fcba0baf4:3334/
```

由于没有完全上传所有文件，使用浏览器访问时会报错

### 07.30

- 今日学习时间：1 h
- 学习内容小结：使用 ethfs-cli 删除文件和 refund。

删除文件

```
npx ethfs-cli remove -f modules/Image.js -a 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4 -c 3334 -p 0x...

Removing file modules/Image.js
Transaction Id: 0x64a4c16fdb487fea3767e7d4eb7e00aee6cce3da6ddf98bd4eef1251e55b3d90
Remove file: modules/Image.js succeeded
domainBalance: 710000000000000000000, accountBalance: 39284297009767386778, balanceChange: 569504000000000
```

删除文件后会返还上传时支付的 W3Q，balance 变化会体现在合约地址上，使用 refund 操作可以将合约地址上的余额提取到创建者的地址上。

```
npx ethfs-cli refund -a 0xAe3A76c0Fd59C8af8e183931794c959fCba0BaF4 -c 3334 -p 0x...

Transaction Id: 0xeb09d1473fb59f9298c7a3b2126efeca08652a302cfc064de9cfd24467bee346
Refund succeeds
```

之后就可以在创建者的地址上看到余额变化。

### 07.31

- 今日学习时间：1 h
- 学习内容小结：尝试编写了 resourceRequest resolve mode 的 web3url 合约。

resourceRequest resolve mode 是 auto mode 和 manual mode 外的另一种 web3url 的解析方式。

它对 web3url 的处理接口为

```
struct KeyValue {
    string key;
    string value;
}

interface IDecentralizedApp {
    /// @notice                     Send an HTTP GET-like request to this contract
    /// @param  resource            The resource to request (e.g. "/asdf/1234" turns in to `["asdf", "1234"]`)
    /// @param  params              The query parameters. (e.g. "?asdf=1234&foo=bar" turns in to `[{ key: "asdf", value: "1234" }, { key: "foo", value: "bar" }]`)
    /// @return statusCode          The HTTP status code (e.g. 200)
    /// @return body                The body of the response
    /// @return headers             A list of header names (e.g. [{ key: "Content-Type", value: "application/json" }])
    function request(string[] memory resource, KeyValue[] memory params) external view returns (uint statusCode, string memory body, KeyValue[] memory headers);
}
```

例如 web3url 中的 `/gzip.js?12=34` 会解析为参数 `resource=["gzip.js"],params=[["12","34"]]`，且返回值接口被设置为与 http 兼容的形式。

编写合约代码如下

```
// SPDX-License-Identifier: GPL-3.0

pragma solidity ^0.8.18;

struct KeyValue {
    string key;
    string value;
}

contract Hello {
    function resolveMode() external pure returns (bytes32) {
        return "5219";
    }

    function isEqual(bytes memory a, bytes memory b)
        private
        pure
        returns (bool)
    {
        if (a.length != b.length) {
            return false;
        }

        for (uint256 i = 0; i < a.length; i++) {
            if (a[i] != b[i]) {
                return false;
            }
        }

        return true;
    }

    function request(string[] memory resource, KeyValue[] memory params)
        external
        pure
        returns (
            uint256 statusCode,
            bytes memory body,
            KeyValue[] memory headers
        )
    {
        if (resource.length == 1) {
            if (isEqual(bytes(resource[0]), bytes("a.txt"))) {
                // compress data
                body = hex"1f8b0800eb4aaa6602ff0bc9c82c5600a24485b4cc9c5485f2cc920c85e4fcdc82a2d4e2e2ccfc3c3d00c55e612e20000000";
                statusCode = 200;
                headers = new KeyValue[](2);
                headers[0].key = "Content-Type";
                headers[0].value = "text/plain";
                headers[1].key = "Content-Encoding";
                headers[1].value = "gzip";
            } else if (isEqual(bytes(resource[0]), bytes("a.js"))) {
                // set Content-Type
                statusCode = 200;
                body = bytes('console.log("This is a js file.");');
                headers = new KeyValue[](1);
                headers[0].key = "Content-Type";
                headers[0].value = "application/javascript";
            } else {
                statusCode = 404;
                body = bytes("Not Found");
            }
        } else {
            statusCode = 404;
            body = bytes("Not Found");
        }
    }
}
```

部署的地址为 `web3://0x6ef267986a6acd841013dfd4971bc3715dfaf526:11155111`

访问 `web3://0x6ef267986a6acd841013dfd4971bc3715dfaf526:11155111/a.txt` 

响应如下

```
> 0xdd473fae
* RPC provider used: https://rpc.sepolia.org
< 0x3532313900000000000000000000000000000000000000000000000000000000
* Resolve mode: resourceRequest
*
* Path parsing... 
* Contract call mode: method
* Method name: request
* Method arguments types: [{"type":"string[]"},{"type":"tuple[]","components":[{"type":"string"},{"type":"string"}]}]
* Method arguments values: [["a.txt"],[]]
* Contract return processing: decodeErc5219Request
*
* Calling contract ...
* Contract address: 0x6ef267986a6acd841013dfd4971bc3715dfaf526
> 0x1374c46000000000000000000000000000000000000000000000000000000000...0000000000000000000000000000000000000000000000000000000000000000
* RPC provider used: https://rpc.sepolia.org
< 0x00000000000000000000000000000000000000000000000000000000000000c8...677a697000000000000000000000000000000000000000000000000000000000
*
* Decoding contract return ...
* HTTP Status code: 200
* HTTP Headers: 
*   Content-Type: text/plain
This is a file with compression.
```

可以看出压缩编码的文件可以正确解压展示。

访问 `web3://0x6ef267986a6acd841013dfd4971bc3715dfaf526:11155111/a.js`

```
> 0xdd473fae
* RPC provider used: https://rpc.sepolia.org
< 0x3532313900000000000000000000000000000000000000000000000000000000
* Resolve mode: resourceRequest
*
* Path parsing... 
* Contract call mode: method
* Method name: request
* Method arguments types: [{"type":"string[]"},{"type":"tuple[]","components":[{"type":"string"},{"type":"string"}]}]
* Method arguments values: [["a.js"],[]]
* Contract return processing: decodeErc5219Request
*
* Calling contract ...
* Contract address: 0x6ef267986a6acd841013dfd4971bc3715dfaf526
> 0x1374c46000000000000000000000000000000000000000000000000000000000...0000000000000000000000000000000000000000000000000000000000000000
* RPC provider used: https://rpc.sepolia.org
< 0x00000000000000000000000000000000000000000000000000000000000000c8...6170706c69636174696f6e2f6a61766173637269707400000000000000000000
*
* Decoding contract return ...
* HTTP Status code: 200
* HTTP Headers: 
*   Content-Type: application/javascript
console.log("This is a js file.");
```

同样可以得到预期结果。

### 08.03

- 今日学习时间：0.5 h
- 学习内容小结：大致了解了 EthStorage 工作原理。

### 08.04

- 今日学习时间：1 h
- 学习内容小结：阅读了一下  [ethstorage-sdk](https://github.com/ethstorage/ethstorage-sdk/tree/main) 的源码，大致了解了如何用 js 接口进行 EthStorage 相关的合约操作。

<!-- Content_END -->
