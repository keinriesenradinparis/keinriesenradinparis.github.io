---
title: Notes on DeFi from Finematics
date: 2025-07-29
categories: 
  - "web"
layout: page_light
---

<!-- # Notes on DeFi from Finematics -->

> [!NOTE] Summary
> The website [Finematics](https://finematics.com/guide-to-decentralized-finance/) gives a gentle (but slightly technical) introduction to the DeFi system, principally discussing around Ethereum.

> [!TIP]
> The real technical part is the development of smart contracts.
> A friendly introduction is given by [Solidity by examples](https://solidity-by-example.org/).

## Finance — DeFi

Sources from 2020–2021:
- [Finematics playlist](https://youtube.com/playlist?list=PLjrTIwaNiTwlQgZy4F55JM8p6gpfFAbns&si=BYGeeDzwspfS1b2m)

**Circuit breakers 熔断机制**
- Circuit Breakers are automatic mechanisms that calm down the stock market and prevent the stock market from a free fall (stop panic selling, regulate to avoid total collapse) by halting trading for a predefined time. 
- The New York Stock Exchange has 3 levels of market-wide circuit breakers.
	- -7% (S&P 500) before 3:25 PM, trading halted for 15 min
	- -13% (S&P 500) before 3:25 PM, trading halted for 15 min
	- -20% (S&P 500) at any time, trading halted for the rest of the trading day
- Individual stocks, future exchanges have their own circuit breakers.
- Crypto exchange do not have circuit breakers as they are not regulated in the same way as more traditional exchanges.

**Quadratic funding**
- Quadratic funding is a concept that extends ideas from quadratic voting to a funding mechanism. Both concepts were widely discussed by Vitalik Buterin in his blog posts and a paper that he co-authored together with Zoë Hitzig and Glen Weyl. At the core of Quadratic funding is its **matching pool**. A matching pool is a pool of money that is provided by the **matching partners**. Matching partners are companies, individuals or even protocols supporting public goods projects. The funds collected in the matching pool are used to magnify the individual contributions to different projects.
- Public goods: non-excludable and non-rivalrous, e.g.
	- clean air, infrastructure, privacy
	- open-source, free education, free services (ethical hacking, finding vulnerabilities in open-source projects) — these benefit from quadratic funding.
- Quadratic voting
- Quadratic funding
- **Matched amount** is computed by the **quadratic funding formula** $v_i^p((\sum_j \sqrt{c_j^p})^2) - c_i^p$, where $c_j^p$ is the funding amount for the project $p$ coming from the individual $j$. Consequence: this favours smaller contribution more.

**DeFi — Future of Finance?**
- Instead of relying on old and inefficient infrastructure, Decentralised finance, or DeFi, leverages the power of cryptography, decentralisation and blockchain to build a new financial system. A system that can provide access to well-known financial services such as payments, lending, borrowing and trading in a more efficient, fair and open way.
- Key metrics in DeFi:
	- TVL (Total Valued Locked)
	- DEX Volume (trading volume across decentralised exchanges)
- GameStop short squeeze:
	- GameStop (GME) 是一家实体游戏零售商，股价因业绩和行业变化长期低迷。
	- 大量对冲基金认为 GameStop 股价会跌，进行了大量做空（short selling），即借股票卖出，希望股价下跌后低价买回赚差价。
	- 但有一群散户投资者（主要聚集在Reddit论坛的r/WallStreetBets）发现大量做空头寸后，开始大量买入GameStop股票。
	- 散户的买入推高股价，迫使做空的对冲基金被迫回补空头（买回股票止损），导致股价进一步上涨，形成了**空头挤压（short squeeze）**。
	- 股价在几周内从约20美元飙升至最高约480美元。
	- **Robinhood**作为一个流行的零佣金交易平台，在股价飙升期间限制了GameStop股票及其他被散户炒作的股票交易，引发用户和公众强烈争议。
	- This is an instance of centralised finance.
- A DeFi solution of DEX: Uniswap.
- Challenges:
	- More security responsibilities to the users: there is no handholding but only direct interaction with new DeFi protocols.
	- Regulatory requirement like KYC.
	- Scaling problem: high gas fees resulting from high demand of the ethereum –> already have a solution to this: **Layer 2** and **Rollup**.
	- Hacks.
	- Whales and voters apathy in certain governance models.
	- How to implement collateralised loans and mortgages? –> One try: Aave.

**Perpetual protocol**
- Perpetual Protocol is a DeFi project with the main goal of creating the best, most accessible and most secure DEX (decentralised exchange) for perpetual futures. 
- Perpetual Protocol was founded in 2019 by a small team of startup founders and software engineers. Initially called “Strike”, the project pivoted to perpetual futures and changed its name in the summer of 2020. 
- The first version of the protocol was launched on the xDai network in December 2020. 
- Version 2 of the protocol named Curie after the famous scientist and a Noble Prize winner - Marie Curie, launched on Optimism (Layer 2 solution) on the 31st of November 2021. 
- The design of Perpetual Protocol that we're going to explain later is extremely interesting as it leverages the DeFi “money legos” ethos to both build upon other already existing DeFi projects as well as provide building blocks for other protocols in the future. 
- Perpetual Protocol is one of the projects that focus on derivatives in DeFi.
- The main derivative product: perpetual futures.
	- Funding rate: to make sure that the price of the perpetual contract does not diverge too much from the actual price of their underlying assets.
	- Easy access to leverage, but could also be dangerous!
- Perpetual Protocol:
	- Launched on Layer 2: scalable, low transaction fees, high transaction throughput
	- Builds upon **Uniswap V3**: providing liquidity, and leveraging the DeFi “money legos” ethos in a completely permissionless way.
	- Uses **Clearing House** contract: minting and burning **v-tokens** (virtual tokens).
	- Uses *cross* margin mode.
	- Can use isolated margin mode by creating separated wallets.

**FTX collapse**
- Founder: Sam Bankman-Fried (SBF), graduated in 2014 from MIT with a degree in physics, started working full-time in Jane Street Capital, launched in 2017 the Alameda Research (quant trading company focused on the crypto market), alleged to believe in "Effective Altruism", secured profits from a big arbitrage opportunity created by price discrepancies of Bitcoin traded in American and Asian exchanges, launched in 2019 FTX.
- Rise To Power in 2021 : liquidity supplied by Alameda Research itself, invested by Sequoia Capital, Soft Bank, Tiger Global, etc.
- Controversy: SBF's legislation lobbying at the detriment of DeFi.
- The Collapse in 2022:
	- Insolvency rumours: a leaked balance sheet of Alameda shows that most of the funds comes from FTT, the token of FTX, which has a small float (only a small portion of the total supply of the token was actively traded).
	- Binance wanted to exit their investment on their rival FTX, but FTX decided to pay back using stable coins and FTT. Worried by insolvency rumours, CZ decided to sell their FTT position. CZ revealed a big hole (lending funds to Alameda at some point during the 3AC Saga) in the FTX balance sheet.
- Impact:
	- Solana market impacted: Solana had FTX and Alameda as big supporters, and wrapped assets on Solana such as BTC and ETH were backed by FTX and Alameda.
	- BlockFi stopped withdraws: BlockFi had offered a $400m credit facility to FTX.
	- Damaged the already shaken reputation of crypto industry.
- The Path Forward:
	- more centralisation (regulation),
	- On-chain transparency, self-custody, fair access, self-regulation by protocols — whose codes can be fully audited by anyone.


## Guide To Decentralized Finance

Sources from 2020–2021:
	- [Finematics post](https://finematics.com/guide-to-decentralized-finance/)

![](https://finematics.com/wp-content/uploads/2020/11/guide-smaller-1024x499.png)

### About This Guide

Are you new to Decentralized Finance (DeFi) and don't know where to start? Or maybe you want to up your game and take your DeFi skills to the next level? No matter where you are in your DeFi journey, this guide is for you. 

This guide is split into 3 levels:

![](https://finematics.com/wp-content/uploads/2020/11/levels-1024x334.png)

Each level contains the knowledge and skills required before advancing to the next level. This way, you are presented with a structured guide that is easy to follow. Each skill and every single piece of knowledge is built on top of already acquired information. 

We provide links to our own material (videos and articles) whenever we can, but we also make use of other resources that we find useful. All of the external resources are thoroughly reviewed and highly recommended by us. 

Decentralized Finance is one of the fastest developing new industries. That is why this guide is being constantly reviewed and updated when necessary. If you have any suggestions related to this guide please send them to [jakub@finematics.com](mailto:jakub@finematics.com) 

Welcome to the future of finance.  

### DeFi Novice

This is our first level which is perfect for beginners. If you have heard about decentralized finance before, but all of the concepts and terminology seem a bit overwhelming – this is where you start.

1. **What is Decentralized Finance?**  
    Let's start from understanding what decentralized finance is all about.  
    _Knowledge:_ ? [video](https://youtu.be/k9HYC0EJU6E) ? [article](https://finematics.com/defi-explained/)  
    _Skills:_ Check out [DeFi Pulse](https://defipulse.com/). TVL (Total Value Locked) represents the amount of value locked in different DeFi protocols. You can check different categories of protocols such as lending, dexes (decentralized exchanges), derivatives, payments and assets.
2. **DeFi Wallets**  
    Okay, we just learned what DeFi is. Time to get a cryptocurrency wallet that makes interacting with DeFi protocols easy.  
    _Knowledge:_ ? [video](https://youtu.be/JCYIFtb8DwM) ? [article](https://finematics.com/top-3-defi-wallets-for-2021/)  
    _Skills:_ Install one of our recommended wallets and get ready for interacting with different DeFi protocols. Here is a useful Metamask [guide](https://decrypt.co/resources/metamask).  
    Now, as you have your wallet ready, it's time to send some ETH to it. If you don't have any ETH just yet and you want to buy it we'd recommend using one of the established cryptocurrency exchanges such as Coinbase or Kraken.
3. **Smart Contracts**  
    In the first step, we learnt that decentralized finance is based on smart contracts that run on open blockchains such as Ethereum. Time to learn more about this concept.  
    _Knowledge:_ ? [video](https://youtu.be/pWGLtjG-F5c) ? [article](https://finematics.com/smart-contracts-explained/)  
    _Skills:_ Let's check out how a simple Solidity smart contract looks like [here](https://docs.soliditylang.org/en/v0.4.24/introduction-to-smart-contracts.html). If you're a developer you may want to dive deeper into this topic as pretty much all DeFi protocols are built using smart contracts. If you're not a developer, it's enough to just scroll through the linked tutorial and see that smart contracts are basically just pieces of code that can be used to build permissionless DeFi protocols.
4. **Uniswap**  
    Uniswap is currently the most popular decentralized exchange by a wide margin. It's also one of the easiest protocols in DeFi allowing the users to exchange their tokens in a completely decentralized and permissionless way. In this step, we're just learning the basics of Uniswap. You can find a deeper dive into liquidity pools and automated market makers on the DeFi Apprentice level.  
    _Knowledge:_ ? [video](https://youtu.be/LpjMgS4OVzs) ? [article](https://finematics.com/uniswap-uni-token-explained/)  
    _Skills:_ Let's try to use Uniswap. Go to the Uniswap [website](https://app.uniswap.org/#/swap) first. You'll have to connect your Metamask wallet. After that, you can choose the tokens that you want to trade. If you decide to swap some tokens, you'll have to approve 2 transactions. The first one to approve spending of particular tokens. And the second one to approve the actual swap.
5. **Lending and Borrowing**  
    Lending and borrowing is one of the most important element of any financial system. DeFi lending allows users to become lenders or borrowers in a completely decentralized and permissionless way while maintaining full custody over their coins.   
    _Knowledge:_ ? [video](https://youtu.be/aTp9er6S73M) ? [article](https://finematics.com/lending-and-borrowing-in-defi-explained/)  
    _Skills_: Let's go to the Compound [website](https://app.compound.finance/) and make ourselves familiar with the user interface. We have “Supply Markets” on the left side – these are tokens that you can lend out and “Borrow Markets” on the right side – these are tokens that you can borrow. If you decide to lend out your tokens you have to approve them as collateral first. If you decide to borrow other tokens the interface will guide to find a safe amount that can be borrowed based on your supplied collateral.

Great! This is all the knowledge and all the skills required on DeFi Novice level. 

Time to advance to the next level.

### DeFi Apprentice

At this level, you feel comfortable with all the concepts included at the DeFi Novice level and you're ready to take a deeper dive into the future of finance.

1. **Liquidity Pools**  
    We already learnt a little bit about Uniswap at the previous level. Now, it's time to better understand how Uniswap works under the hood.  
    _Knowledge:_ ? [video](https://youtu.be/cizLhxSKrAc) ? [article](https://finematics.com/liquidity-pools-explained/)  
    _Skills:_ Time to learn how you can add liquidity to a Uniswap liquidity pool. If you decide to do it make sure you go through the next step that describes what impermanent loss is. Without this knowledge, you may end up exposing yourself to impermanent loss without even knowing it.  
    Go to the Pool section on the Uniswap website. Click on “Add liquidity”. You'll have to choose 2 tokens that you want to provide. Approve both of them. And finally, approve the transaction that adds liquidity. You have to have a correct ratio of tokens in the first place – 50/50.
2. **Impermanent Loss**  
    Impermanent loss is one of the most important concepts to understand before deciding to provide liquidity in a liquidity pool.  
    _Knowledge:_ ? [video](https://youtu.be/8XJ1MSTEuU0) ? [article](https://finematics.com/impermanent-loss-explained/)  
    _Skills:_ To understand impermanent loss better you can go through the example from our video and try to get to the same amount of ETH and DAI by using formulas from [this](https://pintail.medium.com/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) article by Pintail.
3. **Yield Farming**  
    Yield Farming is one of the most discussed topics when it comes to DeFi. Learn more about this topic to understand where the high returns are coming from.  
    _Knowledge:_ ? [video](https://youtu.be/ClnnLI1SClA) ? [article](https://finematics.com/yield-farming-explained/)  
    _Skills:_ Check out some of the yield farming opportunities available. You can find them, for example, on Coingecko's [website](https://www.coingecko.com/en/yield-farming). Be careful with less popular yield farming opportunities. The chances of losing money are high. Try to stick to the main projects such as Uniswap or Compound if you're just starting.
4. **Yearn Finance**  
    If you have decided to make some money on lending your coins in DeFi, you can quickly realise that rates keep changing all the time. If you want to make your life easier and switch between different lending protocols automatically, you can check out Yearn Finance.  
    _Knowledge:_ ? [video](https://youtu.be/qG1goOptZ5w) ? [article](https://finematics.com/yearn-finance-and-yfi-explained/)  
    _Skills:_ Provide liquidity in stable coins to the Curve's [Y Pool](https://www.curve.fi/iearn/). The Curve protocol partnered with Yearn Finance and made it possible to supply liquidity in stable coins to the Y Pool. On top of getting a return on your yTokens such as yDAI, you'll also get trading fees for providing liquidity for swapping between yTokens. Caution: providing liquidity to the Y Pool is usually quite costly – transaction-wise. Try doing it when the Ethereum network congestion is low.
5. **Yearn Vaults**  
    You are already familiar with the Yearn Protocol and yield farming. Time to combine these two together. Yearn Vaults offer an easy way to participate in yield farming without spending too much on gas fees.  
    _Knowledge:_ ? [video](https://youtu.be/9vTaNl2_B8A) ? [article](https://finematics.com/yearn-vaults-eth-vault-explained/)  
    _Skills:_ Check out Yearn Vaults [here](https://yearn.finance/vaults). If you decide to put your money into a Vault, make sure you're ok with the risk involved (smart contract risk, strategy risk etc.).

Amazing! Liquidity pools, AMMs, yield farming – this level was quite a challenge, right? Some of the concepts included at this level can be quite hard and it's always worth going through them a few times before advancing to the next level.

### DeFi Master

Concepts included in DeFi Novice and DeFi Apprentice seem to be easy for you. Time to bring your skills to the next level.

1. **Flash Loans**  
    Flash loans are worth understanding even if you're not planning on using them. This is because flash loans are notorious for being used in DeFi hacks with [the bZx attack](https://www.coindesk.com/the-defi-flash-loan-attack-that-changed-everything) being one of the most famous ones.  
    _Knowledge:_ ? [video](https://youtu.be/mCJUhnXQ76s) ? [article](https://finematics.com/flash-loans-explained/)  
    _Skills:_ Check out our flash loan tutorials. If you are a developer, check out our coding [tutorial](https://finematics.com/how-to-code-a-flash-loan-with-aave/). If you don't want to code, check out our Furucombo [tutorial](https://finematics.com/how-to-use-furucombo/).
2. **Sushi Vampire Attack**  
    Vampire Attack presents an interesting way of trying to steal users of another DeFi protocol. It's an advanced topic that is worth understanding.  
    _Knowledge:_ ? [video](https://youtu.be/UFjXwrCGuog) ? [article](https://finematics.com/vampire-attack-sushiswap-explained/)  
    _Skills:_ Check out the original SushiSwap [here](https://sushiswapclassic.org/). Try to answer the following question: how can a protocol protect itself from a vampire attack?
3. **Ampleforth**  
    Time for something completely new. Learn more about Ampleforth, elastic money supply and rebases. Ampleforth's model was also widely used in multiple other DeFi projects, so it's worth to understand it.  
    _Knowledge:_ ? [video](https://youtu.be/e-8yjmsshFg) ? [article](https://finematics.com/ampleforth-explained/)  
    _Skills:_ Check out Ampleforth's [dashboard](https://www.ampleforth.org/dashboard/) to see rebases and price targets in action.
4. **NFTs in Defi**  
    Another advanced topic. Learn more about how Non-fungible Tokens can be used in DeFi.  
    _Knowledge:_ ? [video](https://youtu.be/Xdkkux6OxfM) ? [article](https://finematics.com/what-are-nfts-and-how-can-they-be-used-in-defi/)  
    _Skills:_ Check out some of the popular NFT marketplaces such as [Rarible](https://rarible.com/) or [OpenSea](https://opensea.io/).
5. **Layer 2 Scaling**  
    Learn how DeFi can scale up using Layer 2 scaling solutions.  
    _Knowledge:_ ? [video](https://youtu.be/BgCgauWVTs0) ? [article](https://finematics.com/ethereum-layer-2-scaling-explained/)  
    _Skills:_ Try using a decentralized exchange on Layer 2 such as [Honeyswap on xDai.](https://www.xdaichain.com/about-xdai/project-spotlights/honeyswap)

Awesome! If you managed to complete all the levels – congrats! You are now a DeFi Master. There is not a lot of time to celebrate though. Decentralized finance moves fast and there are always new things to learn. 

To stay up to date and learn even more about decentralized finance, make sure you subscribe to Finematics on [Youtube](https://www.youtube.com/c/finematics) and follow us on [Twitter](https://twitter.com/finematics).


## Guide to DeFi — notes taken

Sources from 2020–2021:
- [Finematics playlist](https://youtube.com/playlist?list=PLjrTIwaNiTwn39tg3sR_bPBWGHoznv47D&si=mbboW5aMU3-5dlUl)
- [Finematics post list](https://finematics.com/category/defi/)


**Smart contracts**
- Code is law (a piece of code that can be executed automatically and in a deterministic way), aimed at removing human factors from decision making
- Most popular platform for smart contracts: Ethereum, where the language is called Solidity.
- Basics building blocks of **dApps**.
- Risks:
	- Bugs & hacking: security audit, formal verification (the smart contract always behaves in the expected way).
	- Protocol changes like upgrade of the Ethereum network.
	- Oracle services helping receive real world information (e.g. accidental damages in car renting): Chainlink.

**DeFi**
- It started with MakerDao, founded in 2015, which uses DAI (algorithmic stable coin, unlike USDT, USDC which needs a 1:1 matching fiat currency reserve).
- Benefits, and risks:
	- Bugs.
	- Admin keys.
	- Systemic risks.

**Yield farming**
- Yield farming is a way of trying to maximise a rate of return on capital by leveraging different DeFi protocols. Sometimes there is an incentivising token as reward.
- Yield farmers try to chase the highest yield by switching between multiple different strategies.
- High APY: **liquidity mining** (Compound), leverage. But with high risk!
- Strategies can become obsolete very quickly.

**Liquidity pools**
- Liquidity pools are pools of tokens that are locked in a smart contract. They are used to facilitate trading by providing liquidity and are extensively used by some of the DEXes.
- Opposed to the Order Book model (buyer & sellers).
- Price adjustment mechanism:
	- **Automated Market Maker** (AMM): deterministic algorithm.
	- Constant product market maker: $x y =k$ (bonding curve), where $x$ is the token x quantity, and $y$ is the token y quantity, with $k$ being a constant.
	- AMM does not work well for assets with similar prices, e.g. stable coins (cf. the Curve pool).
	- Basic form: Uniswap.
- Risks additional to those of DeFi:
	- **Impermanent loss**.
	- **Liquidity pool hacks**.

**Ampleforth**
- **Elastic** and **non-dilutive** (by changing the supply of AMPL — hence the number of my AMPL tokens keeps changing).
- An early approach to "stable" coins.

**Bancor V2**
- Bancor is an on-chain liquidity protocol that enables automated, decentralised token exchange on Ethereum and across blockchains.
- Users add liquidity to AMM in exchange for trading fees, staking rewards and future voting rights in the Bancor DAO.
- Update in Bancor V2: Dynamic AMM (DAMM).
	- Addresses two issues of V1: "impermanent loss" and exposure to multiple assets.
		- Price oracles such as Chainlink provide external prices to smart contracts in a decentralised and reliable way.
		- Variable **weight**: uses dynamic fees to push the pool price to be equal to the market price, in order to avoid arbitrage (which could make impermanent loss a permanent loss to stakers); similarly for supply change.
	- Provide more efficient bonding curves to obtain less slippage.
- However, the exchange still depends on the intermediate coin BNT.
- Also, cannot create a USDT-USDC pool in Bancor V2.

**Yam**
- Yam is a protocol built in 2022 as a monetary experiment, combined some of the most interesting innovations in programmable money and governance, such as an elastic supply, on-chain governance, a governable treasury and a fair distribution mechanism.
- Similar to Ampleforth, the difference being that:
	- Yam was meant to use a portion of each supply expansion to buy yCRV that is a high-yield USD-denominated stable coin. 
	- Once bought, yCRV was supposed to be added to the Yam treasury. 
	- YAM holders were able to decide how to use these funds for future development and changes to the protocol entirely on-chain through community voting.
- **One bug** was found: no governance is possible in some situation.
- Bug was fixed in 24 hours and gained massive necessary votes, but the update proposal was not able to be executed due to **a new bug**.

**Impermanent loss**
- Impermanent loss is a temporary loss of funds occurring when providing liquidity in standard liquidity pools where the **liquidity provider** (LP) has to provide both assets in a correct ratio, and one of the assets is volatile in relation to the other, for example, in a Uniswap DAI/ETH 50/50 liquidity pool.
- Often explained as a difference between holding an asset versus providing liquidity in that asset.
- If ETH goes up in value, the pool has to rely on arbitrageurs continually ensuring that the pool price reflects the real-world price to maintain the same value of both tokens in the pool. This basically leads to a situation where profit from the token that appreciated in value is taken away from the liquidity provider. At this point, if the LP decides to withdraw their liquidity, the impermanent loss becomes permanent.
- Incentives for LPs:
	- trading fees,
	- rewarding tokens (liquidity mining).
- Solutions: 
	- Balancer: pool with arbitrary weight,
	- Bancor V2:pool with adjustable weight.

**Yearn Finance**
- The **Yearn protocol** is a yield optimiser that focuses on maximising DeFi capabilities by automatically switching between different lending protocols.
- History: in early 2020, the author of Yearn protocol - Andre Cronje, started looking into automating his strategy for choosing the highest paying lending protocol for his stable coins. 
- The protocol, in essence, creates a pool for each stable coin. By depositing a stable coin to a pool, the user receives their yTokens that are yield-bearing equivalents of the coin that was deposited. 
	- For example, if a user deposits DAI, the protocol issues yDAI. The DAI that is pooled together can then be moved between different lending protocols to always maximise the yield. 
	- For instance, if Aave offers a better yield on DAI than Compound, the yearn protocol can decide to move all or some of the DAI to Aave. The protocol checks if there is a better yield available at the time a user deposits or withdraws money from the pool, triggering a rebalance of the pool if necessary. If a user wants to withdraw their initial DAI + accrued interest they can redeem their yDAI and receive the underlying DAI. 
- One thing that the protocol always assures is to never swap the initially deposited stable coin to a different stable coin, even if there is a higher yield available. 
	- For example, if a user deposits DAI, the protocol would never swap it to USDC, even if USDC has a higher yield. This is because most users want to withdraw the same stable coins as they initially deposited.
- As the money in the pools started growing, some of the previously obvious strategies stopped working, so one had to optimise splitting funds.
- Compound makes it more difficult to find strategies with best APY.
- Then comes the **Yearn Vault**: pools with funds with an associated strategy (voted in by the Yearn community) for maximising returns on the asset in the vault.
	- e.g. ETH Vault: by supplying ETH collateral to MakerDAO the ETH strategy can borrow DAI at 200% collateralisation ratio, creating a collateralised debt position (CDP) — however, if this ratio drops below 150% due to ETH price falling, the CDP owners have one hour to bring the ratio back to over 150%, otherwise susceptible to liquidation.
- Governance token: YFI.
	- The token distribution was focused on a fair launch: no pre-mining, no VCs allocation, no team reward.
- Other services: YSwap, YTrade, YBorrow, YInsure.

**Vampire Attack**
- The project SushiSwap, led by ChefNomi, aimed at directly competing with Uniswap (V2 at that time) by forking the project and siphoning out liquidity with a process later called a vampire attack. The main goal of the project was to create a community-governed automated market maker and fairly distribute its token. The concept of a **vampire attack**, although quite simple, is quite ingenious in its nature as it creates very strong incentives for liquidity providers to migrate their liquidity to a new platform. The liquidity is basically sucked out of the first platform and moved into the second platform, hence the name — vampire attack.
- Unexpected event: ChefNomi himself sold his entire SUSHI stake, worth around $14M, for ETH. The community lost trust in ChefNomi who later decided to leave the project. This led to yet another unexpected event where ChefNomi basically transferred the control of the project to SBF, who decided to be a saviour of Sushi and provide even more incentives to the liquidity providers to stay for the migration with an extra 1 million of SUSHI tokens. Two days after the migration, ChefNomi came back, returning $14M worth of ETH to the dev fund and apologising to the community.

**History of Uniswap**
- (Skipped)

**NFT**
- Non-fungible tokens (NFT):
	- unique,
	- provably scarce,
	- indivisible.
- NFTs on Ethereum: related standards:
	- ERC-20: for creating fungible tokens, such as stable coins and DeFi tokens.
	- ERC-721: for creating non-fungible tokens.
	- ERC-1155: for creating contracts that support both fungible and non-fungible tokens.
- NFT spaces: CryptoKitties, Gods Unchanged, Decentraland, Rarible, SuperRare, OpenSea, etc.
- NFT collateralised loans:
	- Their price cannot be easily measured by for example price oracles.
	- One solution: Peer-to-peer loans: NFTfi.

**Flash Loans**
- Allows you to borrow any available amount of assets from a designated smart contract pool with no collateral.
- They can be used in DeFi for things like arbitrage, swapping collateral and self-liquidation.
- Initially introduced by the Marble protocol, then popularised by Aave and dYdX.
- A flash loan has to be borrowed and repaid within the same blockchain transaction.
- User interfaces: Collateralswap, Defisaver or Furucombo
	- Furucombo is a tool that allows you to construct an Ethereum transaction using a simple drag-and-drop user interface. It can visualise complex DeFi transaction by showing a chain of interactions displayed as individual “cubes”. Each cube represents one specific interaction, for example, taking a flash loan or swapping coins on Uniswap. Try with the [link](https://furucombo.app/combo).

**Is Yield Farming DEAD?**
- Depends on several factors:
	- viability of the project,
	- general market sentiment.


#eth
**Ethereum Layer 2 Scaling**
- Need for scaling: The scaling debate always heats up after a period of major network congestion (–> high gas fees). Firstly: 2017 crypto bull market.
- Two major ways of doing it: scaling the base layer itself (Layer 1) or scaling the network by offloading some of the work to another layer – Layer 2.
	- Layer 1 is our standard base consensus layer where pretty much all transactions are currently settled.
	- Layer 2 is another layer built on top of Layer 1.
		- Layer 2 doesn't require any changes in Layer 1, it can be just built on top of Layer 1 using its existing elements such as smart contracts. It handles transactions off-chain (off Layer 1).
		- Layer 2 also leverages the security of Layer 1 by anchoring its state into Layer 1.
	- Scalability Trilemma: scalability, security, decentralisation.
- Layer 2 scaling solutions:
	- Payment Channels: 
		- Application specific, cannot be used to scale general-purpose smart contracts.
		- Example: Raiden.
	- Plasma:
		- Proposed by Joseph Poon and Vitalik Buterin.
		- Uses child chains.
		- Long waiting period for withdrawal of funds from Layer 2, cannot be used to scale general-purpose smart contracts.
		- Examples: OMG Network, Matic Network (rebranded to Polygon).
	- Sidechains:
		- Independent blockchains with their own consensus models and block parameters.
		- Example: xDai.
	- Rollups:
		- Bundling or "rolling up" sidechains transactions into one transaction and generating a cryptographic proof, also known as a SNARK (succinct non-interactive argument of knowledge). Only this proof is submitted to the base layer.
		- All transaction state and execution are handled in sidechains. The main Ethereum chain only stores transaction data.
		- Two types of rollups:
			- Zk rollups: faster, more efficient, not easy for migrating the existing smart contracts to Layer 2.
				- Example: Loopring and Deversifi (DEXs), ZkSync (scalable crypto payments).
			- Optimistic Rollups: runs an EVM-compatible virtual machine called OVM (Optimistic Virtual Machine), making it easier for the existing smart contracts to maintain their composability.
				- Example: Optimism.
	- Community: mainly scaling through rollups, cf. Vitalik Buterin's post *A rollup centric Ethereum roadmap*.

#eth
**EIP-1559**
- Ethereum Improvement Proposal No. 1559, a.k.a the **fee burn proposal**.
- Previous fee model: a simple auction mechanism known as **first price auction**.
	- The users who want to have their transaction picked up by a miner have to essentially bid for their space in a block. This is done by submitting a gas price that they are willing to pay for a particular transaction. The miners are incentivised to pick up transactions by sorting them by the highest gas price and including the most profitable ones first.
	- Problem: overpaying for their transactions, or waiting for a long confirmation period.
- EIP-1559:
	- This is also where EIP 1559 comes into play. The proposal was made to accommodate these problems and it aims to achieve the following goals. 
		1. Making transaction fees more predictable.
		2. Reducing delays in transaction confirmation.
		3. Improving user experience by automating the fee bidding system.
		4. Creating a positive feedback loop between network activity and the ETH supply.
	- More concretely:
		- **Base fee** (BASEFEE) = minimum gas fee for getting included in a block.
		- Increased network capacity: from 12.5M to 25M gas limit per block.
		- Base fee adjustment logic:
			- When the network is at > 50% utilisation, the base fee is incremented. 
			- When the network is at < 50% utilisation, the base fee is decremented.
		- **Miner tip** – a separate fee that can be paid directly to the miner to incentive them to prioritise a transaction.
			- To avoid a situation where miners can collude and artificially inflate the base fee for their own benefit, the entire base fee is burnt, while instead, the miner tip is paid to them.
		- **Fee cap** (FEECAP) can be set by users for each transaction –> simplifies wallets' user interfaces.
	- Implications:
		- Burning the base fee creates an interesting feedback loop between the network usage and the ETH supply. 
			- More network activity = more ETH burnt = less ETH available to be sold on the market by miners, making the already existing ETH more valuable.
		- Due to miner tip ≠ base fee, ETH would end up being sometimes inflationary and sometimes deflationary — not a major problem in practice.
		- Does not lower gas fees, but only smooths fee spikes.
			- Main ways of lowering gas fees: ETH 2.0 and Layer 2 scaling solutions.

**Lending and Borrowing in Defi**
- Most loans are overcollateralised: determined by the **collateral factor**.
- How it works:
	- For example, lending and borrowing ETH in Compound: 
		- Lending: deposit their ETH in exchange for cETH.
		- Borrowing: lock their cETH to borrow other tokens such as ETH.
	- As for in Aave:
		- Use instead aETH tokens.
- Lenders earn interest:
	- Compound: the amount of cTokens stays unchanged, but the exchange rate changes (usually increases).
	- Aave: the interest are distributed directly as aTokens.
- Risks:
	- Smart contract risks as usual.
	- quickly changing APYs.

**Top 3 DeFi Wallets for 2021**
- Popular shapes: 
	- a browser extension,
	- a hardware wallet,
	- a mobile app,
	- or a web wallet.
- Metamask
	- Non-custodial + recovering seed phrase.
	- Browser extension or App.
- Ledger:
	- Non-custodial.
	- Hardware Wallet.
- Argent:
	- Non-custodial + social recovery model.
	- Mobile app.
	- Has daily limits and locking option.
- DeFi dashboards (no wallets): Zapper, Zerion, etc.

**Ethereum 2.0**
- a.k.a. Eth2.
- A set of interconnected upgrades to the Ethereum network that aims at making Ethereum more scalable, more secure and more sustainable.
	- From Proof of Work to Proof of Stake (more sustainable and more secure).
	- (Data) **sharding** (and rollups that has been realised before Eth2) (more scalable), but sharded chains alone won’t be able to handle transactions or smart contracts.
	- The Beacon Chain: responsible for coordinating a Proof of Stake based system by randomly assigning stakers to validate different shards (and it becomes one of the Eth2 shards).
	- Docking: a process in which the current Ethereum chain becomes one of the shards in the Eth2 Proof of Stake system.

**Quadratic funding**
- Quadratic funding is a concept that extends ideas from quadratic voting to a funding mechanism. Both concepts were widely discussed by Vitalik Buterin in his blog posts and a paper that he co-authored together with Zoë Hitzig and Glen Weyl. At the core of Quadratic funding is its **matching pool**. A matching pool is a pool of money that is provided by the **matching partners**. Matching partners are companies, individuals or even protocols supporting public goods projects. The funds collected in the matching pool are used to magnify the individual contributions to different projects.
- Public goods: non-excludable and non-rivalrous, e.g.
	- clean air, infrastructure, privacy
	- open-source, free education, free services (ethical hacking, finding vulnerabilities in open-source projects) — these benefit from quadratic funding.
- Quadratic voting
- Quadratic funding
- **Matched amount** is computed by the **quadratic funding formula** $v_i^p((\sum_j \sqrt{c_j^p})^2) - c_i^p$, where $c_j^p$ is the funding amount for the project $p$ coming from the individual $j$. Consequence: this favours smaller contribution more.

**"Bitcoin" on Ethereum**
- Wrapped BTC (wBTC): custodian and centralised.
	- The custodian can mint/burn wBTC on Ethereum in response for merchant's receiving/sending BTC on Bitcoin.
- RenBTC: similar to wBTC, but decentralises the custody of BTC.
	- Ren protocol runs by operating a network of decentralised nodes called Darknodes. It also leverages a few interesting elements in cryptography such as Shamir's Secret Sharing and Secure Multiparty Computation.
- tBTC: similar to RenBTC, but uses a network of signers for minting tBTC.
	- Randomly chosen (for each minted tBTC) "signers" have to provide ETH as collateral to ensure they cannot walk away with locked BTC, and they have to overcollateralise their ETH (but they will be rewarded with fees during the lock-up period).
- sBTC: an synthetic asset (a derivative backed by SNX collateral) created by Synthetix protocol.
	- There is no underlying BTC, the value is secured by SNX token collateral, usually highly overcollateralised (mainly in order to absorb any sharp price changes in synthetic assets).
- The actual BTC is never on Ethereum!

**The Graph**
- "The Google Of Blockchains".
- The Graph is an (decentralised) indexing protocol for querying blockchain data that enables the creation of fully decentralised applications.
- Centralised indexing/ingestion services: Etherscan, Blockchain, etc.
- The Graph uses the query language GraphQL: queryable data is organised in the form of subgraphs, e.g. subgraphs (containing for example many volume data) of protocols such as Uniswap, Compound, etc.
- Architecture:
	- Indexers: stake GRT tokens and run a Graph node.
	- Consumers: query Indexers and pay them.
	- Curators: use GRT tokens to signal worth-indexing subgraphs.
	- Delegators: stake GRT tokens and earn a portion of Indexers' rewards and fees, do not run any Graph node.
	- Fisherman and Arbitrators: useful in case of a dispute, e.g. incorrect data provided by Indexers to Consumers.

**Aave**
- Most popular lending protocols in DeFi.
- Once known as ETHLend — peer-to-peer model.
- Later switched to peer-to-contract model.
- Aave means "a ghost" in Finnish.
- Popularised the feature Flash Loans.
- V2 features:
	- Collateral Swap: possible thanks to flash loans.
	- Batch Flash Loans: borrow multiple assets at the same time (within the same transaction).
	- Debt Tokenisation: borrowers receive tokens that represent their debt.
	- Native Credit Delegation: this provides liquidity without necessarily providing collateral, but rather debt tokens.

**Derivatives in DeFi**
- Derivatives are one of the key elements of any mature financial system. As the name suggests derivatives derive their value from something. This "something" is usually the price of another underlying financial asset such as a stock, a bond, a commodity, an interest rate, a currency or a cryptocurrency. Some of the most commonly used derivatives are forwards, futures, options and swaps.
- Main usages: hedging and speculation.
- Protocols:
	- Synthetix: allows for creating synthetic assets that track the price of their underlying assets (using price oracles).
		- Debt pool model.
		- Collateral should be provided in the form of SNX tokens.
		- Highly overcollateralised: ~500%, meaning that $500 (of SNX) ~ $100 (of synthetic assets).
	- UMA: does not rely on price oracles, but relies on liquidators, who are financially incentivised, to find improperly collateralised positions and liquidate them (hence allows for adding a very long tail of synthetic assets that otherwise wouldn’t have a reliable price feed).
	- Hegic: American style options
	- OPyn: European style options.
	- Perp: perpetual contracts (all being processed using the xDai Chain — a Layer 2 solution, hence almost no gas fees).
	- dYdX: derivatives exchange that offers spot, margin and perpetuals trading.
		- Architecture: combines non-custodial, on-chain settlement with an off-chain low-latency matching engine with order books.
		- Perpetual trading on Zk Rollups.
	- BarnBridge: a risk tokenising protocol that allows for hedging yield sensitivity and price volatility (by accessing debt pools of other DeFi protocols, and transforming single pools into multiple assets with different risk/return characteristics).
		- Smart Yield Bonds: interest rate volatility risk mitigation using debt based derivatives.
		- Smart Alpha Bonds: market price exposure risk mitigation using tranched volatility derivatives. 
		- Liquidity mining, distributing its own token BOND.

**DeFi — Future of Finance?**
- Instead of relying on old and inefficient infrastructure, Decentralised finance, or DeFi, leverages the power of cryptography, decentralisation and blockchain to build a new financial system. A system that can provide access to well-known financial services such as payments, lending, borrowing and trading in a more efficient, fair and open way.
- Key metrics in DeFi:
	- TVL (Total Valued Locked)
	- DEX Volume (trading volume across decentralised exchanges)
- GameStop short squeeze:
	- GameStop (GME) 是一家实体游戏零售商，股价因业绩和行业变化长期低迷。
	- 大量对冲基金认为 GameStop 股价会跌，进行了大量做空（short selling），即借股票卖出，希望股价下跌后低价买回赚差价。
	- 但有一群散户投资者（主要聚集在Reddit论坛的r/WallStreetBets）发现大量做空头寸后，开始大量买入GameStop股票。
	- 散户的买入推高股价，迫使做空的对冲基金被迫回补空头（买回股票止损），导致股价进一步上涨，形成了**空头挤压（short squeeze）**。
	- 股价在几周内从约20美元飙升至最高约480美元。
	- **Robinhood**作为一个流行的零佣金交易平台，在股价飙升期间限制了GameStop股票及其他被散户炒作的股票交易，引发用户和公众强烈争议。
	- This is an instance of centralised finance.
- A DeFi solution of DEX: Uniswap.
- Challenges:
	- More security responsibilities to the users: there is no handholding but only direct interaction with new DeFi protocols.
	- Regulatory requirement like KYC.
	- Scaling problem: high gas fees resulting from high demand of the ethereum –> already have a solution to this: **Layer 2** and **Rollup**.
	- Hacks.
	- Whales and voters apathy in certain governance models.
	- How to implement collateralised loans and mortgages? –> One try: Aave.

**High Gas Fees**
- Gas price: the main reason for having a separate unit (i.e. gas price) for measuring computational effort is to decouple it from the price of ETH. 
	- This means that the increase in the ETH price should not change the cost of transactions. If the network activity stays the same and the price goes up we should see the gas price going down, so the final transaction cost measured in ETH stays the same in dollar value.
- Solutions:
	- Layer 2.
	- 1inch exchange: mint CHI tokens (and create dummy smart contracts) when the gas fee is low, and burn CHI (hence destroy smart contracts) to get gas refund.

**Binance Smart Chain (BSC) and CeDeFi**
- Binance Chain: a high-speed blockchain (based on Tendermint consensus model) able to support large transaction throughput.
- Binance Smart Chain: to accommodate smart contracts (thus sacrificing its performance).
	- Instead of creating from scratch, they forked Ethereum’s go client – geth.
		- This allowed the network to quickly bootstrap its ecosystem by essentially either reusing or forking all popular Ethereum services and applications.
		- Pancakeswap: a fork of Uniswap.
		- Venus: a fork of Compound.
		- Autofarm: a protocol resembling Yearn.
	- And optimise this new chain for low fees and higher transaction throughput by sacrificing decentralisation and censorship-resistance properties of the network.
	- Adopted the **Proof-of-Staked-Authority** model, tweaked a few other parameters such as the block time and the gas limit per block.
		- Staked Authority: Active validators are determined by ranking all validators based on the amount of BNB tokens they hold. The top 21 validators with the highest amount of BNB become active and take turns validating blocks. This is determined once per day and the set of all validators is stored separately on Binance Chain.
		- Has higher transaction throughput and faster confirmation time, but requires larger data storage (but the 21 validators can just run their nodes on institutional-grade hardware).
		- Centralising aspect: Currently, with an average block size of 40,000 bytes, Binance Smart Chain grows by around 1.15 GB per day which is around 420 GB per year. After a couple of years, this of course eliminates most of the consumer-grade hardware.
- CeDeFi:
	- A mixed solution between centralized and decentralized finance which Binance Smart Chain is a good example of.
	- CeDeFi allows users to get a feel for using DeFi without paying high transaction fees.

**Polygon (Matic)**
- Ethereum's Internet of Blockchains.
- Initial goal (as Matic): to tackle Ethereum’s scaling problems.
- Solutions:
	- Plasma Chains: a Layer 2 scaling solution, secured by the main layer, the Ethereum.
	- PoS Chain: a Ethereum sidechain (or rather, a **Commit Chain**, secured primarily by its own separate PoS consensus mechanism (ultimately relying on Ethereum's PoS), EVM-compatible.
- New goal (when rebranded Polygon): to connect multiple different scaling solutions (Layer 2, sidechains).

**Uniswap V3**
- V1: Nov 2018, ERC20–ETH liquidity pools.
- V2: May 2020, ERC20–ERC20 liquidity pools.
- V3:
	- Better capital efficiency, reduced downside risk.
	- Multiple fee tiers:
			- 0.05% for stable pairs,
			- 0.3% for standard pairs,
			- 1% for exotic pairs.
	- Advanced Uniswap Oracle.
	- Key: **Concentrated liquidity**: V3 creates individualised price curves for each of the liquidity. providers
		- Offers capital efficiency.
		- **Active Liquidity**: when the price moves outside of the LP's price range, LP's price range can be updated. 
			- Although it is entirely possible that there will be no liquidity at a specific price range, in practice this would create an enormous opportunity for liquidity providers to indeed provide liquidity to that price range and start collecting all trading fees.
		- **Range Limit Orders**:
		- **Non-Fungible Liquidity**: as each LP can basically create their own price curve, the liquidity positions are no longer fungible and cannot be represented by well-known ERC20 (i.e. fungible) LP tokens, but are rather tracked by ERC721 (i.e. non-fungible) LP tokens.

**Truth about DeFi**
- Challenges:
	- Lack of smart contract **composability** between different scaling solutions: a single transaction may need to interact with multiple different DeFi protocols.
	- Lack of **interoperability** between different scaling solutions: e.g. borrow funds on Aave on the Matic PoS Chain but later want to swap them using Uniswap on Optimism.
- Truth: at this point, no one can be certain what the future of DeFi will look like.

**Defi Hacks an Exploits**
- **“Rekt”** is internet slang that comes from the word **“wrecked.”**
	- In crypto, gaming, and online communities, it means:  
		- Suffering a big loss (for example, losing money in a rug pull or bad trade)  
		- Getting badly defeated (like losing hard in a game).
	- It’s used informally, like:
		- _"I got rekt."_ → _I lost badly / I got destroyed._
		- _"He got rekt by that scam."_ → _He lost everything because of that scam._
- The **Rug Pull** 圈钱删号跑路: suddenly removing the majority of liquidity from a liquidity pool.
	- Lesson: check how the liquidity is locked, is there a timelock, is there a multisig? Do you know anything about the team?
- Economic exploit / Flash Loan: "hacks and exploits".
	- The flash loans can then be used to take advantage of loopholes in code, or to manipulate pricing and profit from arbitrage.
	- Attack on Harvest Finance:
		1. Take a $50m USDT flash loan.
		2. Swap 11.4m USDC to USDT –> causing USDT price to go up.
		3. Deposit 60.6m USDT into Vault.
		4. Exchange 11.4m USDT to USDC –> USDT price goes down.
		5. Withdraw 61.1m USDT from Vault –> resulting in 0.5m USDT profit.
		6. [Rinse and repeat 32 times.](https://etherscan.io/address/0xf224ab004461540778a914ea397c589b677e27bb) (without any prior testing).
		7. [Convert to renBTC](https://app.zerion.io/0x3811765a53c3188c24d412daec3f60faad5f119b/history) and exit to BTC and [ETH](https://etherscan.io/tx/0x5abe6f9b498471042f6c9f68c63fc3d84398b95a3a9e58c621cee09b3c972879) via Tornado Cash (a service that allows for making anonymous transactions on Ethereum, therefore covering the attacker’s tracks).
	- Other malicious usage of flash loans:
		- re-entrancy,
		- front-running,
		- Arbitrage.
- Arbitrage exploit.
- An audit is not a guarantee of safety!

**Polygon PoS Chain**
- **Sidechains**: 
	- run in parallel or “on the side” of the main chain.
	- have their own consensus mechanisms usually in the form of Proof-Of-Stake (PoS), Delegated-Proof-Of-Stake (DPoS) or Proof-Of-Authority (PoA).
	- 2-way bridge: for sending/withdrawing tokens from the main chain to a side chain and conversely, typically controlled by several PoA signers, causing security risks.
- Polygon PoS Chain is a **Commit Chain** rather than a typical sidechain:
	- PoS , and everyone can become a validator by staking their MATIC tokens and running a full node.
	- **The staking is on Ethereum, the main chain.**
	- **Heimdall Chain**:
		- Use Tendermint consensus to select Checkpoint proposers, but select a new one only if the previous Checkpoint has been successfully submitted to the Ethereum mainnet.
		- **Checkpointing**: aggregating blocks produced by Bor into a single Merkle root and periodically publishing it to the Ethereum main chain. If failed, republish the previous checkpoint until succeeded.
	- **Bor Chain**:
		- Block producer layer of the Polygon PoS Chain.
		- Block producers are popped up from a (periodically) shuffled set of validators (weighted by their stake amount of MATIC). This set is robust.
	- 2-way bridge: secured by a robust set of validators rather than PoA.
	- The Polygon PoS Chain contract deployed on the main chain is considered to be the ultimate source of truth, and therefore all validation is done via querying the Ethereum main chain contract.

**Thorchain**
- Goal: to swap between native assets across different blockchains.
- Previous solutions: represent external assets (e.g. Bitcoin) in the form of wrapped or synthetic tokens.
	- Tradeoffs: custody and/or security.
- Solution: Thorchain, a decentralized liquidity protocol that allows the swap of native assets between different blockchains (Bitcoin, Ethereum, BSC).
	- A "cross-chain Uniswap".
	- Uses a liquidity pool model.
	- Core: a network of nodes built with Tendermint and Cosmos SDK (hence PoS).
		- Tendermint BFT model: allows the network to reach consensus even if up to 1/3 of all the nodes start failing.
		- Example: sends Bitcoin from Bitcoin network to the Ether network:
			1. On Bitcoin network: user sends a Bitcoin transaction to the Bitcoin vault (a Bitcoin address controlled by the Thorchain network).
			2. On Thorchain: nodes keep monitoring vault addresses in order to acknowledge new transactions.
			3. On Thorchain: for the above inbound transaction, the witness transaction is initially recorded as in the "pending" state.
			4. On Thorchain: after the majority of nodes agree on the inbound transaction, the state is muted to "finalised".
			5. On Thorchain: once the inbound transaction becomes "finalised", the Thorchain protocol initiates a swap.
			6. On Ether: the vault (controlled by Thorchain) sends Ether to the user.
		- How to control vault addresses on other blockchains?
			- Use Threshold Signature Scheme (TSS): a better version of multisig.
				- Multisig is usually implemented on the application layer (as a smart contract).
				- TSS is a cryptographic primitive, regardless of the blockchain.
			- Inbound vaults: 2/3 for TSS.
			- Outbound vaults: one signature suffices.
		- PoS on Thorchain: staking (a.k.a. **bonding**) RUNE tokens (for signers, but not validators).
			- **Churning**: every 50000 blocks, replace the active set of signer nodes by the standby set, and so on it goes.
			- Currently on a multi-chain chaos network (but it should soon become the mainnet).
	- Comparison with Uniswap:
		- Uniswap allows for swapping only ERC-20 (using associated wrapped or synthetic tokens), but Thorchain allows for swapping all native assets without wrapping them.
		- Thorchain charges a dynamic slip-based fee, making the **sandwich attack** more difficult.
		- The swapping time on Thorchain depends on the blockchains that the swapped assets are on.
		- Lack of composability of decentralised applications on Thorchain.
		- Thorchain relies on strong economics incentives (RUNE tokens), so it is less decentralised (but this not quite a big problem in view of its usage for only swapping).

**Sushi**
- Recall: back then know as SushiSwap, it was forked from Uniswap & used a Vampire attack.
- New products:
	- SushiBar:
		- A smart contract where SUSHI holders have to stake their SUSHI (to get xSUSHI) in order to benefit from profit sharing. When one redeems xSUSHI, one gets the original amount of SUSHI plus additional rewarded SUSHI.
	- Onsen: a liquidity incentive system that accelerates new projects by providing extra rewards in the form of SUSHI tokens.
	- BentoBox: a special smart contract that acts as a vault for certain tokens.
		- A pool of funds that can be used by Bento-enabled applications in the Sushi ecosystem.
	- Kashi (“lending” in Japanese): a (Bento-enabled) lending platform.
		- Can short an asset.
		- Requires a reliable price oracle.
		- Adding a new risky asset to one of the existing money markets would threaten the solvency of the whole protocol: it may make the account undercollateralised.
	- Miso: a launchpad for new tokens/protocols.

**Bank Run — Iron Finance Fiasco**
- Aiming at creating an ecosystem for a partially collateralised algorithmic stablecoin.
- Mechanism: 
	- Peg the price of IRON/USDC by minting/burning TITAN.
	- While redeeming IRON, you get TITAN for the extra value in additional to previously collateralised USDC.
	- Whales started removing liquidity from IRON/USDC and then started selling their TITAN to IRON, then selling IRON to USDC directly via liquidity pools, causing the TITAN token price to drop.
	- Other users panicked and started selling TITAN, the **time-weighted price oracle** used for reporting TITAN prices started reporting **stale prices** that were still higher than the actual market price of TITAN, thus causing a death spiral (redeem IRON for USDC and TITAN and sell TITAN immediately). The price of TITAN goes to almost 0 and the impermanent loss of the liquidity pool become almost 100%.

**Rollups**
- The ultimate Ethereum scaling solution.
- Executes transactions, takes the data, compresses it and rolls it up to the main chain in a single batch, hence the name – a rollup.
- Question: How does Ethereum know that the posted data is valid and wasn't submitted by a bad actor trying to benefit themselves?
	- **Optimistic rollups** use fraud proofs.
		- The party that is able to submit batches of transactions to layer 1 has to provide a bond, usually in the form of ETH. Any other network participant can submit a **fraud proof** if they spot an incorrect transaction.
		- The system enters the dispute resolution mode to see whether the transaction is invalid or the fraud proof is incorrect.
	- In contrast, **Zk rollups** use validity proofs.
		- This is possible by leveraging a clever piece of cryptography called **Zero-Knowledge proofs** hence the name ZK rollups.
- Comparison:
	- Optimistic rollups:
		- Easier EVM-compatibility.
		- Computation-easy.
	- Zk rollups:
		- Hard to create an EVM-compatible Zk rollup.
		- Computation-heavy.
- Challenge: composability between different rollups and fractured liquidity.

**DeFi 2.0 — A New Narrative?**
- The experimentation centres around the innovation in the liquidity mining design and is very often associated with protocols **owning their own liquidity** instead of temporarily renting it out via liquidity mining incentives. Adding vesting 锁仓期 is not enough.
- Building a "moat" 护城河 around the protocol.
- Examples: OlympusDAO, Tokemak

**Perpetual protocol**
- Perpetual Protocol is a DeFi project with the main goal of creating the best, most accessible and most secure DEX (decentralised exchange) for perpetual futures. 
- Perpetual Protocol was founded in 2019 by a small team of startup founders and software engineers. Initially called “Strike”, the project pivoted to perpetual futures and changed its name in the summer of 2020. 
- The first version of the protocol was launched on the xDai network in December 2020. 
- Version 2 of the protocol named Curie after the famous scientist and a Noble Prize winner - Marie Curie, launched on Optimism (Layer 2 solution) on the 31st of November 2021. 
- The design of Perpetual Protocol that we're going to explain later is extremely interesting as it leverages the DeFi “money legos” ethos to both build upon other already existing DeFi projects as well as provide building blocks for other protocols in the future. 
- Perpetual Protocol is one of the projects that focus on derivatives in DeFi.
- The main derivative product: perpetual futures.
	- Funding rate: to make sure that the price of the perpetual contract does not diverge too much from the actual price of their underlying assets.
	- Easy access to leverage, but could also be dangerous!
- Perpetual Protocol:
	- Launched on Layer 2: scalable, low transaction fees, high transaction throughput
	- Builds upon **Uniswap V3**: providing liquidity, and leveraging the DeFi “money legos” ethos in a completely permissionless way.
	- Uses **Clearing House** contract: minting and burning **v-tokens** (virtual tokens).
	- Uses *cross* margin mode.
	- Can use isolated margin mode by creating separated wallets.

#defi2022
**DeFi — Past, present and future**
- Keep optimistic in the current market cooldown?

#defi2022
**FTX collapse**
- Founder: Sam Bankman-Fried (SBF), graduated in 2014 from MIT with a degree in physics, started working full-time in Jane Street Capital, launched in 2017 the Alameda Research (quant trading company focused on the crypto market), alleged to believe in "Effective Altruism", secured profits from a big arbitrage opportunity created by price discrepancies of Bitcoin traded in American and Asian exchanges, launched in 2019 FTX.
- Rise To Power in 2021 : liquidity supplied by Alameda Research itself, invested by Sequoia Capital, Soft Bank, Tiger Global, etc.
- Controversy: SBF's legislation lobbying at the detriment of DeFi.
- The Collapse in 2022:
	- Insolvency rumours: a leaked balance sheet of Alameda shows that most of the funds comes from FTT, the token of FTX, which has a small float (only a small portion of the total supply of the token was actively traded).
	- Binance wanted to exit their investment on their rival FTX, but FTX decided to pay back using stable coins and FTT. Worried by insolvency rumours, CZ decided to sell their FTT position. CZ revealed a big hole (lending funds to Alameda at some point during the 3AC Saga) in the FTX balance sheet.
- Impact:
	- Solana market impacted: Solana had FTX and Alameda as big supporters, and wrapped assets on Solana such as BTC and ETH were backed by FTX and Alameda.
	- BlockFi stopped withdraws: BlockFi had offered a $400m credit facility to FTX.
	- Damaged the already shaken reputation of crypto industry.
- The Path Forward:
	- more centralisation (regulation),
	- On-chain transparency, self-custody, fair access, self-regulation by protocols — whose codes can be fully audited by anyone.

#defi2023 
**Staking withdrawals**
- **Shanghai/Capella** (a.k.a. **Shapella**) upgrade: enabled Staking Withdrawals.
- Mechanism:
	- **Full scan**: Once withdrawals are enabled, a validator proposing a block will scan linearly through validator indices to find the first 16 validators with 0x01 credentials who either:
		- have a balance that exceeds 32 ETH (accrued validator rewards), or
		- are "withdrawable" (have fully exited validator set).
	- For each block: **the linear search stops after either finding 16 validators** to match these criteria or after 16384 iterations. The algorithm remembers the index at which the search stopped, so the next validator proposing a block can resume from that index. After getting to the last index, the algorithm starts from the beginning — the index 0.
	- After the scan is completed, the validator creates a list of withdrawals to be included in their execution payload.

#defi2023
**MEV**
- Maximal Extractable Value: additional profit resulting from block proposer's altering the transaction sequence.
	- Frontrunning, backrunning, sandwich attack, etc.
- PGA (Priority Gas Auction) era:
- Flashbots era: to address the negative externalities of MEV in a transparent and community-driven manner.
	- Two integral tools: MEV-Geth and MEV-Relay.
- Post-Merge Era: uses MEV-Boost, a type of proposer-builder separation (PBS) design.
	- PBS allows validators to effectively use third-party block builders for their block-building duties.
- In the future:
	- Two new initiatives: MEV-Share and SUAVE.

#defi2024
**EIP-4844**
- a.k.a. Proto-danksharding: it lays the foundation for further scaling with danksharding in the future.
- Architecture: a new transaction type that accepts “blobs” of data to be persisted in the beacon node for a short period of time.
	- It could reduce transaction fees on L2s by over 90% (if the demand does not increase too much).

#defi2024
**DeFi Renaissance — Ethereum, L2s, Solana**
- Fall 2024: emerging from the bear market, it is a period revolutionising the way we think about decentralised finance.