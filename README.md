# Mars Improvement Proposals (MIPs)

The Martian Council is comprised of all MARS holders who have staked either directly or via delegation, as well as the Mars Protocol builders who hold [smart-contract-locked MARS](https://github.com/mars-protocol/periphery/tree/main/contracts/vesting).

Note that all MARS holders can cast a vote, however their voting power will be 0 in the event they haven’t delegated or staked. Mars builders are not permitted to stake or delegate any tokens that have yet to vest, but can cast votes and have a voting power that is non zero.

Governance proposals can be submitted to the Martian council by any MARS token holder. The entire process first requires any individual to compose a governance proposal and later publish it on the [Mars forum](https://forum.marsprotocol.io/).  An on-chain governance vote is required to determine whether such a proposal may be implemented. Such a proposal must be submitted in accordance with the Mars governance protocol standards and criteria (which includes an upfront (liquid i.e. unstaked) MARS deposit requirement–see below). 

Governance proposals may cover any topic related to Mars; however, the exact nature of these proposals–and the consequences of an approval or rejection–will vary depending on the category and topic of the proposal. 

The Martian Council only has binding governance power over the configurable parameters of Mars Hub and Mars Outposts deployed as smart contracts to the respective L1 chain. Both Mars Hub and the Mars Outposts are directly responsive to the governance decisions of the Martian Council, and therefore are under the Martian Council’s direct control. This includes control of whether, when and how to spend $MARS that remain in the community pool and the setting of caps on the Mars Outposts, governance parameters such as quorum and approval thresholds, etc. 

However, the Martian Council can also express its preferences on a broader range of Mars-related topics relating to further development of the Mars Protocol, which future Outposts should be developed or, Mars website feature changes, etc. As these dimensions of the Mars community are not under the direct control of the Martian Council, the  governance proposals on these topics should be regarded as signaling the Martian Council’s preferences–i.e. governance proposals on these topics are non-binding and require the assistance of off-chain actors and processes.

In summary, there are two main categories of governance proposals:

1. **Binding proposals:** Are proposals to make changes to the configurable aspects of the Mars Hub and/or the Mars Outposts; because the Martian Council controls these pieces of infrastructure, the Martian Council’s vote is both necessary and sufficient to approve these changes.
2. **Signaling proposals:** Are all other governance proposals made to the Martian Council–for example, signaling a preference for certain code or functions to be added to Mars or the marsprotocol.io website. Signaling proposals (including this proposal) are voted upon on-chain in the same way as binding proposals. However, because these proposals require off-chain implementation actions by extrinsic parties–such as a website operator, a smart contract developer, or others–the Martian Council’s approval is neither necessary nor sufficient to cause these proposals to be implemented. Therefore, these proposals merely signal the Martian Council’s support for or opposition to the proposed outcome.

We foresee four main governance proposal topic categories:

1. **Technical Proposals:** Certain proposals for changes to certain configurable aspects of Mars Hub and/or the Mars Outposts (binding), which can be modified directly by on-chain votes, or code changes to the Mars Protocol (signaling), which require upgrading the protocol.
2. **Red Bank Asset Listing Proposals:** Proposals to add or remove support for one or more assets within the Red Bank (typically binding).
3. **Credit Line Extension Proposals:** Proposals from developers aiming to secure a virtual “credit line” from the Red Bank for unique applications such as leveraged yield farming (binding or non-binding, depending on whether code is ready and deployed on chain at time of proposal).
4. **General Proposals:** All other proposals impacting areas such as the treasury, governance, and tokenomics (mix of binding and non-binding).

All proposals should follow the following steps:

1. Post a Mars Request for Comment (MRC) on the [Mars Protocol Forum](https://forum.marsprotocol.io/). Note that formal requests for comment should follow the naming convention proposed here: MRC-#: [Title of MRC]. Submitters should replace the “#” with the number of the MRC based on the order in which it was submitted and the title should match the content of the request.
2. Submit a formalized Mars Improvement Proposal (MIP) that adheres to the specifications below for on-chain voting.
3. If approved, the MIP will be implemented (binding MIPs) or may be implemented (signaling MIPs). 

The following timeline shows the proposed flow for protocol modifications:

![assets/image1.png](assets/image1.png)

## Abstract

The Mars Improvement Proposals (MIPs) Framework defines all subsequent MIPs to utilize, provides the necessary templates, processes, and guidelines for working within the framework, and defines the key roles required for the operation of the MIPs Process.

## Motivation

For Mars to successfully operate as a fully decentralized and self-sustainable DAO, a formalized process of decision-making is required. In a permissionless protocol, everyone should be able to propose changes and improvements.

The MIP Framework serves to empower each Martian Council participant by giving them a standardized way of interacting with the wider DAO and defining its future shape.

## Specification

### Definitions of the Mars Improvement Proposal Framework

- **Mars Improvement Proposals (MIPs):** MIPs are standardized proposals to the Martian Council to either re-parameterise Mars Hub or the Mars Outposts or signal support for certain off-chain initiatives (such as further development of the Mars Protocol codebase). MIPs can be added, amended, replaced, and removed as required after they are initially published on the [Mars Forum](https://forum.marsprotocol.io/).
- **MIP Types:** MIPs can be one of four types: Technical proposals that impact smart contract code, Red Bank asset listing proposals, credit line extension proposals or general proposals. General MIPs are sub-categorized as treasury, UI, governance, and tokenomics. 
- **Minimum Feedback Period:** The minimum amount of time within which the community can give feedback in response to a proposed MRC before it can advance to an on-chain vote and becomes known as a MIP.
- **Minimum Frozen Period:** The minimum amount of time during which an MRC must remain unchanged before it can advance to an on-chain vote as a MIP.
- **MIP Editor(s):** MIP Editors enforce the administrative and editorial aspects of the overall MIPs process. ***Note:*** *MIP Editors’ approval is not required for a proposal to be valid–running MIPs past the editors is merely suggested as a good practice for having consistent, high-quality, community-recognized proposals.*

### Core Principles

1. **Specificity:** A MIP must define and address a specific behavior or single responsibility.
2. **Completeness:** A MIP must be thorough. Relevant, specific particulars must not be left undefined or unreferenced.
3. **Avoid overlap:** Multiple MIPs must not implement the same type of behavior independently. For instance, there should not be two separate, interchangeable ways to integrate new apps in the Fields of Mars.
4. **Clarity:** A MIP must not have equally valid conflicting interpretations. A MIP must be as clear and easy to understand as possible.
5. **Brevity:** A MIP must be as short as possible, including only what is essential given the other core principles.

### MIP Proposal Type Categories

There are two main categories of Martian Council governance proposals:
1. **Binding proposals:** Are proposals to make changes to the configurable aspects of the Mars Smart Contracts; because the Martian Council controls these smart contracts, the Martian Council’s vote is both necessary and sufficient to approve these changes.
2. **Signaling proposals:** Are all other governance proposals made to the Martian Council–for example, signaling a preference for certain code or functions to be added to Mars or the marsprotocol.io website. Signaling proposals (including this proposal) are voted upon on-chain in the same way as binding proposals. However, because these proposals require off-chain implementation actions by extrinsic parties–such as a website operator, a smart contract developer, or others–the Martian Council’s approval is neither necessary nor sufficient to cause these proposals to be implemented. Therefore, these proposals merely signal the Martian Council’s support for or opposition to the proposed outcome.

#### MIP Topic Categories Categories

There are four potential categories for MIPs:

- Technical MIPs
- Red Bank Asset Listing MIPs
- Credit Line Extension MIPs
- General MIPs

Each category has specific considerations and requirements as detailed below.

##### Technical MIPs

Certain proposals for changes to certain configurable aspects of the Mars Smart Contracts (binding), which can be modified directly by on-chain votes, or code changes to the Mars Protocol (signaling), which require upgrading the protocol. Technical MIPs should be formatted per the [Technical MIP Template](https://github.com/mars-protocol/mips/blob/main/Technical-MIP-Template.md).

##### Red Bank Asset Listing MIPs

Proposals to add support for one or more new assets within the Red Bank. Proposals should meet the specifications in the [Mars Risk Framework](https://github.com/mars-protocol/mips/blob/main/Mars-Risk-Framework.md) and should be formatted as per the [Red Bank Asset Listing MIP Template](https://github.com/mars-protocol/mips/blob/main/Red-Bank-Asset-Listing-MIP-Template.md).

##### Credit Line Extension MIPs

Proposals from developers aiming to secure a virtual “credit line” from the Red Bank for unique applications such as leveraged yield farming that utilize C2C lending. Proposals should meet the specifications of the [Mars Risk Framework](https://github.com/mars-protocol/mips/blob/main/Mars-Risk-Framework.md) and should be formatted as per the [Credit Line Extension MIP Template](https://github.com/mars-protocol/mips/blob/main/Credit-Line-Extension-MIP-Template.md). 

##### General MIPs

A general category for proposals that do not fall under the above categories. General proposals can be sub-categorized in accordance with their various topics and should be formatted per the [General MIP Template](https://github.com/mars-protocol/mips/blob/main/General-MIP-Template.md).

### The MIP Lifecycle

#### MIP Lifecycle Breakdown

1. **Conception:** A MIP Author posts a MRC proposal on the [Mars Protocol forum](https://forum.marsprotocol.io/) under the appropriate category. From this point on, MIP Editors will be available to assist the MIP Author.
2. **Approved by MIP Editor(s):** A MIP Editor verifies that the posted MRC proposal:
- Follows the appropriate format of the MIP Template for its type.
- Is either an original MIP or a replacement for an older MIP.
- Has been submitted to the [MIP GitHub](https://github.com/mars-protocol/mips) repository with a Pull Request by either the MIP Author or a MIP Editor.
3. **If the verification is successful, the MIP Editor:**
- Approves the MIP and assigns it a formal MIP number.
- Merges in the PR.
- Mars Request for Comments (MRC): A period of reviewing by the community and attendant redrafting begins. The minimum duration of this period is determined by two variables:
    - Feedback Period: 5 days.
    - Frozen Period: 2 days.

Please note that in the case of UI MRCs, there is no need for a Frozen Period.

4. **Fulfilled Feedback Period Requirements:** After the MIP has fulfilled the MRC phase, it is ready for on-chain submission.
5. **On-Chain Submission:** At this point, the MIP Author has two options: submit an on-chain MIP vote referencing the associated MRC and then notify the Mars community on the forum or request help from a MIP Editor to submit the on-chain vote. Proposals can only be submitted via the CLI using the Mars Daemon marsprotocol.io.
6. **Accepted/Rejected:** The MIP is voted on and users may opt for either of the four options i) Yes ii) No iii) Veto iv) Abstain. In the event 33.40% of the votes are for option iii) ‘Veto’, then the proposal is vetoed and the deposit is donated to the community pool. In the event the proposal passes the voting threshold, If it passes, it is officially accepted and is given the Accepted status. If not, the MIP is rejected.

#### On-Chain Submission

The following steps must be completed to submit a proposal on chain and take it to a vote.

[On-chain Submission](./on-chain-submission)

#### Resubmission

A MIP can be resubmitted for an on-chain vote up to 3 times without having to go through phases 1-4 again if it failed to pass due to legitimate external reasons (e.g., potential low governance participation that did not meet the minimum on-chain quorum)

#### Other MIP Statuses

- **Withdrawn:** Assigned when an MIP Author withdraws their MIP proposal.
A MIP may be withdrawn at any point before it enters an on-chain vote. Note that a withdrawn proposal can be taken over from the original Author with a simple transition facilitated by a MIP Editor and the respective parties. If the original MIP Author ceases to be available, a MIP Editor may proceed with the transfer of authorship.
- **Deferred:** Assigned when a proposal has been deemed as not ready or not a priority but can be re-proposed at a later date. This status can be assigned during MRC or by a rejecting forum poll.
- **Obsolete:** Assigned when:
    - A MIP has been superseded or deprecated.
    - A MIP has been deferred for over six months.
    - A MIP Author has abandoned the proposal and no person has communicated willingness to take over the responsibility of an MIP Author.

#### MIP Status Change Process

If a MIP Author requests a status change for a MIP, a MIP Editor will review it. If the status change is warranted, the MIP Editor will change the status. Otherwise, the MIP Editor will revert and highlight issues for the MIP Author to fix before requesting another status change.

### MIP Replacement Process

A MIP can define one or more replacement targets in its preamble. If the MIP is given the Accepted status, the replacement target(s) MIPs receive the Obsolete status and effectively become inactive. The replaced MIP will record the number of the MIP that replaced it. MIPs that depend on the replaced MIP will instead interact with the new MIP.

Since dependencies carry over, a MIP with defined replacement target must strictly adhere to dependency requirements and interface correctly with MIPs that depend on the replaced MIP.

### Supporting Materials

MIPs can optionally refer to external materials. External materials must be added to the [MIPs GitHub](https://github.com/mars-protocol/mips) in the same folder as the MIP which references them.

Externally referenced materials are not MIP content and are not ratified when a MIP becomes Accepted unless it is explicitly stated otherwise in an MIP Component specification.

### MIP Templates

#### Technical MIP Template

- The Technical MIP Template should be used for MIPs for changes to certain configurable aspects of Mars Hub and the Mars Outposts (binding), which can be modified directly by on-chain votes, or code changes to the Mars Protocol (signaling), which require upgrading the protocol.
- The Technical MIP Template is located at https://github.com/mars-protocol/mips/blob/main/Technical-MIP-Template.md.

#### Red Bank Asset Listing MIP Template

- The Red Bank Asset Listing MIP Template should be used for MIPs when proposing support for a new asset that’s not currently supported by the Red Bank.
- All Red Bank Asset Listing MIPs should meet the specifications of the Mars Risk Framework, which is located at https://github.com/mars-protocol/mips/blob/main/Mars-Risk-Framework.md
- The Red Bank Asset Listing MIP Template is located at https://github.com/mars-protocol/mips/blob/main/Red-Bank-Asset-Listing-MIP-Template.md.

#### Credit Line Extension MIP Template

- The Credit Line Extension MIP Template should be used for MIPs when proposing the extension of a credit line for a specific set of smart contracts associated with a Mars Outpost.
- All Credit Line Extension MIPs should meet the specifications of the Credit Line Extension Risk Framework, which is located at https://github.com/mars-protocol/mips/blob/main/Mars-Risk-Framework.md
- The Credit Line Extension MIP Template is located at https://github.com/mars-protocol/mips/blob/main/Credit-Line-Extension-MIP-Template.md.

#### General MIP Template

- The General MIP Template should be used for MIPs whenever a more specific template is not more appropriate.
- The General MIP Template is located at https://github.com/mars-protocol/mips/blob/main/General-MIP-Template.md.

### MIP Editors

The MIP Framework depends on MIP Editors.

#### MIP Editor

MIP Editors enforce the administrative and editorial aspects of the overall MIPs process and program.

**Specific authority of the MIP Editor(s) in MIP0 processes**

- MIP Editors control phase 2 of the MIP lifecycle and can assign MIP numbers.
- MIP Editors are admins on the [MIPs GitHub repository](https://github.com/mars-protocol/mips).
- MIP Editors moderate the relevant MRCs categories in the forum.
- MIP Editors are responsible for updating the status of MIPs.

#### Editor Responsibilities

A MIP Editor’s responsibilities include:

- Providing feedback in the MIP sections of the [Mars Forum](https://forum.marsprotocol.io/).
- Assign formal number labels to MIPs.
- Make sure that titles, MIP statuses, category placements all track the actual MIPs.
- Confirm there is a (real) dedicated MIP author, coordinator, funder and/or sponsor, etc.
- Correspond with MIP authors/coordinators.
- Review MIPs for obvious defects in the language.
- Make sure that MIPs follow the style guide (template).
- Work and communicate with MIP authors to help them submit an MRC for on-chain voting as a MIP.

MIP Editors can correct issues themselves, but they are not required to.

**Disclaimers/Disclosures**

This proposal is being made by Delphi Labs Ltd., a British Virgin Islands limited company. Delphi Labs engages in incubation, investment, research and development relevant to multiple ecosystems and protocols, including the Mars Protocol. Delphi Labs and certain of its service providers and equity holders own MARS tokens and have financial interests related to this proposal. Additionally, Delphi Labs is one of several entities associated with one another under the “Delphi Digital” brand. Delphi Digital’s associated entities and/or equityholders or service providers of such entities may hold MARS and may have financial interests related to this proposal. All such entities, service providers, equity holders and other related persons may also have financial interests in complementary or competing projects or ecosystems, entities or tokens, including Osmosis/OSMO. These statements are intended to disclose relevant facts and to help identify potential conflicts of interest, and should not be misconstrued as a complete description of all relevant interests or conflicts of interests; nor should they be construed as a recommendation to purchase or acquire any token or other asset..

This proposal is also subject to and qualified by the [Mars Disclaimers/Disclosures](https://mars-protocol.medium.com/mars-disclaimers-disclosures-f44cc7c54a33). Delphi Labs may lack access to all relevant facts or may have failed to give appropriate weighting to available facts. Delphi Labs is not making any representation, warranty or guarantee regarding the accuracy or completeness of the statements herein, and Delphi Labs shall have no liability in the event of losses or damages ensuing from approval or rejection or other handling of the proposal. Each user and voter should undertake their own research and make their own independent interpretation and analysis of all relevant facts and issues to arrive at their own personal determinations of how to vote on the proposal.

## Copyright

Copyright and related rights waived via [CC0 1](https://creativecommons.org/publicdomain/zero/1.0/).






















