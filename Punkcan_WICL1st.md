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



### 07.17

- 今日学习时间：1h
- 学习内容小结：
	- \/\<methodName\>\/\<methodArg1\>\/\<methodArg2\>\/...[?returns=(\<type1\>,<type2>,...)]
	- URL一次只会对一个方法进行呼叫，因此URL第一格一定是方法
	- 如果该方法有多个输入（Arg），就依序列出，returns也依序列出他们的类型（type，如果多个值要列出多个）
	- Arguments 的格式是自动辨识的，辨识顺序如下
	- uint256，bytes32，address，bytes，bytes
	- ?returns=如果没有指定，预设为bytes（但如果回传不是bytes，就会发生错误）
	- 回传的整个内容是JSON
	- 也就是说如果用来储存网页内容，可以将合约写成一次输出多个值，回传就一个JSON，我们在用parse去取值，这样速度也快
	- 如果returns有()但填入任何值，就会返回十六进制字符串，例如  ["0xAB9e1DDf806a20C9B06A94c655a59C3eDF495Ca5"]就会变成["0x000000000000000000000000ab9e1ddf806a20c9b06a94c655a59c3edf495ca5"]，通常解析原始数据时会用到
	- 最后一个参数是媒体类型
	- web3://0x4e1f41613c9084fdb9e34e11fae9412427480e56/tokenSVG/9352?mime.type=svg，这样可以指定输出成SVG格式
	- 换成https 就是 https://0x4e1f41613c9084fdb9e34e11fae9412427480e56.w3eth.io/tokenSVG/9352?mime.type=svg
	- Auto mode 跟 manual mode的差异
		-  这两个模式是合约上设定的，一般来说，合约并没有考量到Web3URL的需求，就不会开manual模式，大多数状况下采用auto
		- 要采用manual模式，智能合约要打开接口

			```js
				function resolveMode() external pure returns (bytes32) {
		        return "manual";
			    }
			```

		- 我们可以这样理解，如果要读取出图片或是页面，manual可以有比较多的操作空间
		- manual模式，预设回传的是text/html 的MIME
		- 另外要写上一个fallback，fallback是一个包罗万象的函数，当没有适配函数时，就会调用他，但是fallback的gas价格更高，最好避免做写入的行为，另一种类似的函数是receive，当收到eth但是什么要求都没有的时候就会调动receive，专门用来设计例如收到钱就给代币之类的功能，Gas较低
		- fallback是用来作为一个路由，也就是说当有人对这个合约作出calldata的动作，就会吐出fallback的内容，用来将合约当成一个网页特别适用，以下是DOC的范例
		```js
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
		- 如此一来只需要呼叫页面的index，就可以叫出页面内容，并完成encode
	- 重要参考：  **https://etherscan.io/address/0x2b51A751d3c7d3554E28DC72C3b032E5f56Aa656#code**


- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）
	- 如果回传的是JSON，要如何将JSON变成网页呢？



### 07.18

- 今日学习时间：0.5h
- 学习内容小结：
	- 听闻 EIP 6860 跟EIP 4804很类似，研究他们之间的差异是什么？
		- 简单地解释就是6860类似4804的一个扩展，4804虽然更为简化，但也意味着扩展弹性更高，也会有较高的兼容性
		- 对于更加复杂的使用，EIP 6860提供更多功能，例如更多的MIME类型等等
		- 两组的提案跟开发人员基本上一致
	- Resource request mode 目前还在草案
		- 算是将处理HTTP数据的一种补完
		- 可以回传HTTP 标头跟状态代码
		- path的解析转移到浏览器端
		- https://vscode.blockscan.com/ethereum/0x2b51A751d3c7d3554E28DC72C3b032E5f56Aa656 是一个很完整的案例
		-  Chunk support 这部分的概念大概是说可以将内容分成多块
			- 不过测试的时候 web3://0x8e990356262a2f8164981298e167c3ad2409faa1:11155111/getFile/abcd 并没有正常回传，而是后面又接了一段400
			- 
			
				```html
				start<html><h1>400: Bad Request</h1>Unrecognized domain name<html/>
				```
			- web3://0x8e990356262a2f8164981298e167c3ad2409faa1:11155111/getFile/abcd?chunk=1 倒是正常了，总之就是可以用来把大型内容分段或是分页
		- Compression 可以将数据压缩后上链，利用这个协议进行解压缩返回给client
		
	
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）
	- 如果目前不知道是透过网关去读取合约还是读取合约后透过网关转译内容，如果是先读取合约，如果是「读取合约后透过网关转译内容」，可否在合约里定义网关清单之类的？
	- 网关如果被和谐了，一般用户如何知道怎么修改网关？
	- 网关的架设能否有激励制度？
	- 

### 07.19

- 今日学习时间：0.5h
- 学习内容小结：
	- 网关
		- 网关的原理是将http的请求转换成web3protocol-go能处理的web3://
		- 目前firefox的addon，是先转web3://的链接为https://的链接，然后送给网关去获取需求
		- 也就是说未来如果有浏览器原生支援，就不需要网关了
		- 目前有w3link.io多链跟w3eth.io主网单链两个官方项目网关
		- 不过目前多链网关有支援的范围，不是所有测试网都可以用（之前看还没有支援holesky，目前已经加入支援）
		- 目前有一款项目方释出的EVM Browser，Chrome extension 对安全需求高，无法上架
		- https://w3-sandbox.eth.eth.w3link.io/ 是一个sandbox，可以测试完成的web，回传数据的细节，跟Dev视窗相比，比较能清楚分出哪些Web3数据
		- Web3curl 虽然是用来调试的，可以实践web3://的脚本化
		- web3curl -v可以列出调试细节
		- 最后一个（我觉得）比较重要的是[web3protocol-js](https://github.com/web3-protocol/web3protocol-js) ，从源码粗浅的看来，似乎可以让一般https的网站链接获取到web3://的资源，甚至可以跳过网关，因为他这跟EVM节点API交互，而不是跟网关交互
		- 还有web3protocol-go，这是做网关的关键，不过我不熟悉Go
		- 
	- ethfs-uploader
		- 算是一个档案上传的工具，可以透过npm安装
		- 算是给不会写合约的用户一个方便的模式
		- 第一步可以用来创建目录合约，这个合约可以方便你之后上传档案
		- 上传文件时，呼叫合约为了要辨识是哪一条链，要去查一下链的缩写[the EIP-3770 address](https://eips.ethereum.org/EIPS/eip-3770)，采用EIP-3770 的格式
		- 格式：w3q-g:0x37DF32c7a3c30D352453dadACc838461d8629016
			- 但这里我有点不懂，为什么要用缩写？因为缩写不是很好查询
		- 完整的上传格式范例 npx ethfs-uploader /Users/.../dist w3q-g:0x37DF32c7... --privateKey 0x112233...
		- 暂时安装不了，无法实操，过两天再弄
		- 
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.20

- 今日学习时间：0.5h
- 学习内容小结：
	- ethfs-sdk ，可以让档案的存取建档等等脚本化，或是写成web界面来操作
	- 尝试申请W3NS，但是无法正常申请，已经提交issue
	- ERC-5018 是一个以太坊改进提案（EIP），它定义了一个类似文件系统的接口，用于以太坊区块链上的合约。该提案制定了一套API，用于在智能合约中管理目录和文件，使其能够读写任意大小的二进制对象。特别地，如果对象太大，不适合在单一交易中处理，该标准还支持分块处理功能。主要功能包括：
		- **写入（Write）**：在目录中为文件写入数据。
		- **读取（Read）**：从目录中的文件读取数据。
		- **文件大小和块（Size and Chunks）**：获取文件的大小以及数据块的数量。
		- **删除（Remove）**：删除目录中的文件。
		- **分块操作（Chunk Operations）**：对大文件进行分块写入、读取和删除操作，以适应单次交易的数据大小限制。
	- 也就是说5018可以解决上传档案太大的问题
	- 基本上DOC都看完了，花了六天，该开始写合约了
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.21

- 今日学习时间：0.5 h
- 学习内容小结：
	- 布署开发合约的环境，包括remixd，完成环境设定，但还没开始开发（更新remixd花太多时间了）
	- 注册W3NS：punkcan.w3q 完成，之前的失败应该是网络原因
	- Web handler 应该是填写Web3URL要用来呈现http输出的合约地址，暂时还没设定
	- ethfs-uploader安装一直出现「安全提示」，无法完成安装，正在解决中

- Homework 部分（如果有安排需要填写证明完成）

- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.22

- 今日学习时间：1h
- 学习内容小结：
	- 先解决了 npm i ethfs-uploader 的问题，基本上就是把相关套件通通移除后，重新npm cache clean --force，重新update，再进行安装
		- W3Q网路不支援最新的EVM，编译一直出错，后来直接降到柏林后成功
	- 正在写合约
		- Automode: https://0xe5182111d079103e8c02e8f284cde8b47b91f566.3334.w3eth.io/automode
	- 解析fallback的范例
		```js
		fallback(bytes calldata cdata) external returns (bytes memory) {
		// 检查传入的数据长度是否为0，或者数据的第一个字节是否不等于0x2f（即'/'字符）
		// 如果任一条件满足，则返回一个空的字节序列
		if (cdata.length == 0 || cdata[0] != 0x2f) {
			return bytes("");
		}
		// 如果请求只包含一个'/'字符，返回首页内容
		// 调用indexHTML(1)生成首页的HTML内容，并将其编码为字节序列返回
		if (cdata.length == 1) {
			return bytes(abi.encode(indexHTML(1)));
		}
		// 检查是否为形如'/index/[uint]'的请求
		else if (
			cdata.length >= 6 && ToString.compare(string(cdata[1:6]), "index")
		) {
		uint page = 1;
		// 如果路径后有更多字符，尝试解析页码
		if (cdata.length >= 8) {
			page = ToString.stringToUint(string(cdata[7:]));
		}
		// 如果解析页码为0，返回"Not found"
		if (page == 0) {
			return abi.encode("Not found");
		}
		// 否则，调用indexHTML(page)获取指定页码的HTML内容，并编码返回
			return abi.encode(indexHTML(page));
		}
		// 如果以上条件均不满足，返回"Not found"
			return abi.encode("Not found");
		}
		```

	
- Homework 部分（如果有安排需要填写证明完成）
	- https://0xe5182111d079103e8c02e8f284cde8b47b91f566.3334.w3eth.io/automode
	
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）



### 07.23

- 今日学习时间：0.5h
- 学习内容小结：
	- 完成第一阶段最后一项作业，Manual合约
	- 完成测试，并注册多个W3NS，准备规划项目
- Homework 部分（如果有安排需要填写证明完成）
	- https://0x91122cb8e0111ac58ef46278c0a65378692f3563.3334.w3eth.io/index/
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.24

- 今日学习时间：0.5h
- 学习内容小结：
	- 实作ethfs-cli的各项指令，不过这个有点太简单就不写细节了
	- 本地网关架设....这个也有点简单，不过这个我觉得可以写成一个一键安装的套件，最好有GUI，这样大家可以在自己本机开网关
	- 讨论项目进行
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.25

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.26

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.27

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.28

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.29

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.30

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### 07.31

- 今日学习时间：
- 学习内容小结：
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）


### ToDo


- 研究0x2b51A751d3c7d3554E28DC72C3b032E5f56Aa656的架构
- 了解网关如何架设
- Claim EthStorage Testnet tokens(Use a new address)
- Upload a file via web3box and paste link
- Write  a blog and paste link
- Use ethfs-uploader to upload a folder
- Challenge: Use ERC6944 to return a uncompressed compressed data determine a customized MIME
- 研究如果使用web3protocol-js，是否可以不用网关就获取数据


<!-- Content_END -->
