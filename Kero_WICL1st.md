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

#### Questions and Ideas

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

- 今日学习时间：1 hour
- 学习内容小结：
  - How to maintain my blog using ETHStorage and Web3-URL?
  - Read https://docs.web3url.io/

#### Note: How to Maintain My Blog using ETHStorage and Web3-URL?

Access via HTTPS gateway: https://docs.web3url.io/web3-clients/https-gateway#w3link.io-all-blockchains-public-gateway

Debubg Web3-URL using `web3curl`: https://docs.web3url.io/web3-clients/web3curl

Faucet of Web3Q Galileo Chain: https://faucet.w3q.w3q-g.w3link.io/

How to upload files or folders using the ethfs-uploader tool:
1. `npx ethfs-uploader --create --privateKey 0x112233... --chainId 5 --RPC https://...`
2. `npx ethfs-uploader /Users/.../dist w3q-g:0x37DF32c7... --privateKey 0x112233...`
3. `npx ethfs-uploader --default w3q-g:0x37D... --file hello.txt. --privateKey 0x1122..`
4. `https://${address}.w3q-g.w3link.io/${filename}`


The Web3Q Galileo Chain seems suspended to produce new blocks for already 23 hours. Waiting for reply...

### 07.18

- 今日学习时间：0.5 hour
- 学习内容小结：
  - Continue how to maintain my blog using ETHStorage and Web3-URL?

#### Note

```
$ npx ethfs-uploader --create --privateKey <..> --chainId 3334

Transaction: 0x50270e7ba71169e54555c3f9a181f2a775541a18f851ad2c4429bfd30e61bee7
FlatDirectory Address: 0xA10F8D4394F4d2f016411aec53E9A2b73A8CD2f7
```

```
$ npx ethfs-uploader /this-is-a-dir w3q-g:0xA10F8D4394F4d2f016411aec53E9A2b73A8CD2f7  --privateKey <..>

providerUrl = https://galileo.web3q.io:8545
chainId = 3334
address: 0xA10F8D4394F4d2f016411aec53E9A2b73A8CD2f7

Start upload File.......
跨链.md, chunkId: 0
Transaction Id: 0xb6d9f6c99bee830c91571c807b19b89ef2d2f76c589bb3ede8731c01e2bad659
for-fun.jpeg, chunkId: 0
Transaction Id: 0x5d920b8f9127de0cfeafaca15208649449b47ac64a3b48f7c26b9ea1d3b894bd
File 跨链.md chunkId: 0 uploaded!
File for-fun.jpeg chunkId: 0 uploaded!
```

Visit https://0xa10f8d4394f4d2f016411aec53e9a2b73a8cd2f7.w3q-g.w3link.io/crosschain.md

#### Questions

 我上传了一个中文文件名的文件，
交易为 https://explorer.galileo.web3q.io/tx/0xb6d9f6c99bee830c91571c807b19b89ef2d2f76c589bb3ede8731c01e2bad659/internal-transactions ，
文件名为 "跨链.md"，
但是访问 https://0xa10f8d4394f4d2f016411aec53e9a2b73a8cd2f7.w3q-g.w3link.io/跨链.md 结果为空。
换成英文名就正常返回结果。

看起来是哪儿对中文的支持不完全。

### 07.19

- 今日学习时间：0.5 hour
- 学习内容小结：
  - https://eips.ethereum.org/EIPS/eip-4804
  - https://eips.ethereum.org/EIPS/eip-6860
 
### 07.20

- 今日学习时间：0.5 hour
- 学习内容小结：
  - Read codebase https://github.com/web3-protocol/web3protocol-js
  - Read codebase https://github.com/web3-protocol/web3curl-js
  - Read codebase https://github.com/web3-protocol/web3protocol-go

### 07.22

- 今日学习时间：1 hour
- 学习内容小结： 主要在启动项目 web3url.rust --- 一个 Rust 版本的 Web3Url SDK

> This project aims to provide a Rust SDK for [web3url](https://docs.web3url.io/), heavily inspired by [web3protocol-js](https://github.com/web3-protocol/web3protocol-js).


### 07.24

- 今日学习时间：0.5 hour
- 学习内容小结：work on web3url.rust

### 07.25

- 今日学习时间：0.5 hour
- 学习内容小结：决定终止 web3url.rust 项目，将精力转为开启 web3url-on-starknet 新项目。除了决定转变项目外，今天的主要学习内容是深入学习 web3protocol-js，以及翻阅现有的 web3url example projects，为后续集成 web3url-on-starknet 做前期准备

### 07.26

- 今日学习时间：2 hours
- 学习内容小结：Read ERC5018 and associated contracts

#### ERC5018 Notes

一些智能合约需要类似于 filesystem 的操作，比如创建/读取/更改/删除文件。ERC 5018 规范化了一套 filesystem interfaces，用于规范化此类智能合约的接口。同时，由于区块链的交易大小有限制，ERC 5018 为了支持操作大文件，设计了 "dynamic-sized-chunks" 到 "file" 的映射关系。
这套设计不那么像 Unix filesystem，原因是
1. 受到区块链的交易体积的限制；
2. 兼容区块链的不同存储方式
	1. local contract storage via SLOAD/SSTORE; and
	2. contract-code-based via CREATE/CREATE2/EXTCODECOPY.
	3. even outside storage
3. 为了灵活性甚至还把 chunk 设计为 dynamic-sized（或者叫 undefined-sized）

直观上感觉 ERC5018 的 interfaces 设计得有点 “不伦不类”，是 chunk-based 和 file-based 的混合体，虽然能解决应用的问题，但直观上这个设计略显混乱。但在理解了它所要考虑的因素比较复杂后，我倒也找不到更好的方式。
如果我设计的话，我可能会先设计一套 file-chunks interfaces 和 file-metadata interfaces 结合：

```
function create(name, opts = {default_chunk_size})
function read(name, range)
function append(name, data)
function write(name, offset, data)
function writeAndTrunkate(name, offset, data)
function trunkate(name, offset)

function get_metadata(name) -> (length_of_chunks, size_of_file)
```

但是上述这套设计没有考虑到 “何时该新开 chunk”。要把情况都考虑到的话还是挺花时间的，暂时就这样，不深入了。


#### Contracts Notes

- [`ERC5018.sol`](https://github.com/ethstorage/evm-large-storage/blob/b393f054eaca3ef383f9cf9486c774fa76c881f8/contracts/ERC5018.sol) 的多数工作量是做多种模式的兼容，算是一个大而全 filesystem-like contract
- [`FlatDirectory.sol`](https://github.com/ethstorage/evm-large-storage/blob/e51778c7d2dbb9d6f6dc6f8e22b0a71da166b6cd/contracts/examples/FlatDirectory.sol) 约等于 [ERC5018.sol](https://github.com/ethstorage/evm-large-storage/blob/b393f054eaca3ef383f9cf9486c774fa76c881f8/contracts/ERC5018.sol)，只是加上了个 `fallback` 函数而已。
- `SimpleFlatDirectory.sol` 不是 ERC5018 规范的合约，是使用 `StorageManager.sol` 而搞的文件系统。可能这个合约是为了展示 web3url 的用途。
- `SimpleNameService.sol` 可能这个合约是为了展示 web3url 的用途。
- `SimpleW2box.sol` 可能这个合约是为了展示 web3url 的用途。

### 07.28

- 今日学习时间：0.5 hour
- 学习内容小结：如何区分 client side 和 server side 代码；一个 React 项目是如何运行的（dist）；

#### Note by ChatGPT4

运行React项目时使用到Node.js主要是因为Node.js提供了npm（Node Package Manager），这是一个包管理工具，用于安装和管理项目依赖。React项目通常会依赖许多外部库和工具，例如React本身、React-DOM以及可能的路由和状态管理库等，这些都可以通过npm轻松安装和更新。

此外，Node.js环境支持使用Webpack、Babel等工具来构建和打包JavaScript代码。这些工具可以帮助开发者将React的JSX语法转换为浏览器能理解的JavaScript代码，同时还可以优化应用的性能，比如通过压缩文件来减少加载时间。

虽然理论上你可以不使用Node.js直接在浏览器中使用React（例如通过CDN直接引入React库），但这种方式通常只适用于非常简单的项目。对于大多数现代的、复杂的React应用来说，使用Node.js及其生态系统中的工具是非常必要的，因为它们提供了构建、测试、开发和部署等一系列自动化和优化功能，极大地提高了开发效率和项目的可维护性。

总的来说，虽然不是绝对必须，但在大多数情况下，使用Node.js来运行和管理React项目会更加高效和方便。

### 07.28

- 今日学习时间：4 hour
- 学习内容小结：基于 React + Next + wagmi 开发 web3url on-chain blog

#### Note

好像 https://github.com/web3-protocol/web3protocol-js 是一个后端库，不适用于前端，反正对于我这种没有网站开发经验的人来说，不知道怎么在前端项目里适用 web3protocol-js。

还是自己包装个库吧，不折腾 web3protocol-js 了。


<!-- Content_END -->
