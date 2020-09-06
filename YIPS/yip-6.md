---
yip: 6
title: 为YFII机枪池建立iToken系统
status: WIP
author: YFII Community
discussions-to: https://gov.yfii.finance/
created: 2020-09-06
updated: N/A
---

## 什么是iToken？( What is YFII iToken? )

**iToken**是YFII 核心业务机枪池（Vault）的权益Token。**iToken**承载了YFII的核心业务价值，将投资者存入YFII Vault的普通Token转化为生息Token，并通过机枪池的自动优化收益策略，持续提升iToken的价值。同时iToken符合ERC20标准，可用于与其他DeFi产品进行乐高式组合，生成更为复杂的DeFi衍生品。


**iToken** is the equity token of **YFII Vault**. They carries the core business value of YFII. This will convert ordinary Tokens deposited by investors into interest-bearing Tokens, and continues to increase the inner value of iToken through the automatic optimization of strategies of the **YFII Vault**. At the same time, iToken complies with the ERC20 standard and can be used for Lego-style combination with other DeFi products to generate more complex DeFi derivatives.



## 为什么要开发iToken？对YFII有哪些好处？ （ Why design iToken? What are the benefits for YFII? )

iToken对应于Yearn系统的yToken，是YFII开展后续业务的基础Token。与yToken的差异在于，iToken的收益策略不限于基本借贷，还会延伸至Yield Farming以及未来更广泛的DeFi业务领域。同时iToken在功能上进行了优化，对闪电贷以及巨鲸稀释池内权益等方面做了防范，让投资者的利益得到充分保障。


iToken corresponds to the yToken from Yearn and make them as the cornerstone Token for YFII to carry out following business. The difference with yToken is that iToken's bear interests strategy is not limited to lending, but also extend to Yield Farming and more potential DeFi business in the future. At the same time, iToken has been optimized in terms of functions, and has taken precautions against flashloans and the dilution from whales, so that the benefits of investors are fully protected.



## iToken的机制是怎样的？( What is the mechanism of iToken? )

机枪池（Vault）内每个币种均对应于一个专属iToken，如USDT机枪池产生的权益iToken为iUSDT，代表了用户对机枪池内USDT资产的权益份额。因为机枪池会持续产生收益，iUSDT价格相对于USDT的汇率也会持续提升。


Each token in the Vault corresponds to an exclusive iToken. For example, the equity iToken which generated in USDT Vault will be iUSDT, which represents the user's equity share in the USDT Vault. Because the Vault will continue to generate revenue, the exchange rate of iUSDT price relative to USDT will continue to increase.


## 具体产品设计上有哪些特性？( What are the characteristics of iToken's product design? )

iToken会收取0.2%的提现费，用于防止巨鲸注资稀释其他用户权益

用户资金进入机枪池后，会自动配置该币种下最优挖矿策略，在保证本金安全前提下进行最高收益挖矿。其利润的90%将通过DEX路由自动兑换为本币，从而增加iToken持币者权益。其余的10%利润根据YIP-5的决议进行分配：
1. Harvest收割奖励 1%，用于补贴收割gas费用，同时降低目标矿币转化为本币与YFII时产生的滑点
2. 策略开发者奖励 1%，用于激励合约开发者为机枪池提供策略。此部分资金提供方原为保险基金，保险业务尚未开展，而开发者激励比较紧急
3. 开发者基金 3%，用于YFII 项目可持续发展。包括开发者合约部署、服务器申请等费用报销。以及为运营活动、前端开发、数据工具开发等提供Grant
4. 循环挖矿 5% ，用于激励Vault入金、激励新项目支持YFII挖矿、激励iToken的DEX流动性等


iToken charges a 0.2% withdrawal fee to prevent giant whales from diluting other users' rights

After the user's token enter the Vault, the optimal mining strategy for the token will be automatically configured, and the highest profit mining will be performed under the premise of no loss of the principal. 90% of Vault's profits will be automatically converted to the original token through DEX, thereby increasing the interests of iToken holders. The remaining 10% of profits will buy back YFII and be distributed according to the YIP-5 resolution:
1. Harvest rewards 1%, which is used to subsidize the gas cost of harvesting, and reduce the slippage when the target mining token is converted into the Vault's token and YFII
2. The strategy developer rewards 1%, which is used to encourage contract developers to provide strategies for the Vaults. This part of the fund was originally insurance fund, the insurance business has not yet been launched, and the developer's incentive is relatively urgent
3. 3% of the developer fund is used for the sustainable development of YFII projects. Including smart contract deployment, server application and other expenses reimbursement. And provide grants for operating activities, front-end development, data tool development, etc.
4. YFII Recycle farming 5%, used to incentivize the usage of YFII Vaults, encourage new projects to support YFII farming, and incentivize iToken's DEX liquidity, etc.



## 简单介绍一些iToken的应用案例? ( introduce some application cases of iToken? )
1. iToken将用户的机枪池权益从单一的充值与提现中解放出来，转化为一种可流通的资产。类似于Uniswap的LPT或者Balancer的BPT，可以在支持这些iToken的项目中使用。比如可以抵押iUSDT进入YFII的循环矿池，来获得额外的YFII奖励。
2. 对应于Yearn在Curve.fi所建立的yPool以及对应的PoolToken也就是yCRV，iToken也将会基于合作的稳定币互换平台建立自己的多稳定币池Token，也就是iCRV，并用于后续的项目如CRV挖矿中。这样可以同时获得YFII机枪池生息收益、稳定币互换平台手续费以及目标项目挖矿收益共三重收益。
3. 因为iToken的内在价值始终大于等于Token本币价值，或出现抵押iToken借出Token本币的借贷业务，来提升借贷杠杆率，并且不存在爆仓方面风险

1. iToken tokenized the investors' Vault assets, let the property into a tradable ERC20 token. Similar to Uniswap's LPT or Balancer's BPT, it can be used in projects that support these iTokens. For example, iUSDT can be mortgaged to enter YFII's circulating farming pool to farm additional YFII rewards.
2. Corresponding to the yPool established by Yearn on Curve.fi and the corresponding PoolToken yCRV, iToken will also establish its own multi-stablecoin pool Token **iCRV**, based on the cooperated stablecoin swap platform, and use it for the new DeFi projects into yield farming. In this way, it is possible to obtain a triple income of interest-bearing income from the YFII Vault, stablecoin swap platform fees, and target projects' farming income.
3. Because the inner value of iToken is always greater than the value of Token itself, there might be a loan business that mortgages iToken to lend this Token to increase the lending leverage ratio with no risk of liquidation


## 交易所如何使用iToken？(How does the exchange use iToken?)
1. 首先，交易所可以为用户提供DeFi市场的高收益理财策略，通过向YFII Vault注资而获得相应币种的iToken，iToken可以直接根据用户提供的流动性进行分发，也可集中托管。
2. 为了减少iToken提现时产生的额外费用，交易所可建立iToken/Token的币币交易对，转由二级市场完成iToken的价值贴现

1. First of all, the exchange can provide users with high-yield financial management strategies in the DeFi market, and obtain iToken in the corresponding currency by injecting capital into YFII Vault. iToken can be distributed directly based on the liquidity provided by users, or centralized custody.
2. In order to reduce the extra cost incurred when iToken is withdrawn, the exchange can establish an iToken/Token currency trading pair and transfer it to the secondary market to complete the value discount of iToken

## 用户如何使用iToken？( How do users use iToken? )
1. 存入本币Token进入机枪池，获得iToken，抵押iToken进入循环矿池获得YFII 额外收益
2. 在与YFII合作的稳定币互换平台生成iCRV类PoolToken，并参与支持iCRV挖矿的项目

1. Deposit Token into the Vaults to get iToken, mortgage iToken into the YFII's circulating farming pool to get extra YFII as rewards
2. Generate iCRV on the stablecoin swap platform cooperating with YFII, and participate in new projects that supporting iCRV mining


## iToken未来有哪些计划？( What are the future plans for iToken? )
1. 与更多的DeFi项目进行合作，合成具有更高收益的DeFi衍生品
2. 对iToken所在机枪池策略进行投保，使iToken汇率始终保持在对本币不亏损状态
3. 因同一币种的单一策略资金容量有限，资金进入过多会导致收益率稀释。社区未来将开发多策略机枪池，同一币种自动配置资金进入该币种旗下多个策略，实现整体收益的最大化

1. Cooperate with more DeFi projects to synthesize DeFi derivatives with higher returns
2. Insuring the Vault's strategy where iToken is located, so that the iToken exchange rate is always maintained at a state of no loss to the raw token
3. Due to the limited capital capacity of a single strategy in the same token, too much funds will lead to dilution of total APY. The community will develop a multi-strategy Vault in the future, and the same token will automatically allocate funds into multiple strategies of the token to maximize overall revenue
