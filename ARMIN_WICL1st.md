# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为 WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   ARMIN，一名好奇心旺盛的应届生，擅长 Solidity 合约开发，熟悉前端，对 web3:// protocol 很感兴趣，所以来学习学习

2. **组队期待：**

   暂时还没什么想法，随时更新~

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   Maybe 80%

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

- 今日学习时间：1.5h
- 学习内容小结：学习了 PPT 中的内容，有些地方不太懂，明天继续
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.16

- 今日学习时间：2h
- 学习内容小结：补完了昨天的腾讯会议，看了一下技术文档以及 awesome-web3 中的一些应用
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas：感觉有很多东西可以去做，有了一些大致的想法，关于什么需要上链这个古老的问题还是需要再斟酌一下

### 07.17

- 今日学习时间：0.5h
- 学习内容小结：今天比较忙，继续看了https://docs.web3url.io/这个文档
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.18

- 今日学习时间：0.5h
- 学习内容小结：写了一部分作业
- Homework 部分：

#### 1. Find the ownership of an your favor NFT

在 Chrome 输入以下 URL：

```
https://0xed5af388653567af2f388e6224dc7c4b3241c544.w3eth.io/ownerOf/123?returns=(address)
```

返回值：

```json
["0x2aE6B0630EBb4D155C6e04fCB16840FFA77760AA"]
```

#### 2. Find the balance of an account in an ERC-20 contract (USDC / USDT)

在 Chrome 输入以下 URL：

```
https://0xdac17f958d2ee523a2206206994597c13d831ec7.w3eth.io/balanceOf/0x1648ce7e8Ac365aFc64e6FAAb810A3AB8404C69E?returns=(uint256)
```

返回值：

```json
["0x4820900b"]
```

转换成十进制：

```javascript
const amount = parseInt(0x4820900b);
console.log(amount);
```

返回值：

```
1210093579
```

#### 3. Deploy a contract in auto model and say “hello world”

没了解过 auto model 和 manual model，明天查查。

- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.19

- 今日学习时间：0.5h
- 学习内容小结：完成了作业
- Homework 部分

#### 3. Deploy a contract in auto mode and say “hello world”

Sepolia 合约地址：

```
0x6886ea01840dbe9f11082950cc96beac3f618f72
```

合约代码：

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract helloWorld{
    function printHelloWorld() public pure returns(string memory){
        return "Hello World";
    }
}
```

因为是默认的解析模式，合约中不存在 resolveMode 方法时便会通过 auto mode 解析
在 Chrome 中输入：

```
https://0x6886ea01840dbe9f11082950cc96beac3f618f72.sep.w3link.io/printHelloWorld
```

返回值：

```
Hello World
```

#### 4. Deploy a contract in manual mode and say “hello world”

Sepolia 合约地址：

```
0x97345e8c3343dcd0636d73feab40087cdf10ff66
```

合约代码(借鉴了https://docs.web3url.io/web3-url-structure/resolve-mode/mode-manual)：

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract helloWorld{
    function printHelloWorld() public pure returns(string memory){
        return "Hello World";
    }

        function resolveMode() external pure returns (bytes32) {
        return "manual";
    }
    // Fallback function to handle manual mode calls
    fallback(bytes calldata cdata) external returns (bytes memory) {
        // Check if calldata is empty or does not start with '/'
        if (cdata.length == 0 || cdata[0] != 0x2f) {
            return bytes("");
        }

        // Handle "/printHelloWorld"
        if (cdata.length == 16 && keccak256(cdata[1:16]) == keccak256("printHelloWorld")) {
            return abi.encode(printHelloWorld());
        }

        // Default case: return "Not found"
        return abi.encode("Not found");
    }
}
```

这次指明 resolveMode 为 manual mode，并通过 fallback()处理请求
在 Chrome 中输入：

```
https://0x97345e8c3343dcd0636d73feab40087cdf10ff66.sep.w3link.io/printHelloWorld
```

返回值：

```
Hello World
```

- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.20

- 今日学习时间：0h
- 学习内容小结：今天休息一下
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.21

- 今日学习时间：1h
- 学习内容小结：系统性了解了 Filecoin、IPFS、Arweave 和 Ethstorage 的区别，不过 Ethstorage 文档中讨论技术比较多，并没有提到共识机制、经济模型等，期待明天的课中能有说明
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.22

- 今日学习时间：1h
- 学习内容小结：看了一下https://github.com/ethstorage/awesome-web3中的项目，想挑战一下独立完成项目
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

<!-- Content_END -->
