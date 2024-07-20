---
timezone: Asia/Shanghai
---

# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为 WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# Bruce Xu

1. **自我介绍：**

大家好，我是 Bruce Xu，LXDAO 核心成员，Web developer。之前一直对 Web3 URL 比较好奇，但是没有很好的时间和机会来学习和讨论，这次报名跟大家一起学习。

2. **组队期待：**

暂时没什么想法，到时候学习过程中可能会出现吧。

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

50%，期间会前往 EDCON 大会，会在路上，所以又可能没有时间学习。

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

- 今日学习时间：1h
- 学习内容小结：

- ERC-4804 / 6860: Web3 URL to EVM Call Message Translation - an IANA Registered URI Scheme，看起来感觉是 web3:// 访问协议可以把 http 访问转换成 EVM Call
  - IANA 是 Internet Assigned Numbers Authority 用来协调全球 DNS 根域名、数字资源、协议等。如果创建新的协议，需要进行注册，例如 https、ftp 协议等，这些名字需要在 IANA 注册 https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml
  - web3:// 被 Qi Zhou 注册了 https://www.iana.org/assignments/uri-schemes/prov/web3 这种标准化的思维非常值得学习
  - URI vs URL vs URN: URI 是统一资源标识符，包含 URL 和 URN；URL 是统一资源定位符，用于指定资源的位置，如 https://www.example.com；URN 是统一资源名称，用于唯一标识资源，如 urn:isbn:978-3-16-148410-0。
- 这个 URI 的设计挺有意思的，借鉴了 http 和 ftp 的设计，但是含义有所不同
  ![image](https://github.com/user-attachments/assets/f9e5963c-979e-4cf4-b44b-e08364935eec)

  - 这里可能存在几个问题：
    - chainid 用数字表示不太容易看懂是什么链，然后似乎只是 EVM based 的链，可能无法扩展到其他链比如 BTC 或者 Solana
    - 如果没有 ENS，这个 URI 地址会非常长，不是人类可读，不过 ENS 就是为了做这个的，毕竟之前也是因为 IP 地址不好记
      - L2 的 ENS 读取咋实现？
    - 从目前的这个 case 来看，获得的 return 是合约返回的，普通常见的合约似乎只能原始返回 string 等，甚至不是 JSON 格式，不确定返回的 Content Type 能否指定，还是只能 text/plain。
      - 如果需要托管 Web Server 的话，需要合约实现 HTML Template 引擎，根据其他信息合并生成 HTML 返回才能渲染。

- 很多信息目前在链上，但是没有像是 http 一样可以直接读取链上信息的协议或者方法，提供一种新的协议直接调用或者交互合约，所以 web3:// 出来了

  - 等待浏览器直接原生内置估计需要起码 5 - 15 年，可以跟 Brave 这种浏览器聊合作。部分浏览器可能支持插件进行重定向或者代理，不然就是自己做一个浏览器，太难了。
  - 在此之前只能使用 Gateway，但是可能会存在其他问题，比如 Gateway 的审查或者稳定性
    - web3://eth-store.eth/ => https://eth-store.w3eth.io/
    - w3link.io is the current gateway for multi-chain: web3://w3url.eth:11155111/ => https://w3url.11155111.w3link.io/

- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.16

- 今日学习时间：0.5h
- 学习内容小结：

  - 可能的一些应用
    - 去中心化的博客、Dropbox、邮件、git 等
  - 目前需要的帮助

    - 浏览器原生支持和 EF 的帮助
    - gateway 因为一些原因，被举报封禁了
    - 存储费用太高了，放在主网上面

  - 第一节课 https://youtu.be/hmN77o-ex8I

    - 需要有很多应用，这样应用驱动协议落地到主流浏览器上
    - 相比传统应用开发，其实可能更简单，只需要支付部署一次的 gas，然后就可以永久上线了
    - shisui 是一个 Portal Network 的轻客户端，这样就可以从前到后都包括了
    - 欢迎创建 Solana 的版本
    - 以太坊适合读的应用，性能和节点都不错，但是写的应用就不太行了

### 07.17

- 第一节课 https://youtu.be/hmN77o-ex8I
  - 不是所有 Web2 的应用都应该或者适合转成 Web3，什么时候放在 Web3 做是需要思考的
  - 6860 是进行中的标准，更加严谨和完善，4808 是比较简单的
  - 整个 https://w3url.w3eth.io/#/ 就是基于 Web3 URL 和存储在 Web3Q Galileo 上面
    - TODO 这个链是怎么运转的？存储成本怎么样？
      - Note：这是他们维护的一个测试网，将会迁移到 EthStorage 上面
    - TODO 这个合约是怎么实现的？代码在哪里？
    - TODO 每个图片对应的 calldata 是不一样的，访问 URL 的时候，如何映射到合约对应的文件？比如访问 https://w3url.w3eth.io/img/browser.e3be7910.svg
      如何知道 calldata 是 0x2f696d672f62726f777365722e65336265373931302e737667？
  - 目前 Web3 URL 只是读合约和数据，写还是需要自己去调用合约
  - 读取和渲染性能跟客户端比较相关，比如 rust 的就更加快
  - TODO Vitalik 博客的合约是怎么实现的？代码在哪里
  - 所有数据都在链上，Web3 URL 网关只负责读取和组装展示
  - ES 要做的就是一条 L2 可以把存储的费用降低
  -

### 07.18

- https://web3url.io/#/

  - https://cyberbrokers-meta.w3eth.io/renderBroker/5
  - manual mode 和 auto mode 有什么区别？https://docs.web3url.io/web3-url-structure/resolve-mode/mode-auto

    - https://0x4e1f41613c9084fdb9e34e11fae9412427480e56.w3eth.io/tokenSVG/9352?mime.type=svg 通过 ?mime.type 可以指定 content type 来渲染
    - manual 模式是通过合约里面返回相应的信息来判断的
    - 技术实现是使用 fallback 方法进行 url 解析，返回的数据必须是 abi.encoded bytes

    ```
    fallback(bytes calldata cdata) external returns (bytes memory) {
        if(cdata.length == 0 || cdata[0] != 0x2f) {
            return bytes("");
        }

        // Frontpage call
        if (cdata.length == 1) {
          return bytes(abi.encode(indexHTML(1)));
        }
        // /index/[uint]
        else if(cdata.length >= 6 && ToString.compare(string(cdata[1:6]), "index")) {
            uint page = 1;
            if(cdata.length >= 8) {
                page = ToString.stringToUint(string(cdata[7:]));
            }
            if(page == 0) {
                return abi.encode("Not found");
            }
            return abi.encode(indexHTML(page));
        }

        // Default
        return abi.encode("Not found");
    }
    ```

    - manual 默认返回的信息头格式是 Content-type: text/html，如果有后缀，则使用相应的 mime
    - TODO 这样的话，解析和渲染流程也需要行程标准，让 Native 浏览器进行实现？目前这些逻辑实际上在 gateway 层面
    -

-

### 07.19

- https://web3url.io/#/
  - 工作原理：输入 Web3 协议 URL + ENS、解析合约地址、调用合约返回 HTML、渲染页面
  - 基本上要支持整个 http 协议的东西
  - DNS 是去中心化的，基于 ENS
  - 存储在 L2 Storage 上面
  - 动态的由智能合约生成
  - Wanna contribute to the decentralization and run your gateway? Apply a grant for support!
    - TODO Public Goods Node 可以运行一个，LXDAO 的 gateway
  -

### 7.20

- https://docs.web3url.io/web3-clients/https-gateway#w3link.io-all-blockchains-public-gateway
  - gateway 格式 https://xxxx.eth.1.w3link.io/xxx?returns=(string)
- https://docs.web3url.io/
  - TODO Web3 URL 应该针对 NFT 等合约创建一个标准的 Web 智能合约库，这样可以让 NFT 或者 Defi 协议等自动天然的支持交易页面的渲染，完全上链。当然，次之就是通过合约调用的方式，做一个独立的合约也可以
    - 感觉目前常见的 Web server 组件和功能，都可以智能合约化，比如部署一个智能合约博客、论坛、推特等。但是编辑功能可能需要检查
  - TODO 可以用一些插件可以支持将网站内容或者静态内容发布到链上，或者做一个 mirror？
    - 从这个角度来看，EthStorage 和 AR 或者 IPFS 的区别是什么？如何实现以太坊主网合约调用 EthStorage 的数据？如何实现 L2 之间的通信？
  - TODO 可以创建一个 Web3 URL playground 和生成器，类似 GraphQL 这样
  - https://docs.web3url.io/#id-2-categories-of-smart-contracts 标题的 2 一般是 Two？一开始以为是序号
  - TODO Web3 URL gateway 应该也支持写入的场景，无非就是增加 POST 和 PUT method，然后传入相关参数调用合约，同时支付相应 L2 的 gas。从某种角度来说，Web3 URL 实现了以太坊等链的读写一致性
    - 写入的实现？似乎有点麻烦，可能需要 SDK 生成签名等，Web3 URL 接收进行代理发送到网络，也可能需要类似 bundler 的角色，实现 gas fee 等代付，代付的话又会出现内容所属权或者抗审查的问题
- https://eip.fun/eips/eip-4804
  - TODO 默认没有参数的 calldata 是 0x 还是 0x2F？
  - web3://cyberbrokers-meta.eth/renderBroker/9999
    - "Calldata" = "0x" + keccak("view(uint256)")[0:4] + abi.encode(uint256(9999)). 为什么是 view(uint256) method？而不是 renderBroker 方法？
  - TODO 可以跟 bodhi 之类的智能合约都联合起来，前端可以免除？
  - TODO 博客换肤功能，可以通过部署新的合约，然后将 ens 指向新的合约实现
  - TODO ENS Blog，直接基于 ENS 开发博客系统
  - TODO returns 可以支持 GraphQL 查询语句进行组装，这样不就成了 The GraphQL 了吗
    - TODO 有什么链上的数据是比较适合用合约调用和读取的？
  - returns attribute in query tells the format of the returned data. If not specified, the returned message data will be parsed in "(bytes32)" and MIME will be set based on the suffix of the last argument. If returns is "()", the returned data will be parsed in raw bytes in JSON. Otherwise, the returned message will be parsed in the specified returns attribute in JSON. If multiple returns attributes are present, the value of the last returns attribute will be applied. Note that returnTypes is the alias of returns, but it is not recommended to use and is mainly for backward-compatible purpose.
  - Example 4，这里的 to 0x9e081Df45E0D167636DB9C61C7ce719A58d82E3b 是如何确定的？
  - TODO maximum likelihood 的方法，其实会导致 Native 浏览器实现的复杂性，这一点需要纳入考虑，至少把规则写清楚而去比较确定

TODO：

- https://docs.web3url.io/ 官方文档
- 找到相应的合约看看代码实现
- 查看对应的 ERC 原文
  - https://eip.fun/eips/eip-4804
  - https://eip.fun/eips/eip-6860
- 原生支持的浏览器实现 https://github.com/web3-protocol/evm-browser
- 第一节课 https://youtu.be/hmN77o-ex8I
- 查看 https://github.com/ethstorage/awesome-web3
- EthStorage 是怎么扩容以太坊的，通过很低的 costs
- ERC5018: Filesystem-Like Interface https://eips.ethereum.org/EIPS/eip-5018 ethfs-uploader to synchronize folder/files https://www.npmjs.com/package/ethfs-uploader
- ERC5219, ERC6944: Contract Resource Requests Customized headers / error code for ERC4804
- ERC6821: ENS => Address Mapping Standard
- Homework 1
  - Find the ownership of an your favor NFT
  - Find the balance of an account in an ERC-20 contract (USDC / USDT)
  - Deploy a contract in auto model and say “hello world”
  - Deploy a contract in manual model and say “hello world”
- 可以开发一个一键上传或者创建 Web3 站点的合约？

<!-- Content_END -->
