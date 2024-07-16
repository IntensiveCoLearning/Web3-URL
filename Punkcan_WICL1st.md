# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ Punkcan ]

1. **自我介绍：**
   
   Punkcan
   
   现在是个普通上班族，编程，数据库，服务器，杂七杂八的都会一点点。
   
   Web3 URL 以前没接触过，新玩意就想捣鼓一下。
   
   年纪有点大，还有严重老花，可能不适合长时间编程。
   
   INTP

2. **组队期待：**
   
   还不确定，看哪需要人哪去

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**
   
   66. 666% 

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

举例示范：

- 今日学习时间：1h

- 学习内容小结：
  
  - EIP-4804，主要是能够透过协议定位EVM内部的资源
  - 现在的Firefox的addon ，是直接转换网关的网址
  - 最直观的理解就是透过URL的方式直接呼叫智能合约Read 所Response的内容
  - ![](https://web3url.io/img/auto-mode.02a3a3cc.svg)
  - 上面这张图，白话解释就是：从333这个chain上，呼叫example.eth这个合约或地址的BalanceOf（Arg0是要传入的参数）
  - 目前Web3URL的网站的合约：0xEbcA4860ebBe969E9Bc42643fcb437879dBDa9C6 @ Web3Q Galileo (id 3334)，可以参考
  - 可以跨链，内容可以储存在便宜的L2或是其他侧链上，也可以布署在测试网上
  - EVM读取速度很快，所以用户读取速度不影响（EVM是写的慢）

- Homework 部分（如果有安排需要填写证明完成）

- Question and Ideas
  
  - 如果有js framework支持，就可以让一般网站也可以混合使用？现在有吗？
  - 如何让浏览者产生交互？如果写留言板，意味着操作界面要做到「呼叫钱包写入数据EVM」对吗？
    - 应该是的
  - 网关如何搭建？
    - [GitHub - ethstorage/web3url-gateway: A gateway implementation of the web3 access protocol (web3://) that can serve HTTP-style Web3 URL for blockchain resource access.](https://github.com/ethstorage/web3url-gateway)

- ### 07.16

- 今日学习时间：1h

- 学习内容小结：
  
  - 今天看到网关的架设，似乎有一个支援的Chainlist，也就是说并不是随便架设一个chain 就可以支援，衍生出：如果要架设一个Chain来专门处理，要如何申请Chain ID的问题，查了一下EIP155的资料，流程如下
    
    - 查询 Chain ID
      
      1. **访问 GitHub 仓库**： 打开 [ethereum-lists/chains](https://github.com/ethereum-lists/chains) 仓库。
      
      2. **查看 chains.json 文件**：在查看已经登记的 Chain ID 列表。
      
      3. **Fork 仓库**
      
      4. **修改 chains.json 文件**
         
         - 在fork 仓库中，编辑 `chains.json` 文件，添加您选择的 Chain ID 及其详细信息。
         
         例如：
         
         ```json
         {
           "name": "My Custom Network",
           "chainId": 12345,
           "networkId": 12345,
           "rpc": ["https://my-custom-network.rpc.url"],
           "faucets": [],
           "explorers": [{"name": "my-explorer", "url": "https://my-explorer.url"}],
           "nativeCurrency": {"name": "MyToken", "symbol": "MTK", "decimals": 18}
         }
         ```
      
      5. **提交 Pull Request**：
         
         - 提交修改，并创建一个 Pull Request 将您的更改提交回 `ethereum-lists/chains` 仓库。
         - 在 Pull Request 中，详细描述您的链和 Chain ID 的用途，解释为什么选择该 ID。
      
      6. **等待审核和合并**：
         
         - 社区维护者会审核您的 Pull Request。如果没有问题，他们会将您的更改合并到主仓库中。
         - 一旦合并，您的 Chain ID 就正式登记在案，其他开发者可以看到并避免选择相同的 ID。
  
  - 格式理解：
    
    - web3://0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48/balanceOf/nemorino.eth?returns=(uint256) 
    
    - 如果换成现在网关的URL 就会变成https://0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48.w3eth.io/balanceOf/nemorino.eth?returns=%28uint256%29
    
    - 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48 就是读取的合约，现在使用的是USDC的合约，如果要换成USDT合约，就是0xdAC17F958D2ee523a2206206994597C13D831ec7
    
    - balanceOf 就是要读取哪个方法
    
    - nemorino.eth 就是要输入的值（Arg0)
    
    - returns=(uint256)，回传值，如果这个没有指定，会发生错误
    
    - 如果要换到类似Polygon上，格式变成  web3://0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48:**137**/balanceOf/nemorino.eth?returns=(uint256)
    
    - http 变成https://0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48 **.137.** w3eth.io/balanceOf/nemorino.eth?returns=%28uint256%29
    
    - 但是在这时候要注意一个问题，就是ENS在Polygon上是无法解析的，所以要打完整的个网址名称
    
    - 以下网址就可以读取到我在Polygon上的USDT https://0xc2132d05d31c914a87c6611c10748aeb04b58e8f.137.w3eth.io/balanceOf/0x1d41D6B1091C1a8A334096771bd1776019243d5e?returns=(uint256)
    
    - 另一个小问题就是SSL无法支援 0xc2132d05d31c914a87c6611c10748aeb04b58e8f.137.w3eth.io 会报安全错误
    -  web3://0xe42cad6fc883877a76a26a16ed92444ab177e306/owner?returns=(address) ，这个案例中owner并没有需要输入的arg0，因此returns直接接在owner即可
  


- Homework 部分
  
  - Find the ownership of an your favor NFT
    - 测试了https://etherscan.io/address/0xe42cad6fc883877a76a26a16ed92444ab177e306#readContract
    - https 的格式 https://0xe42cad6fc883877a76a26a16ed92444ab177e306.w3eth.io/owner?returns=(address)
    - web3URL 的格式 web3://0xe42cad6fc883877a76a26a16ed92444ab177e306/owner?returns=(address)
    - 正确显示 "0xAB9e1DDf806a20C9B06A94c655a59C3eDF495Ca5"
    - 
    ![[Pasted image 20240716173459.png]]
  -  Find the balance of an account in an ERC-20 contract (USDC / USDT)
	  - 查我自己在Polygon上的
	  - https://0xc2132d05d31c914a87c6611c10748aeb04b58e8f.137.w3eth.io/balanceOf/0x1d41D6B1091C1a8A334096771bd1776019243d5e?returns=(uint256)
	  - ![[Pasted image 20240716173742.png]]
  - 

	


- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）
  
  - 一个用来储存的EVM，会面临什么问题？要如何解决？
- TODO：搞懂自动模式跟手动模式的差异，尝试布署合约做下两个Homework
### 07.17

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.18

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.19

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.20

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.21

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

<!-- Content_END -->
