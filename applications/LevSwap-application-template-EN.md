# Open Grant Proposal

* **Project Name:** LevSwap
* **Team Name:** Up Labs
* **Payment Address:** 比特币 或 以太坊(DAI) 的收款地址。我们暂时不会接收其它币种。(例如 123mp123...)

## Project Overview :page_facing_up:
Levswap is a never-ending and easy-to-use trading platform based on synthetic asset leverage tokens. 
Users can use bar trading on LevSwap to magnify their asset returns in the form of buying and selling tokens.

### Overview
  In the outbreak of DeFi in 2020, the top 10 market capitalization projects include the exchange ,Yield Farming Aggregators (e.g. YFI), lending (e.g. aave), synthetic token (e.g. synthetixs) and etc. It is not difficult to find that improving the utilization rate of funds is the real demand of the market, then one product must be mentioned,--lever trading which is also an indispensable part of traditional financial transactions. This can be proved by the trading volume of leverage and futures products of centralized exchanges.
  
  LevSwap will implement lever trading in a decentralized environment in the form of synthetic assets. 
  Users can use the operation mode of DEX to buy and sell the corresponding synthetic asset tokens to do long and short. LevSwap uses the Swap token model to get rid of the margin model, customers in the extreme market will not burst, And LevSwap can effectively improve the safety of customer funds, and reduce risks. Through the calculation of the long-short force, LevSwap can adjust the leverage ratio in real time, Combining with the transaction rate, LevSwap can balance the long-short force, guide the return of the token price, and improve the effectiveness of the transaction.

    
   Our team comes from the top blockchain companies and financial institutions in the industry. Members have participated in the development of allied chain and several Dapp projects, and have a deep understanding and accumulation of blockchain technology and research. After our investigation and discussion, we found that some transaction efficiency problems of the main network (lag and high gas fee), these problems can not be solved on the main network. After studying the technology of polkadot and Substrate, we find that the advanced technology of polka can fit our project very well. at the same time, LevSwap, based on the transaction of synthetic assets can well cater to the cross-chain needs of assets generated for long-short transactions in other networks (such as etherum network). In a sense, it realizes the asset link between polka and other networks.
    
### Project Details
    
  <img width="1439" alt="LevSwap UI" src="https://user-images.githubusercontent.com/24887514/109506388-88b4b180-7ad8-11eb-845a-2fcd20a92697.png">
  The structure of LevSwap mainly consists of three parts: Tokens,Pricing,Swap, can be subdivided into five functional modules: token synthesis, token management, subject matter pricing, leverage ratio adjustment and dynamic rates.  
  
  ![Levswap feature](https://user-images.githubusercontent.com/24887514/109508258-a2ef8f00-7ada-11eb-917e-f97b8c3e9dc0.png)

  #### Synthetic tokens
  The LevSwap platform introduces two kinds of synthetic tokens as long-short representatives of the subject matter of the transaction. 
Users directly open long/short positions by buying bull tokens and bear tokens, and close long/short positions by selling. The number of bull tokens and bear tokens represents the size of the corresponding positions of users, and the tokens are priced based on eth standard, so users can indirectly get the asset changes of eth standard through the balance of synthetic tokens.
  #### Governance tokens
  The project will give rewards to the users who hold the position, and the rewards will be realized through the issuance of governance tokens. 
At the same time, in the adjustment of long-short ratio, price regression, will also be achieved through the issuance of governance tokens. 
  #### Pricing
  For the pricing of the subject matter, we use the oracle machine of UniSwap to avoid the risk of the subject matter price at the transaction level. 
The pricing of synthetic tokens will be determined by bull token and bear token pools. 
  #### Leverage ratio
  Each subject has a desired leverage ratio, which deviates from the powerful side in the case of long-short imbalance, until the long-short force is balanced and the leverage ratio returns to the original ratio. 
This can intuitively tell the trader that the rate of return of the current transaction. 
  #### Dynamic fee
  Fee is the main means to realize the long-short balance of leveraged trading. 
LevSwap uses dynamic fee. According to the current different long-to-empty ratio, LevSwap will update the poundage in real time when the user trades, to guide the multi-empty force back to balance. 
The adjustment is dynamic and directly reflects the strength of the current long/short force.
  ![LevSwap strcuture](https://user-images.githubusercontent.com/24887514/109508315-b4389b80-7ada-11eb-8478-f1efe9ca56f7.png)

  There is a LeveragePair contract for each asset, which provides an interface for buying and selling leveraged tokens and adding liquidity. 
LeveragePair contracts are interfaced with long/short  token contracts (ERC20), such as buying long tokens, which is equivalent to LeveragePair calling LongToken's mint interface to mint tokens. 
Pair contracts provide a series of query interfaces for display, such as leverage ratio, capital rate, leverage token price, etc.

### Ecosystem Fit
There are no similar projects in Polka ecology. 
In the ethereum network ecology, there are Futureswap, Synthetix and etc. 
  
Difference: 
  
1. Compared to Futureswap:   
Futureswap is a perpetual contract trading platform implemented in DEX, while LevSwap is a leveraged trading platform realized through synthetic tokens on DEX. 
Futureswap directly uses usd to do long and short operations on targets such as eth. 
On the other hand, LevSwap uses trading long-short tokens to achieve long-short operations on the subject matter. 
Based on this design, LevSwap's long-short leveraged trading will not burst, which can avoid asset risk in extreme market for customers.

2. Compared to Synthetix:   
Synthetix establishes long/short trading pool of the corresponding assets in the way of B2C, and the operation of the online is performed by the platform, and the long/short pool is relatively independent, so there will be inconsistent pricing for the same kind of underlying transaction pair. 
LevSwap is aimed at the price of a subject matter, directly through the purchase of Bull tokens and Bear tokens to achieve leveraged trading and dynamic multiple leverage transactions. Long-short forces will directly produce the game. 
The selection of the subject matter pool is carried out by the community, and anyone can set up a liquidity pool corresponding to the target for leveraged trading. 
LevSwap is a leveraged trading platform realized through synthetic asset tokens. It is an innovative platform that combines synthetic assets, trading and leverage functions into one product. 
LevSwap not only keeps the products at the basic level, but also has real application-level requirements, so it is different from the above products.
  
## Team :busts_in_silhouette:

### Team Member
* **Rudy Tang:** Senior Blockchain Developer, Head of Blockchain Technology Research.3 years Blockchain Research and Design Experience, 6 years architecture and development Experience.
* **Simon Huang:**   
* **Xin Ge:**  
* **Mike Zhang:**  
* **Rhyme Peng:**  
* **Bk Li:**  Former senior product manager of the world's top 500 financial institutions with rich experience in financial products.


### 联络方式
* **联络人:** 联络人全名 (例如 陈大文)
* **电邮:** 联络人电邮 (例如 john@duo.com)
* **Website:** http://levswap.com

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
