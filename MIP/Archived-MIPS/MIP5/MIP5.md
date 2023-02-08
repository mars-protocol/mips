**New Credit Line Extension: Apollo ANC-UST Astroport Strategy**

**Description of the Proposal**

Apollo DAO is a yield management and auto-compounding platform on Terra. We propose providing Apollo DAO with access to a credit line from Mars to enable ANC-UST leveraged yield farming on Apollo. This would initially be for the ANC-UST Astroport based vault and would allow users to leverage their vault positions.

**Value Proposition**

Apollo DAO currently has $40m in TVL and provides users access to a large number of auto-compounding Terra vaults. Apollo will continue to add new vaults, including bLuna/Luna, stLuna/Luna, nLuna and nEth. We also provide other benefits, such as being able to farm Apollo tokens, with all revenue that Apollo generates going to the Warchest.

By enabling a credit line for Apollo DAO, it would increase UST borrowing from Mars, incentivising more deposits to Mars and increasing Mars’ profitability and fees.

In the future, Apollo also aims to boost their vaults through Astroport’s “Boosties”. The combination of leveraged yield farming, Astroport “Boosties” and Apollo rewards will provide unrivaled rewards for farmers driving borrowing demand on Mars.

The Apollo Warchest also holds nearly 300k Mars tokens, which provides Apollo DAO with a direct incentive to help Mars grow, but also a strong incentive to maintain the safety and security of Mars’ funds. Apollo’s initial implementation of leverage yield farming is heavily based on the leverage yield farming contracts created by the Mars team, with only a few small modifications, which will allow us to provide Apollo rewards to farmers.

**Basic Information**

Apollo

* Project website. [app.apollo.farm](http://app.apollo.farm)
* Project documentation. [articles.apollo.farm](http://articles.apollo.farm)
* Communities. [Twitter](https://twitter.com/ApolloDAO) [Telegram](https://t.me/apollodao) [Discord](https://discord.com/invite/hHvrqk6qTT)

Anchor

* Project website. https://www.anchorprotocol.com/
* Whitepaper. https://www.anchorprotocol.com/docs/anchor-v1.1.pdf
* Project documentation. https://github.com/Anchor-Protocol
* Communities.: [Telegram](https://t.me/anchor_official), [Twitter](https://twitter.com/anchor_protocol), [Discord](https://discord.gg/9aUYgpKZ9c)

Astroport

* Project website. https://astroport.fi/
* Whitepaper. https://astroport.medium.com/astroport-litepaper-1fab783b77b5
* Project documentation. https://docs.astroport.fi/astroport/
* Communities. [Twitter](https://twitter.com/astroport_fi) [Telegram](https://t.me/astroport_fi) [Discord](https://discord.gg/astroport)

**Technical Risk**

The base smart contract (the smart contract that would receive the credit line) as well as the various smart contracts the strategy interacts with have been audited as follows:

* Apollo Audit Report: [Oak 1](https://github.com/oak-security/audit-reports/blob/master/Apollo/2021-08-18%20Audit%20Report%20-%20Apollo.pdf), [Oak 2](https://github.com/oak-security/audit-reports/blob/master/Apollo/2022-03-17%20Audit%20Report%20-%20Apollo%20v1.0.pdf)
* Fields of Mars audits: [Oak](https://github.com/oak-security/audit-reports/blob/master/Mars/Audit%20Report%20-%20Fields%20of%20Mars.pdf), [Halborn](https://github.com/HalbornSecurity/PublicReports/blob/master/CosmWasm%20Smart%20Contract%20Audits/Mars_Protocol_Fields_of_Mars_CosmWasm_Smart_Contract_Security_Audit_Final.pdf)
* Astroport Audits: [Oak](https://github.com/astroport-fi/astro-audits/tree/main/oak), [Halborn](https://github.com/astroport-fi/astro-audits/tree/main/halborn)
* Anchor Audits: [Anchor Protocol SC by Cryptonics](https://anchorprotocol.com/docs/Audit%20Report%20-%20Anchor%20Protocol%20[20210308].pdf), [Anchor Token and Distribution SC by Cryptonics](https://anchorprotocol.com/docs/Audit%20Report%20-%20Anchor%20Protocol%20[20210406].pdf), [EthAnchor Report by Solidified](https://anchorprotocol.com/docs/Audit%20Report%20-%20EthAnchor%20[09.07.2021].pdf)

In terms of the quality of the smart contracts, as mentioned above, Apollo will use a slightly modified version of the current Fields smart contracts, which have been live for more than a month on mainnet working properly. Additionally, these contracts have been audited several times and have an active bug bounty on Immunefi.

Other Relevant Links:

* GitHub page where source code is hosted.
  * Apollo: https://github.com/apollodao/apollo-fields-of-mars

* Anchor: https://github.com/Anchor-Protocol
* Astroport: https://github.com/astroport-fi

* On-chain contract.
  * Astroport ANC-UST Pair: terra1qr2k6yjjd5p2kaewqvg93ag74k6gyjr7re37fs
  * Astroport ANC-UST LP: terra1wmaty65yt7mjw6fjfymkd9zsm6atsq82d9arcd
  * ANC contract address: terra14z56l0fp2lsf86zy3hty2z47ezkhnthtr9yq76
  * Apollo ANC-UST Strategy: ​​terra1j5ec7ecssqvyfxfzguuxghrc9ahz8h35a9lxdp
* Testnet contract (only applies for Base SC).
  * Apollo ANC-UST Strategy: terra1lanxgewats337t49mnkaeh5g098j2g7e87k87s

**Centralization Risk**

For the Base smart contract (SC):

Apollo

* SC upgradability: How is the SC upgradable? Is it immutable, DAO upgradable or controlled by a multisig? If it’s a multisig, what does it control and who are the signers?
  * Contracts are upgradeable by CosmWasm admin feature. Admin is a 3/5 multisig, where the signers are distributed as follows: 2 from the Apollo team, 1 from the Nexus protocol team and 2 Mars contributors.
* Is the SC always in control of the borrowed assets?
  * Yes. Borrowed assets are used to pair with user-supplied assets in liquidity pools, and received LP tokens are staked in Astroport’s Generator contract. These funds can be withdrawn only by the Base SC.
* What oracle is used for the strategy?
  * Mars ANC TWAP Oracle

For the other SCs and assets the Base SC interacts with:

Anchor

* SC upgradability: Anchor currently has an upgradeable multisig in place, controlled by members of the Anchor team. There is a plan in place to change this to a DAO process.

Astroport

* Astroport: 3/5 Multisig comprising of Astroport contributors. In the process of changing to a [DAO governance](https://astroport.medium.com/astroport-development-and-astro-builder-allocation-d112cd51ba61).

**Risk Parameters Suggestions**

Following the [C2C Lending Credit Line Extension Risk Framework](https://docs.marsprotocol.io/mars-protocol/protocol/welcome-to-mars/c2c-lending-credit-line-extension-risk-framework), we calculated the following risk metrics:

* Maximum Intraday Change : 1.44x
* Daily Volatility (30d) : 11.5%
* Daily Volatility (60d) : 9.7%
* Daily Volatility (90d) : 9.0%

Using the above metrics as input, we suggest the following risk parameters for this strategy:

* Maximum Leverage: 2.5x (60% LTV)
* Liquidation Threshold: 2.86x (65% LTV)
* Liquidation Bonus: 5%
* Requested Credit Line Size: 5M UST
* Minimum Position Size: 300 UST
* TWAP Oracle Implementation: Mars ANC TWAP
