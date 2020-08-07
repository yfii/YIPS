---
yip: 2
title: 建立YFII Vault策略 I （Creating YFII's Vault Strategy I)
status: WIP
author: YFII Community
discussions-to: https://gov.yfii.finance/
created: 2020-08-07
updated: N/A
---

## Vault 策略I 是什么？( What is YFII's Vault Strategy I? )

众所周知，YFII Vault是YFII的核心项目，是为普通用户提供一键入金，获得DeFi市场最佳收益的理财协议。为了获得最佳理财收益，Vault将配置多样化的收益策略，而**策略I**是YFII Vault的第一个收益策略

As we all know, YFII Vault is the core project of YFII. It is a crypto assets management protocol that provides retail users with user friendly UI and obtains the best APY in defi market. In order to obtain the best profit at low risk, Vault will configure diversified yield farming strategies, and **Strategy I** is the first farming strategy of YFII Vault

![Vault功能介绍](https://yfii.s3-ap-northeast-1.amazonaws.com/vault3.png)


## 策略I 的工作方式是怎样的? （ How does the Strategy I works? )

1. 建立Balancer YFII/DAI (pool2) 挖矿策略，获得200%以上的基础年化收益率
2. 利用矿池产出的**YFII**，对**YFI**的StrategyYFII挖矿策略进行破解，产生额外套利收益
3. 以**YFII**为利润本位，对YFII Vault的流动性提供者进行分红

1. Establish a Balancer YFII/DAI (pool2) farming strategy and obtain annual percentage rate of 200%+
2. Use the YFIIs which are mined by **strategy I** to exploit YFI’s Strategy and generate additional arbitrage income
3. Take **YFII** as the profit standard, and distribute dividends to the liquidity providers of YFII Vault



## 策略I的机遇与风险分别是哪些？( What is the advantages and risks of YFII Vault? )

1. 根据Balancer 2%YFII+98%DAI 做市权重配比(橙色曲线)，只有当币价发生极端下跌(>60%)时，做市商才可能遇到本金风险。而YFII当前的社区共识是将YFII币价维持在100~120DAI之间，既防止**YFI**的“挖提卖”策略获得过高收益，又同时保证YFII价格不出现显著下降。

2. Dai池的当前年化收益率超过200%，是当前DeFi市场上最高收益的产品之一。只要控制好价格稳定，就是最佳收益策略。
3. 策略将获得多位社区专业智能合约工程师的审计，保证策略的智能合约安全。

![做市商风险曲线](https://yfii.s3-ap-northeast-1.amazonaws.com/bal98.jpeg)

1. According to the Balancer 2%YFII + 98%DAI market-making weighting ratio (orange curve), only when the price has an extreme drop (>60%), the market maker may encounter principal risk.
2. The current community consensus is to maintain the YFII's price between 100~120DAI, which not only prevents YFI’s "digging and selling" strategy from gaining excessive returns, but also ensures that the YFII price does not drop significantly.
3. The current APY of Balancer YFII/Dai pool exceeds 200%, which is one of the most profitable products in the current DeFi market. As long as the price is stable, it is the best profit strategy.
4. The **strategy I** will be audited by several professional smart contract engineers in the community to ensure the security of the strategy.


## 策略I 如何提高YFII价值？( How could Strategy I increase the value of YFII? )
1. 首先，加入策略I是以**DAI**作为入金，这部分资金中的2%需要在市场上购买YFII以生成BPTs（BalancerPoolToken)，从而带来YFII价格的增长。假设有1000万DAI进入策略I，那么会有20万枚DAI需要购买YFII，按照市场价格120DAI一枚计算，可以承接1666枚YFII在此价位上的抛压。与当前池内1600万枚DAI一起，增加池内深度，降低交易滑点。使得价格更难出现极端下跌。
2. 策略I 的理财收益被设置为YFII本位，新挖出的YFII不进行市场抛压，持续稳定YFII市场价格
3. 策略I 的基础farming收益与针对YFI Vault的套利收益，正好都是YFII，减少合约操作步骤，减少操作者Gas消耗

1. First, a crypto investor should use **DAI** as the deposit fund to join **strategy I**. 2% of the funds will automatically buying YFII in the balancer to generate BPT (BalancerPoolToken), which will increase the price of YFII.
2. Assuming 10 million **DAI** enters Strategy I, then there will be 200,000 DAI that need to be purchased for YFII. According to the market price of 120 DAI, there will be 1,666 YFIIs bought at this price.
3. Together with the current 16 million DAI in the pool, **strategy I** can increases the balancer pool's depth and reduces slippages. This makes it more difficult for prices to experience extreme dumps.
4. The revenue of **Strategy I** is set to the YFII standard, and the newly mined YFIIs will not be sold to the market. The YFII's price will continue to be stabilized
5. The basic farming revenue of **Strategy I** and the arbitrage revenue for YFI Vault are both YFII, which reduces the contract operation steps and reduces the operator's gas consumption
