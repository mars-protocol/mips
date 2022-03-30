# The Credit Line Extension Risk Framework

Contract-to-contract (C2C) lending will be one of Mars key features and differentiators. C2C lending, as its name indicates, refers to lending activity that happens between Mars and other smart contracts (thus contract-to-contract), as opposed to between Mars and individual users. From the point of view of other protocols, C2C lending will be a powerful tool that could allow them to innovate on top of Mars by tapping into its liquidity. For Mars, on the other hand, these protocols will effectively represent a new source of demand for the protocol, making its money markets more attractive for depositors and the whole protocol more useful.
Naturally, C2C lending also poses additional risks for Mars. These risks stem from a number of different sources, from the particular use case given to the borrowed assets to the technical and centralization risks associated with the smart contract (SC) borrowing the assets. In this sense, one of the most important goals when designing Mars C2C lending capabilities was to develop a robust and conservative architecture that would maximize the safety of user funds.
One of the tools intended for this purpose is the C2C lending risk framework, which aims to mitigate the risks involved in this process by standardizing the way in which those risks are measured and providing a conservative and thorough methodology for determining:
Content on this page should be migrated to GitHub with the title Credit Line Extension Risk Framework: 

1. Whether a given SC[^1] should be extended a loan. 
2. The specific risk parameters associated with that loan.

    [^1]: This framework will specifically focus on SCs requesting loans to deploy them in leveraged yield farming strategies, but could be expanded eventually to incorporate other use cases.

Throughout this post, this framework will be explored in detail. In the first section, a high-level overview of the new SC loan assessment process will be presented. The next two sections will cover the minimum requirements a new smart contract needs to meet to be considered safe under the risk framework. Lastly, the final sections cover the risk parameters definition methodology.
The overall purpose of the post is to lay the groundwork for a proposal to Mars governance that the framework be adopted as a minimum safety standard for assessing eligibility of new smart contracts to be extended loans. Note: since no person or centralized group controls Mars, it will be up to the Mars community to adopt and enforce this minimum safety standard.

## SC Loan Assessment Process

For a new SC to be extended a loan it should meet a minimum set of requirements at three different levels:

1. The SC requesting the loan itself (from here on the Base SC). This first filter is intended to guarantee a minimum level of quality and safety of the Base SC. 
2. Other SCs (or protocols) the Base SC interacts with. This filter is intended to mitigate the risk of extending loans to SCs that interact with vulnerable or risky protocols. 
3. The assets the SC interacts with. For leveraged yield farming (which is the focus of this framework), these assets refer to the pair of assets used to provide liquidity and yield farm. The objective of this third filter is to reduce the risk of exposing Mars funds to low quality assets.

Mars governance can decide whether to conduct the above process on a case-by-case basis or to whitelist protocols and/or assets to speed up the process going forward. The whitelisting process would require a formal governance vote in which it is decided that a certain protocol or asset that has already met the requirements doesn’t need to be reviewed each time a new loan is requested (this could make sense, for instance, for protocols or assets where several leveraged yield farming strategies have been or are expected to be deployed).
Now, only when an application passes the above filters should governance proceed to establish the specific risk parameters for the leveraged yield farming strategy.



## Base SC Assessment

The first filter a new SC must pass in order to be extended a loan under this framework relates to the safety and quality of the SC itself (the Base SC). This safety will be measured through the risks associated with that SC. Specifically, it will need to meet the following set of minimum requirements:


### Technical quality:
* Audited by a reputable firm. 
* High quality code: 
  * Written with best practices or using battle-tested code. 
  * Adequate, thorough documentation. 
  * High quality tests, including unit tests and integration tests. 
* Significant bug bounty for a minimum of 2 weeks. 
  * On testnet: Minimum $1M for critical bugs. 
  * On mainnet: Minimum $3M for critical bugs.
### Trust minimization:
[https://docs.marsprotocol.io/mars-protocol/protocol/welcome-to-mars/c2c-lending-credit-line-extension-risk-framework](https://docs.marsprotocol.io/mars-protocol/protocol/welcome-to-mars/c2c-lending-credit-line-extension-risk-framework)

Desired destination link: [https://github.com/mars-protocol/mips/Credit-Line-Extension-Risk-Framework.md](https://github.com/mars-protocol/mips/Credit-Line-Extension-MIP-Template.md)