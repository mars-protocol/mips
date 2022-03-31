# Mars Improvement Proposals (MIPs)


The Martian Council is a smart contract governance DAO comprised of all xMARS holders and the original Mars builders who hold smart-contract-locked MARS. Governance proposals are made by a member of the Martian Council to the entire Martian Council. Of course, any person can draft and publish a governance proposal–but it does not become votable unless proposed by a Martian Council member in accordance with the Mars governance protocol (which includes an MARS deposit requirement). 
Governance proposals may cover any topic related to Mars; however, the exact nature of these proposals–and the consequences of an approval or rejection–will vary depending on the category and topic of the proposal. 
The Martian Council only has binding governance power over the configurable parameters of specific copies of Mars deployed as smart contracts to Terra (Mars Smart Contracts). The Mars Smart Contracts are directly responsive to the governance decisions of the Martian Council, and therefore are under the Martian Council’s direct control. This includes control of whether, when and how to spend MARS in the Treasury (initially 10% of MARS total token supply) and the setting of slippage caps on the Mars Smart Contracts autonomous swaps of assets to UST, governance quorum and approval thresholds, etc.
The following timeline gives an overview of the MIP process, which is detailed below:


![assets/image1.png](assets/image1.png)

## Overview

### Definitions

#### MIPs

MIPs are standardized documents subject to community feedback and voting that, once enacted, define the behavior of the Martian Council and the Mars Protocol.

There are two main categories of Martian Council governance proposals:

1. **Binding proposals:** Are proposals to make changes to the configurable aspects of the Mars Smart Contracts; because the Martian Council controls these smart contracts, the Martian Council’s vote is both necessary and sufficient to approve these changes. 


2. **Signaling proposals:** Are all other governance proposals made to the Martian Council–for example, signaling a preference for certain code or functions to be added to Mars or the [marsprotocol.io](https://marsprotocol.io/) website. Signaling proposals (including this proposal) are voted upon on-chain in the same way as binding proposals. However, because these proposals require off-chain implementation actions by extrinsic parties–such as a website operator, a smart contract developer, or others–the Martian Council’s approval is neither necessary nor sufficient to cause these proposals to be implemented. Therefore, these proposals merely signal the Martian Council’s support for or opposition to the proposed outcome.

We foresee four main governance proposal topic categories: 


1. **Technical Proposals:** Certain proposals for changes to certain configurable aspects of the Mars Smart Contracts (binding), which can be modified directly by on-chain votes, or code changes to the Mars Protocol (signaling), which require upgrading the protocol.

2. **Red Bank Asset Listing Proposals:** Proposals to add or remove support for one or more assets within the Red Bank (typically binding).

3. **Credit Line Extension Proposals:** Proposals from developers aiming to secure a virtual “credit line” from the Red Bank for unique applications such as leveraged yield farming (binding or non-binding, depending on whether code is ready and deployed on chain at time of proposal).

4. **General Proposals:** All other proposals impacting areas such as the treasury, governance, and tokenomics (mix of binding and non-binding). If you feel that your API does not fit in any pre-existing sub-categories, you can simply leave it as General.

All proposals should follow the following steps:



1. Post a Mars Request for Comment (MRC) on the Mars Protocol Forum. Note that formal requests for comment should follow the naming convention proposed here: MRC-#: [Title of MRC]. Submitters should replace the “#” with the number of the MRC based on the order in which it was submitted and the title should match the content of the request.

2. Submit a formalized Mars Improvement Proposal (MIP) that adheres to the specifications below for on-chain voting.

3. If approved, the MIP will be implemented (binding MIPs) or may be implemented (signaling MIPs). Implementation of binding MIPs depends only on Terra validators following the Terra protocol. Implementation of signaling MIPs depends upon many factors, including the willingness and availability of off-chain actors to perform the work needed to implement the MIP. 



If you feel that your API does not fit in any pre-existing sub-categories, you can simply leave it as General.

### Authoring and Proposing

MIPs can be brought forth and proposed by anyone.

If you're interested in proposing a MIP, please read below for more details around the lifecycle of a MIP as well as templates you should use to submit your ideas to the Mars community.

### Getting Started with MIPs (for Authors)

MIPs are written using Markdown and hosted on GitHub. Please note that all MIPs (and their associated MRCs) must conform to specific templates!

### Markdown

Markdown is a very simple markup language for formatting text, i.e., adding headers, bullet lists, italicized text, et cetera. When working with MIPs, you should use GitHub-flavored Markdown.

> [GitHub’s Mastering Markdown](https://guides.github.com/features/mastering-markdown/) will get you up to speed in no time. The online Markdown editor [HackMD](https://hackmd.io/) is a solid platform for practice and production.

### GitHub

[GitHub](https://github.com/) is a code hosting platform for version control and collaboration built on [git](https://git-scm.com/), a version control software. GitHub is complex and may seem daunting at first, but only a basic familiarity is necessary for our purposes.

> We recommend that you read these two short guides: [Hello World](https://guides.github.com/activities/hello-world/) and [Forking Projects](https://guides.github.com/activities/forking/).
> 

### Templates

- Technical MIPs must conform to the [Technical MIP Template](https://github.com/mars-protocol/mips/blob/main/Technical-MIP-Template.md).
- Red Bank Asset Listing MIPS must conform to the [Red Bank Asset Listing MIP Template](https://github.com/mars-protocol/mips/blob/main/Red-Bank-Asset-Listing-MIP-Template.md).
- Credit Line Extension MIPs must conform to the [Credit Line Extension MIP Template](https://github.com/mars-protocol/mips/blob/main/Credit-Line-Extension-Risk-Framework.md).
- General MIPs must conform to the [General MIP Template](https://github.com/mars-protocol/mips/blob/main/General-MIP-Template.md).

### Proposing

Once you've picked the appropriate template for your proposal and have a workable draft, the next steps are the following two tasks:

- Post an Mars Request for Comment (MRC) on the [Mars Forum](https://forum.marsprotocol.io/) (note that [Red Bank Asset Listing Proposals](https://github.com/mars-protocol/mips/blob/main/Red-Bank-Asset-Listing-Risk-Framework.md) and [Credit Line Extension proposals](https://github.com/mars-protocol/mips/blob/main/Credit-Line-Extension-Risk-Framework.md) must include a risk framework analysis as detailed here: [Red Bank Asset Listing Risk Framework](https://github.com/mars-protocol/mips/Red-Bank-Asset-Listing-Framework.md) and [Credit Line Extension Risk Framework](https://github.com/mars-protocol/mips/Credit-Line-Extension-Risk-Framework.md))
- Submit the MRC to the GitHub MIP repository

After the two above tasks have been completed, MIP Editors will help assign a number for the proposal. The proposed MRC will then enter a period of community feedback. This is a great opportunity to iterate on your proposal. Once the feedback period is over and you've incorporated your final changes, there will be a one-week period (5 days for feedback plus a 2-day freeze period where the original post cannot be edited) before you can formally submit the proposal for voting as an MIP. Lastly, your proposal will go through a voting period.

For a more detailed breakdown of the full MIP lifecycle, check out MIP-0.

### License

The MIP framework was inspired by the [Astroport Improvement Proposal Framework](https://github.com/astroport-fi/aips).