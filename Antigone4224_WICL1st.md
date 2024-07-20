# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# Antigone4224

1. **自我介绍：**

   我是Antigone,cuit区块链准大三学生，想通过共学计划进一步，学习并参与到web3://这样新兴的协议中。本次共学的笔记会发在[我的博客](https://antigone4224.github.io/)

   **组队期待：**

   还在观望，暂无，随时更新。

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

- 今日学习时间：2h
- 学习内容小结：详情见[我的博客](https://antigone4224.github.io/web3-url-colearing-day1),预习了一下slides里的内容，对于web3-url有了一个大致的了解。

预习了一下第一次的 [slides](https://docs.google.com/presentation/d/1egJUKJrjC9wjkmOF9sLBkTSwHpd6hl8FXkWehPW7kFk/edit#slide=id.g1754f50a55c_0_11),简单的介绍了一下web3://协议

ERC-4804提出了使用RFC 2396 URI来表示一个以太坊消息调用，给予了我们一种直接访问以太坊区块链的方式，也就是web3 url，从此不再需要经过http://或者ipfs的代理。

可以参考下面这张图（直接从slides里扒的链接，可能会没法加载= =）

下面的标识是对应URI的RFC标准，上面的标识是对应了对于区块链中具体寻址的对应。

![img](https://lh7-us.googleusercontent.com/slidesz/AGV_vUcpijLKlO-0God_BdgVPYw8-B1CSb0YvALN8_5X4tXih74cxO9O_35jEs8nUlHKo6ba4NkSgxihzte_nqw-Q53i49ZkHJ-_bjI2IlJPIXT-1A-ghRAGLGQQsgBtx51hNyWWOEQMOe3VnLAOpqj65W7kvLrWFqmz=s2048?key=0jO8rkPrChFDCniaDj_L9Q)

可以看到web3:// 支持大多数http://的功能，就是对标以太坊生态中的http://,与ipfs://不同的是，web3://是直接对接到链上的，虽然看起来都是去中心化的一种应用层协议，但是ipfs://对接的是共享文件的peer节点，web3://对接的是以太坊或者EVM生态的区块链网络。

slides里提供了两种使用web3:// 协议的方式，一种是[火狐浏览器插件](https://addons.mozilla.org/en-US/firefox/addon/web3url/),这种访问还是经过了gateway 经过http://代理来实现的访问(看起来只是将请求转换成了url请求发送给gateway),然后就是一个[EVM Browser](https://github.com/web3-protocol/evm-browser) 这个在我仅仅只看Readme的情况下，需要一个https的链接指定rpc，，翻了下[源码](https://github.com/web3-protocol/web3protocol-js/blob/main/src/chains/client.js)，还真是http call rpc,,

```
  async #rpcCall(rpcUrl, args) {
    if(this.#rpcCallCounters[rpcUrl] === undefined) {
      this.#rpcCallCounters[rpcUrl] = 0;
    }
    this.#rpcCallCounters[rpcUrl]++;

    let postData = {
      jsonrpc: "2.0", 
      id: this.#rpcCallCounters[rpcUrl],
      method: "eth_call",
      params:[
        args,
        "latest"
      ]
    }

    const response = await fetch(rpcUrl, {
      method: 'POST', 
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(postData)
    })

    if(response.status != 200) {
      throw new Error("RPC returned an error HTTP code: " + response.status);
    }

    const json = await response.json()

    if(json.error) {
      throw new Error("RPC returned an error: " + json.error.message);
    }

    if(json.result === undefined || json.result === "" || json.result == "0x") {
      throw new Error("No data returned");
    }
    

    // We got some data!
    return json.result;
  }
```



感觉独立协议的部分应该还是未完全完成的状态？

按照ppt的指引，通过web3://访问

![](https://github.com/antigone4224/blog-img/blob/main/image-20240715131149029.png?raw=true)

浏览器抓包也能很明显看出还是隐式的使用了https

<img src="https://github.com/antigone4224/blog-img/blob/main/image-20240715132058280.png?raw=true" alt="image-20240715132058280" style="zoom: 200%;" />

后面slides还讲了一堆将常规web2应用迁移到web3的例子，展示了web3://代替http://的可能性。

随后 slides里列出了对该erc进行拓展的[ERC-5018](https://eips.ethereum.org/EIPS/eip-5018)：实现一个在合约类文件系统的接口给合约访问/上传资源，让合约应用显得更贴近web应用，更加符合常规web应用开发的逻辑。 

[ERC-6944](https://eips.ethereum.org/EIPS/eip-6944)：希望添加一种请求资源的参数解析模式(erc-4804提出了manual和auto两种，前者并不会自动填充参数，所以应该会产生参数缺失无法成功访问的问题)，应该也是为了优化web3网页的体验。



### 07.16

博客链接：[web3-url-colearning-day2 (antigone4224.github.io)](https://antigone4224.github.io/web3-url-colearning-day2)

完成了hw1

# hw1:

## Find the ownership of an your favor NFT

查询一下slides里展示的cyberbrokers吧

ERC721有ownerOf方法可以通过tokenid查询owner的地址

![image-20240716151628876](https://github.com/antigone4224/blog-img/blob/main/image-20240716151628876.png?raw=true)

在etherscan上查询的合约地址可以调用ownerOf方法，然而cyberbrokers-meta这个地址却不能

![image-20240716151915929](https://github.com/antigone4224/blog-img/blob/main/image-20240716151915929.png?raw=ture)

再尝试了一下发现那个0x89的合约地址同样也无法执行renderBroker的方法

ens上查询了一下0x8b开头的一个合约地址能renderBroker

还是有点不太明白怎么回事暂时。

## Find the balance of an account in an ERC-20 contract (USDC / USDT)

ERC20 有个balanceOf方法可以查询余额

web3:// (addr of contract)/balanceOf/(acc addr)?returns=(uint256)

![image-20240716144143413](https://github.com/antigone4224/blog-img/blob/main/image-20240716144143413.png?raw=true)

## Deploy a contract in auto model and say “hello world”

很明显是要我们关注ERC 6860关于 解析模式(resolve mode)的定义了

```
 Resolve Mode
Once the “To” address and chainid are determined, the protocol will check the resolver mode of contract by calling the resolveMode method of the “To” address. The Solidity signature of resolveMode is:

function resolveMode() external returns (bytes32);
The protocol currently supports two resolve modes: auto and manual.

The manual mode will be used if the resolveMode return value is 0x6d616e75616c0000000000000000000000000000000000000000000000000000, i.e., “manual” in bytes32
The auto mode will be used if :
the resolveMode return value is 0x6175746f00000000000000000000000000000000000000000000000000000000, i.e, “auto” in bytes32, or
the resolveMode return value is 0x0000000000000000000000000000000000000000000000000000000000000000, or
the call to resolveMode throws an error (method not implemented or error thrown from the method)
Otherwise, the protocol will fail the request with the error “unsupported resolve mode”.
```

合约地址：0xea100cb127d5547793172248e730e1b4b6524984

部署在sepolia

代码：

```
pragma solidity >=0.7.0 <0.9.0;

contract Hello_world_auto {
    function sayHelloWorld() public pure returns (string memory) {
        return "Hello World";
    }

    function resolveMode() pure external returns (bytes32) {
        return bytes32("auto");
    }
}
```



![image-20240716200355477](https://github.com/antigone4224/blog-img/blob/main/image-20240716200355597.png?raw=ture)

## Deploy a contract in manual model and say “hello world”

同理

```
pragma solidity >=0.7.0 <0.9.0;

contract Hello_world_manual {
    function sayHelloWorld() public pure returns (string memory) {
        return "Hello World";
    }

    function resolveMode() pure external returns (bytes32) {
        return bytes32("manual");
    }
}
```

不过我还没有比较过manual，和auto访问时候的特性，这个丢到明天来继续。

### 07.17

博客地址：https://antigone4224.github.io/web3-url-colearning-day3

今天稍微有点事情，可能就没法接着把hw做完了，打算完善一下对于resolve mod的理解,阅读ERC 6860文档，对比Auto Mod 和manual  Mod的区别：

```
the protocol will call the address with “Calldata” = keccak("resolveMode()")[0:4] = “0xDD473FAE”
```

在第一访问的开始，会尝试调用resolveMode()方法来确定resolvemod

如果仅指定地址 chainid,路径为空，Manual的calldata会是"/",AutoMod的calldata会为空。。

ManualMod会直接将Path+Query作为Calldata发出，而AutoMod会多一个进行abi转化的功能(AutoMod 可以把参数放到路径中，以及可以通过returns指定返回结果的类型，在调用的时候会自动转化成符合正常合约调用的abi的calldata调用的)。

Manual Mod 返回数据默认为text/html，如果不是会根据MIME后缀名自动识别，而Auto Mod则是根据returns的指定返回application/json，如果没有returns应该是undefined，从这个角度来说，ManualMod更适合于访问资源，而auto mod更适合于作为数据处理的中继。

Manual Mod可以很精准的定位资源在合约中的位置，但很明显这种直接将相对位置作为call data的方式是需要特殊支持的，就好像写web框架需要单独的文件服务一样，它更符合我们对于web2资源访问的构思。

***07.18***

博客地址：[web3-url-colearning-day4 (antigone4224.github.io)](https://antigone4224.github.io/web3-url-colearning-day4)

今天学习一下ethstorage。

```
EthStorage 是一个模块化和去中心化的存储 Layer 2，提供由数据可用性（DA）驱动的可编程键值存储。它为 Rollups 提供了长期的数据可用性解决方案，并为完全链上应用程序（如游戏、社交网络、人工智能等）开辟了新的可能性。

动机
EthStorage 背后的主要动机是提供基于以太坊的长期数据可用性。

EIP-4844 引入了数据斑块（data blobs），这增强了 Layer 2 扩展解决方案（如 Rollups）的吞吐量和效率。然而，这些数据斑块是临时可用的，意味着它们将在几周后被丢弃。这产生了一个显著的影响：L2 无法无条件地从 L1 推导出最新状态。如果某些数据无法再从 L1 检索，Rollup 可能无法同步链。

通过 EthStorage 作为长期数据可用性解决方案，L2 可以随时从它们的数据可用性层（以太坊 DA、Celestia、EigenDA 等 + EthStorage）中推导数据。

EthStorage 还为完全链上应用程序（如游戏、社交网络、人工智能等）开辟了新的可能性。
```



[ethstorage文档](https://docs.ethstorage.io/)

[为ETHstorage提供存储](https://docs.ethstorage.io/storage-provider-guide/tutorials)，也算是某种存储挖矿（，可惜要550g的空余存储空间，不然挖矿还是挺香的

ethstorage的愿景是让以太坊网络的存储变得不再昂贵，到了一种可接受的程度，这样通过web3 url许多web2的网络服务也就可以部署在web3上了。

***07.19***

博客地址：[web3-url-colearning-day5 (antigone4224.github.io)](https://antigone4224.github.io/web3-url-colearning-day5)

在群组中发送地址，得到了1000测试ETH

可以拿来在ETH Storage上传文件

![image-20240719153443861](https://raw.githubusercontent.com/antigone4224/blog-img/main/image-20240719153443861.png)

![image-20240719153355799](https://raw.githubusercontent.com/antigone4224/blog-img/main/image-20240719153355799.png)

https://galileo.web3q.io/file.w3q/0x81fb5c383f192f7fa1f0788e1a06aed26ffac469/b_d42a32a060f284d3ffe3b4cf8cc08501.jpg

上传了我的qq头像（

![](https://galileo.web3q.io/file.w3q/0x81fb5c383f192f7fa1f0788e1a06aed26ffac469/b_d42a32a060f284d3ffe3b4cf8cc08501.jpg)

成功的存在了galileo测试网上（

文件的地址一般是 web3://we3q.io:

花费两个测试ETH

![image-20240719154421408](https://raw.githubusercontent.com/antigone4224/blog-img/main/image-20240719154421408.png)

### 7.20

博客地址：[web3-url-colearning-day6 (antigone4224.github.io)](https://antigone4224.github.io/web3-url-colearning-day6)

今天学习一下[Ethfs](https://docs.ethstorage.io/dapp-developer-guide/tutorials/upload-your-file-folder-with-ethfs-cli)

安装Ethfs-cli

```
npm install -g ethfs-cli
ethfs-cli upload -f <directory|file> -a <address> -p <private-key> -r [rpc] -t [upload-type]

```

创建Flat Directory 合约

```
ethfs-cli create -p privkey
chainId = 3334
providerUrl = https://galileo.web3q.io:8545
FlatDirectory Address: 0x6F3F9E477a931d208c06efE7E6D3af251B000E94
```

得到

上传第一个文件夹

```
ethfs-cli upload -f myfolder -a 0x6F3F9E477a931d208c06efE7E6D3af251B000E94 -c 3334 -p dadd64540987deea8210cfadcf50aeeed4ec14950a1f05260f7f59084f3b0727
providerUrl = https://galileo.web3q.io:8545
chainId = 3334
address: 0x6F3F9E477a931d208c06efE7E6D3af251B000E94

Send Success: File: hello.txt, Chunk Id: 0, Transaction hash: 0xa7a48056301a4b1773dff28a825576d6b8e2b2dd700d8a30dbbac77a4ac0450b
File hello.txt chunkId: 0 uploaded!


Total Upload Chunk Count: 1
Total Upload File Size: 0.005859375 KB
Total Cost: 0.0 ETHethfs-cli upload -f myfolder -a 0x6F3F9E477a931d208c06efE7E6D3af251B000E94 -c 3334 -p dadd64540987deea8210cfadcf50aeeed4ec14950a1f05260f7f59084f3b0727
providerUrl = https://galileo.web3q.io:8545
chainId = 3334
address: 0x6F3F9E477a931d208c06efE7E6D3af251B000E94

Send Success: File: hello.txt, Chunk Id: 0, Transaction hash: 0xa7a48056301a4b1773dff28a825576d6b8e2b2dd700d8a30dbbac77a4ac0450b
File hello.txt chunkId: 0 uploaded!


Total Upload Chunk Count: 1
Total Upload File Size: 0.005859375 KB
Total Cost: 0.0 ETH
```

成功上传

web3://0x6F3F9E477a931d208c06efE7E6D3af251B000E94:3334/hello.txt

![image-20240720184338899](https://raw.githubusercontent.com/antigone4224/blog-img/main/image-20240720184338899.png)

![image-20240720184656521](https://raw.githubusercontent.com/antigone4224/blog-img/main/image-20240720184656521.png)



<!-- Content_END -->
