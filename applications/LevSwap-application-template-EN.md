# Open Grant Proposal

* **Project Name:** LevSwap
* **Team Name:** Up Labs
* **Payment Address:** 0xFB48Fd1F94e54532d9fA1432637324F64Ad1234A

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
* **Simon Huang:** Former crypto wallet product director, experienced in asset manage solution and DeFi protocol design.Former PM in top 500 financial institutions.
* **Xin Ge:**  
* **Mike Zhang:**  
* **Rhyme Peng:**  
* **Bk Lee:**  Former senior product manager of the world's top 500 financial institutions with rich experience in financial products.


### Contact
* **Contact Name:** BK Lee
* **Contact Email:** bk@up-protocol.io
* **Website:** http://levswap.com

### Team’s experience

The core team members have rich experience in blockchain system developing, including consensus, p2p, evm and smart contract. They have ever maintained a well-known enterprice blockchain platform.
The team also has related experience in DeFi protocol design and developing.


### Team Code Repos
* https://github.com/levswap

## Development Roadmap :nut_and_bolt:
We expect that the entire project will be split into two grants. The first grant includes the development of token synthetic and the implementation of core modules. We will implement the basic transfer operation ability of a synthetic token in the test network, which can be tested normally.And in this grant we will implement pricing the synthetic token which represent long and short. The second grant will include the development of a complete product.We will realize the calculation and display of dynamic fee and real-time leverage ratio, and increase the mainstream composite assets.And the leveraged trading will be ompletely and smoothly.

    -----------------------------------------------------------
    | Substrate chain with mint & pricing module               |  <---- This grant
    -----------------------------------------------------------
    | Realize dynamic fee and exchange module                  |  <---- Future grant
    -----------------------------------------------------------
    | More synthetic Assets and support community list         |
    -----------------------------------------------------------


### Overview

* **Total Estimated Duration:** 3 months
* **Full-time equivalent (FTE):**  5
* **Total Costs:** 1.35 BTC

### Milestone 1 — Implement Substrate mint&pricing Module

In this milestone, we developed the mint module and the pricing module. we will complement mint synthetic assets tokens--bull and bear, while the synthetic assets can be pricing successful. After completing this milestone, we can basically transfer the casting synthetic assets tokens which is represant long and short .

* **Estimated Duration:** 1 month
* **FTE:**  5
* **Costs:** 18000DAI

| Number | Deliverable  | Specification                                                                                                                                                                                                                                                          |
| ------------ | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. | Documentation | Instructions and examples for use mint  and pricing        |
| 2. | Testing Guide | provide test suite (mock and test files) for the mint and pricing describing how the module can be tested. |
| 3. | Substrate module: mint | We will create a Substrate module mint. Bull tokens and Bear tokens can be minted. |
| 4. | Substrate module: pricing | We will create a pricing module that both the target price and the long/short tokens‘ price can be successfully acquired and displayed. |
| 5. | Tutorial | We will write an tutorial about how to use mint & pricing. |
| 6. | Testing | The code will have proper unit-test coverage to ensure functionality and robustness. |
| 7. | Docker | We will provide a dockerfile to demonstrate the full functionality of our chain with mint  and pricing moudle. |                                                                                                                                                                                             |

### Milestone 2 — Implement Substrate exchange Module

At this milestone, we developed the exchange module. The first milestone has been able to mint synthetic assets. When this milestone is completed, our synthetic assets will be available for trading.Meanwhile，the dynamic fee function will also run normally when the user is trading.

- **Estimated Duration:** 2 month
- **FTE:**  5
- **Costs:** 12000DAI

| Number | Deliverable                | Specification                                                |
| ------ | -------------------------- | ------------------------------------------------------------ |
| 0.     | License                    | Apache 2.0                                                   |
| 1.     | Documentation              | Instructions and examples for use exchange.                  |
| 2.     | Testing Guide              | provide test suite (mock and test files) for the exchange describing how the module can be tested. |
| 4.     | Substrate module: Exchange | We will create a exchange module that will be used to trade synthetic assets. And dynamic fee is also implemented in the exchange module. |
| 5.     | Tutorial                   | We will write an tutorial about how to use exchange. |
| 6.     | Testing                    | The code will have proper unit-test coverage to ensure functionality and robustness. |
| 7.     | Docker                     | We will provide a dockerfile to demonstrate the full functionality of our chain with exchange module |

## Future Plans
In the future, we will support more leveraged trading of synthetic assets, such as stocks and gold, and will explore portfolio possibilities with other projects in Boca Ecology. 
Fight for the goal that “all things can be synthesized and leveraged”.

## Additional Information :heavy_plus_sign:
So far we have completed the project possibility verification evaluation, completed the Substrate-based architecture design, and released the project white paper.
