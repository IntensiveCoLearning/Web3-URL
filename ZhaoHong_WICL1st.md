---
timezone: Asia/Bangkok
---

# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# ZhaoHong

1. **自我介绍：**

  Web2 Full Stack Developer and Web3 Explorer

2. **组队期待：**

  暂时还没项目想法，有需要队员的项目可以参与其中。

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

  Yes 100%

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

- 今日学习时间：30min
- 学习内容小结：将学习材料全部浏览了一遍，公开课没有回放明天再看看。
- Homework 部分（如果有安排需要填写证明完成）
- Question and Ideas（有什么疑问/或者想法，可以记在这里，也可以分享到共学频道群讨论交流）

### 07.16

- 今日学习时间：30min
- 今日学习内容小结：通过视频转图文回看了公开课内容。

可通过下面链接查看图文：
https://l3ob.notion.site/Web3-URL-1-0cdfdb7041d94b6eab6b64d43b9a511c

部分识别不够准确，不过不影响主要意思。

### 07.17

- 今日学习时间：30min
- 学习内容小结：尝试做一下作业。
- Homework 
  - Find the ownership of an your favor NFT
    - CryptoPunks ID 为 1 的 NFT 
    - https://0xb47e3cd837ddf8e4c57f05d70ab865de6e193bbb.w3eth.io/punkIndexToAddress/1?returns=(address)
  - Find the balance of an account in an ERC-20 contract (USDC / USDT)
    - 看看 Vitalik 有多少 USDT
    - https://0xdac17f958d2ee523a2206206994597c13d831ec7.w3eth.io/balanceOf/vitalik.eth?returns=(uint256)

剩下两个留着明天再做。

### 07.19

- Homework
  - Deploy a contract in auto model and say “hello world”
    - https://0xcced993cea00aa983adc6ab9a6c1348f470da703.11155111.w3link.io/greet
    - https://0xcced993cea00aa983adc6ab9a6c1348f470da703.11155111.w3link.io/greet?returns=(string)
  - Deploy a contract in manual model and say “hello world”
    - https://0x401407b9884fdf0978ae166e9f233d884390dc55.11155111.w3link.io/

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.0;

contract HelloWorld {
    function greet() public pure returns (string memory){
        return "hello world";
    }

    function resolveMode() external pure returns (bytes32) {
        return "manual";
    }

    fallback(bytes calldata cdata) external returns (bytes memory) {
        if(cdata.length == 0 || cdata[0] != 0x2f) {
            return bytes("");
        }

        if (cdata.length == 1) {
          return bytes(abi.encode("hello world"));
        }

        return abi.encode("Not found");
    }
}
```

### 07.20

- Homework
  - Claim EthStorage Testnet tokens
    - 0x9CBd3D6A36cf2d45442fD35Dc160c97f658F8B18
  - Upload a file via web3box and paste link
    - https://galileo.web3q.io/file.w3q/0x9cbd3d6a36cf2d45442fd35dc160c97f658f8b18/WechatIMG153.jpg
  - Write  a blog and paste link
    - https://w3-blog.w3eth.io/#/blog/0xfaf99Fb2Ffaab74F5262756D6CC55f1598d4298e/0

### 07.22

- Homework
  - Use ethfs-uploader to upload a folder

```bash
ethfs-cli create -p $KEY -c 3334
# FlatDirectory Address: 0x005d3A77B67e951540810e29ac3ba46bE9e61282

ethfs-cli upload -f dist -a 0x005d3A77B67e951540810e29ac3ba46bE9e61282 -c 3334 -p $KEY
```

https://0x005d3a77b67e951540810e29ac3ba46be9e61282.3334.w3link.io/index.html


### 07.23

- Homework
  - Challenge: Use ERC6944 to
    - return a uncompressed compressed data 
    - determine a customized MIME

```
function request(string[] memory resource, KeyValue[] memory params) external view returns (uint statusCode, string memory body, KeyValue[] memory headers);
```

遇到一个问题，接口的body是string类型，而文件数据应该是bytes类型，要如何兼容呢？

### 07.24

接上面，测试下来返回 bytes memory 的数据是可以兼容的。

```
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;

import "https://raw.githubusercontent.com/ethstorage/evm-large-storage/master/contracts/ERC5018.sol";

contract FlatDirectoryWithResourceRequest is ERC5018 {
    struct KeyValue {
        string key;
        string value;
    }

    bytes public defaultFile = "";

    constructor(uint8 slotLimit, uint32 maxChunkSize, address storageAddress) ERC5018(slotLimit, maxChunkSize, storageAddress) {}

    function resolveMode() external pure virtual returns (bytes32) {
        return "5219";
    }

    // 比较两个字符串是否相等
    function compareStrings(string memory a, string memory b) private pure returns (bool) {
        // 将字符串转换为字节数组
        bytes memory bytesA = bytes(a);
        bytes memory bytesB = bytes(b);
        
        // 比较长度
        if (bytesA.length != bytesB.length) {
            return false;
        }
        
        // 比较每个字节
        for (uint i = 0; i < bytesA.length; i++) {
            if (bytesA[i] != bytesB[i]) {
                return false;
            }
        }
        
        return true;
    }

    function joinStrings(string[] memory strings) public pure returns (string memory) {
        // Step 1: 计算连接后的字符串的总长度
        uint totalLength = 0;
        for (uint i = 0; i < strings.length; i++) {
            totalLength += bytes(strings[i]).length;
        }
        
        // 加上分隔符的长度
        totalLength += strings.length - 1;

        // Step 2: 创建一个新的字节数组并拼接字符串
        bytes memory result = new bytes(totalLength);
        uint k = 0;
        for (uint i = 0; i < strings.length; i++) {
            bytes memory strBytes = bytes(strings[i]);
            for (uint j = 0; j < strBytes.length; j++) {
                result[k++] = strBytes[j];
            }
            // 添加分隔符，但不在最后一个字符串后添加
            if (i < strings.length - 1) {
                result[k++] = '/';
            }
        }

        return string(result);
    }

    function request(string[] memory resource, KeyValue[] memory params) external view returns (uint statusCode, bytes memory body, KeyValue[] memory headers) {
        string memory pathinfo;
        uint chunks = 0;
        
        if(resource.length > 0) {
            pathinfo = joinStrings(resource);
            chunks = countChunks(bytes(pathinfo));

            // /test.txt
            if(compareStrings(pathinfo, "test.txt")) {
                body = bytes("hello world");
                statusCode = 200;
                headers = new KeyValue[](2);
                headers[0].key = "Content-Type";
                headers[0].value = "application/octet-stream";
                headers[1].key = "Content-Disposition";
                headers[1].value = "attachment; filename=\"test.txt\"";
            } else if(compareStrings(pathinfo, "index.html.gz/decompress")) {
                statusCode = 200;
                (body, ) = read(bytes("index.html.gz"));
                headers = new KeyValue[](3);
                headers[0].key = "Content-Type";
                headers[0].value = "application/octet-stream";
                headers[1].key = "Content-Disposition";
                headers[1].value = "attachment; filename=\"index.html\"";
                headers[2].key = "Content-Encoding";
                headers[2].value = "gzip";
            } else if (chunks > 0) {
                statusCode = 200;
                (body, ) = read(bytes(pathinfo));
            } else {
                statusCode = 404;
                body = bytes("Not Found");
            }
        } else {
            statusCode = 200;
            headers = new KeyValue[](2);
            headers[0].key = "Content-type";
            headers[0].value = "text/html; charset=utf-8";
            headers[1].key = "Content-Encoding";
            headers[1].value = "gzip";

            (body, ) = read(bytes("index.html.gz"));
        }
    }

    fallback(bytes calldata pathinfo) external returns (bytes memory)  {
        bytes memory content;
        if (pathinfo.length == 0) {
            // TODO: redirect to "/"?
            return bytes("");
        } else if (pathinfo[0] != 0x2f) {
            // Should not happen since manual mode will have prefix "/" like "/....."
            return bytes("incorrect path");
        }

        if (pathinfo[pathinfo.length - 1] == 0x2f) {
            (content, ) = read(bytes.concat(pathinfo[1:], defaultFile));
        } else {
            (content, ) = read(pathinfo[1:]);
        }

        StorageHelper.returnBytesInplace(content);
    }

    function setDefault(bytes memory _defaultFile) public onlyOwner virtual {
        defaultFile = _defaultFile;
    }
}
```

https://0x12194f1f2e7eecb33dbf68bc74f909f51262b72d.3334.w3link.io/

- return a uncompressed compressed data 
  - https://0x12194f1f2e7eecb33dbf68bc74f909f51262b72d.3334.w3link.io/index.html.gz/decompress

- determine a customized MIME
  - https://0x12194f1f2e7eecb33dbf68bc74f909f51262b72d.3334.w3link.io/test.txt

### 07.25

w3box：从 https://github.com/ethstorage/awesome-web3 中选取第一个 app 来学习。

访问地址：https://w3-box.w3eth.io/

查了一下使用的是夸克链测试链，领水：https://qkc-l2-faucet.eth.sep.w3link.io/

上传了一个小文件，花费很少，文件地址：https://0x6c00359069c658a42129dc54e801e47bdff0db27.3336.w3link.io/0x9cbd3d6a36cf2d45442fd35dc160c97f658f8b18/IDecentralizedApp.sol

再测试稍大一点的文件（2M+）无法上传

下一步准备看看代码排查一下问题：https://github.com/ethstorage/w3box

### 07.26

项目想法：
https://github.com/IntensiveCoLearning/Web3-URL/discussions/166

<!-- Content_END -->
