# Open Grant Proposal

* **项目名称:** LevSwap
* **团队名称:** Up Labs
* **收款地址:** 比特币 或 以太坊(DAI) 的收款地址。我们暂时不会接收其它币种。(例如 123mp123...)

## 项目概览 :page_facing_up:
Levswap is a never-ending and easy-to-use trading platform based on synthetic asset leverage tokens. 
Users can use bar trading on LevSwap to magnify their asset returns in the form of buying and selling tokens.

### 概览
  在2020年DeFi大爆发，前10市值项目除去交易所就是机枪池yfi、借贷aave、合成代币synthetixs等分类，通过分析不难发现，提高资金利用率是市场的真需求，那么其中一个不可不谈的就是杆杠交易，同时杆杠交易也是传统金融交易中不可或缺的一部分，从中心化交易所的杆杠和期货产品的交易量就可以证明这一点。
  LevSwap将在去中心化的环境中，以合成资产的方式，实现杆杠交易。用户可以以dex的操作方式，买入卖出对应标的的合成资产代币，来做多做空标的物。LevSwap使用了Swap token的模式，摆脱了保证金的模式，客户在极端行情下也不会发生爆仓，可以有效率提高客户资金的安全，降低风险。LevSwap通过对多空力量的计算，可以实时的调整杆杠倍率，结合交易费率，来平衡多空力量，引导代币价格回归，提高交易的有效性。  
    
   我们的团队来自业内顶级的区块链公司以及金融机构，成员曾经参与过联盟链及多个Dapp项目开发，对于区块链技术和研究有较深的理解和积累。在我们碰撞出项目的火花后，发现主网的一些交易效率问题（滞后及gas费昂贵），
这些问题并不能在主网上解决。而在我们对polkadot和Substrate的技术进行研究后，发现polka的先进技术可以很好的切合我们的项目，同时基于合成资产的交易的LevSwap，可以很好的迎合一部分为了在其他网络（例如主网）
进行多空交易而产生的资产跨链的需求，某种意义上，实现了polka和其他网络的资产链接。
    
### 项目详细资料
我们希望团队对项目的预期最终成果已经有扎实的想法。   
    
  <img width="1439" alt="LevSwap UI" src="https://user-images.githubusercontent.com/24887514/109506388-88b4b180-7ad8-11eb-845a-2fcd20a92697.png">
  LevSwap的架构中主要包含三大板块：Tokens，Pricing，Swap，细分为5个功能模块：代币合成、代币治理、标的物定价、杆杠倍率调整以及动态费率。  
  
  ![Levswap feature](https://user-images.githubusercontent.com/24887514/109508258-a2ef8f00-7ada-11eb-917e-f97b8c3e9dc0.png)

  #### 合成代币
  LevSwap平台引入了两种合成代币作为交易标的物的多空代表。用户直接通过买入牛币和熊币实现多空的开仓，通过卖出实现多空的平仓，牛币和熊币的数量代表了用户对应方向的持仓量的大小，代币采用eth本位进行定价，由此，用户可以直接通过代笔余额间接得出eth本位的资产变化。
  #### 治理代币
  项目对于持仓的用户会给予持仓奖励，激励通过发放治理代币实现。同时，在调节多空比例，做价格回归时，也会通过发放治理代币实现。
  #### 定价
  对于标的物的定价，我们使用了uniswap的预言机，来避免标的物价格在交易级别上的风险。而合成代币的定价，将由bull token和bear token两个池子共同决定。
  #### 杆杠倍率
  每一个标的物都有一个期望的杠杆倍率，在多空不平衡的时候，杠杆倍率会向力量大的一方偏离，直到多空力量平衡，杠杆倍率回到最初比例。这可以直观的告诉交易者，目前交易的收益回报率，同时不凭借调仓，即可实现杠杆交易。
  #### 动态手续费
  手续费是实现杆杠交易多空平衡的主要手段。LevSwap采用了动态手续费，即根据当前不同的多空比，在用户交易时实时更新手续费，来引导多空力量回到平衡。调整是动态的，直接反应了当前多空力量的强弱。
  ![LevSwap strcuture](https://user-images.githubusercontent.com/24887514/109508315-b4389b80-7ada-11eb-8478-f1efe9ca56f7.png)

  对应每种资产都有一个LeveragePair合约，该合约提供买卖杠杆代币、添加流动性的接口；
LeveragePair合约对接了多、空杠杆代币合约（ERC20），比如买做多杠杆币，相当于LeveragePair调用了LongToken的mint接口铸造代币；
Pair合约提供了一系列查询接口，用于展示，比如杠杆倍率、资金费率、杠杆代币价格等等；

### 生态合适
波卡生态中，还没有与我们相似的项目。在主网生态中，有futureswap、synthetixs等。  
区别：  
  
1.与Ftureswap相比：  
  Futureswap是在dex实现的永续合约交易平台，而levswap是在dex上通过合成代币实现的杠杆交易平台。Futureswap直接使用usd对eth等标的进行做多做空操作，
而levswap则是用买卖多空代币来实现对标的物多空操作。基于该设计，levswap的多空杆杠交易是不会发生爆仓，能为客户避免极端行情下的资产风险。 
  
2.与Synthetixs相比：    
  Synthetix以B2C的方式建立了对应的资产的固定一倍多空池，上线流动性池的操作由平台执行，且多空池是相对独立的，所以会出现对同一种标的的交易对的多空定价不一致的情况。  
  而Levswap是针对一个标的物的价格，直接通过购买Bull币以及Bear币实现多空的开仓，实现的动态倍率杠杆交易，多空力量会直接产生博弈。标的物池子的选择是由社区执行的，类似uniswap，任何人都可以建立对应标的的流动性池子，进行杠杆交易。    
  LevSwap是通过合成资产代币实现的杆杠交易平台，是一个创新的将合成资产、交易和杠杆功能融合为一个功能的平台。LevSwap不仅仅将产品停留在基础层，而有真正的应用层面的需求，所以是有别于以上的产品的。  
## 团队 :busts_in_silhouette:

### 成员
* 联络人名称
* 组员名称
* 
* **Rudy Tang:** Senior Blockchain Developer, Head of Blockchain Technology Research.3 years Blockchain Research and Design Experience, 6 years architecture and development Experience.
**Simon Huang:**   
**Xin Ge:**  
**Mike Zhang:**  
**Rhyme Peng:**  
**Bk Li:**  


### 联络方式
* **联络人:** 联络人全名 (例如 陈大文)
* **电邮:** 联络人电邮 (例如 john@duo.com)
* 网页

### 法律结构
* **注册地址:** 您注册的法人实体的地址 (如果有)。 请保持在同一行。(例如 High Street 1, London LK1 234, UK)
* **注册法人实体:** 您的注册法人名称（如果有)。(例如 Duo Ltd.)

### 团队经验
请描述团队的相关经验。如果项目涉及开发工作，我们将会很有兴趣您能挑出团队成员在过去的项目中所做出的一些有趣的代码成果。对于与研究相关的拨款，请参考相关领域中的过去项目。

### 团队 Github 代码库
* https://github.com/<your_repo_1>
* https://github.com/<your_repo_2>

### 团队 LinkedIn 资料
* https://www.linkedin.com/<person_1>
* https://www.linkedin.com/<person_2>

## 开发路线图 :nut_and_bolt:

本节应将开发路线图划分为多个里程碑。由于里程碑将出现在拨款合同中，因此有助于描述我们应该期望的功能，以及我们如何检查产品中是否存在此功能。每当交付里程碑时，我们都会参考合同以确保一切均按预期交付。

下面我们提供了一个**路线图例子**。 在描述中，应该清楚说明项目与 Substrate 或与 Polkadot 的关系。 我们建议工作范围应在3个月内，并且团队将路线图的结构定为1个月= 1个里程碑。

在每个里程碑:
* 请确保包括您的软件规范。将其视为合同 - 详细程度必须足以验证稍后软件是否符合规格。为了帮助您定义，我们在[此处](../src/grant_guidelines_per_category.md)建立了一个档案，其中包含一些拨款类别的例子。
* 请列出每个里程碑需求的资金总额。
* 请注意，每个里程碑都需要文档（例如教程，API 规格，架构详细信息)。 这确保了该代码可以被社区广泛使用。
* 请提供一个包含单元测试和集成测试的测试套件，以及有关如何运行它们的教程。
* 请致力提供 dockerfiles 用于交付项目。
* 请指出里程碑的所需时间，以及在每个里程碑上工作的全职员工的人数，并包括日数以及每天的费用。
* 成果(Deliverable) 0a-0d 是强制性的，不可删除，除非您在 PR 的 `其他说明(Additional Notes)` 部分中明确指定了原因（例如 里程碑 X 是面向研究的，因此没有可测试的代码）

### 概览
* **估算总需要时间:** 整个项目需时 (例如 2个月)
* **全职人力工时(FTE):**  受雇人的工作量 ([请参考这里](https://en.wikipedia.org/wiki/Full-time_equivalent)) (例如 2 FTE)
* **总金额:** 整个项目所需要的 BTC 或 DAI 金额。在提交申请时，第一次申請的金额需要低于 $30k 美元 (例如: 0.50 BTC)，而之后接着的申请可以是 $100k。

### 里程碑 1 例子 — 实现 Substrate 模块
* **估计时间:** 1个月
* **FTE:**  1
* **费用:** 0.75 BTC

| 数字(Number) | 成果(Deliverable) | 规范(Specification) |
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 / MIT / Unlicense |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can (for example) spin up one of our Substrate nodes. Once the node is up, it will be possible to send test transactions that will show how the new functionality works. |
| 0c. | Testing Guide | The code will have unit-test coverage (min. 70%) to ensure functionality and robustness. In the guide we will describe how to run these tests |
| 0d. | Article/Tutorial | We will write an article or tutorial that explains the work done as part of the grant.
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be coded for the first milestone) |
| 2. | Substrate module: Y | We will create a Substrate module that will... |
| 3. | Substrate module: Z | We will create a Substrate module that will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Docker | We will provide a dockerfile to demonstrate the full functionality of our chain |

### 里程碑 2 例子 - 额外功能
...

## 未来计划
请包括团队的长远计划和意向。

## 额外资料 :heavy_plus_sign:
任何额外资料你认为对这个申请是相关但是还没有包括。

其他额外资料包括:
* 到目前为止已经做了什么工作？
* 是否有其它团队已经有在财务上为该项目做出了贡献?
* 你是否已经申请了其它的拨款?
