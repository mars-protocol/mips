**Red Bank Asset Listing MIP Template**

**Red Bank Asset Listing MIP Template**

**Preamble**

> MIP#: <# to be assigned>
> 
> 
> Title: <MIP title>
> 
> Author(s): <list of authors' names and/or email addresses and GitHub handles>
> 
> Contributors: <list of contributors’ names and/or email addresses and GitHub handles>
> 
> Tags: <Ticker of asset to be listed>
> 
> Type: MIP Type (Red Bank Asset Listing MIP)
> 
> Category: Binding (Executable Purely On-Chain) vs. Signaling (Non-Binding Social Consensus Signal)
> 
> Status: <Assigned by MIP Editor>
> 
> Date Proposed: <yyyy-mm-dd>
> 
> Date Ratified: <yyyy-mm-dd>
> 
> Dependencies: <List of dependent MIPs if applicable>
> 
> Replaces: <List of MIP it is replacing if applicable>
> 

**References**

- A list of supporting materials referenced by this MIP.

**Summary**

- A short description of the asset to be added to the Red Bank and the reasoning behind adding it. Suggest 30 words max.

**Abstract**

- A 2-4 sentence description of the full MIP going through the benefits of adding the asset and who will and how it will be implemented.

**Motivation**

- A short description of the motivation behind the MIP.

**New Asset Information**

- Project website.
- Whitepaper.
- Project documentation.
- Communities.

**New Asset Market Risk**

The following metrics, as defined in the [Red Bank Asset Listing Risk Framework](https://github.com/mars-protocol/mips/Red-Bank-Asset-Listing-Framework.md):

- Maximum intraday drawdown.
- Volatility.
- 24hr volume.
- Worst 7-day volume.

**New Asset Technical Risk**

Links to the following:

- Audits.
- GitHub page where source code is hosted.
- Must contain unit tests and integration tests.
- On-chain contracts.
- The hash of the contract binary must match the code on GitHub.

The following metrics, as defined in the [Red Bank Asset Listing Risk Framework](https://github.com/mars-protocol/mips/Red-Bank-Asset-Listing-Framework.md):

- Time since launch.
- Honey pot.

**Centralization Risk**

- Smart contracts upgradability: How is the SC upgradable? Is it immutable, DAO upgradable or controlled by a multisig? If it’s a multisig, what does it control and who are the signers? Is there a timelock in place?
- Team: Who is the team behind the project? What’s their technical and crypto expertise? Have they built something in addition to this project?
- What is the proposed oracle for the new asset?

**Risk Parameters Suggestion**

The information provided in the risk sections above should be used to score the asset and provide suggestions for its associated risk parameters, following the methodology provided in the [Red Bank Asset Listing Risk Framework](https://github.com/mars-protocol/mips/Red-Bank-Asset-Listing-Framework.md). These risk parameters are the following:

- Loan-to-Value
- Liquidation Threshold
- Liquidation Bonus
- Optimal Utilization
- Interest Rate Parameters
- Whether the asset will be usable as collateral

**Poll**

- The MRC should contain a link to a pre-existing poll to gather community sentiment for the MRC.

**Implementation**

- Describes how the MIP can be implemented or if it was already implemented, how it was done.

**Technical Instructions for Submitting a new asset listing proposal**

To submit a proposal a send call needs to be done to the MARS token, sending at least the proposal_required_deposit amount stored (as uMARS or 10 ^ -6 MARS) in config. The msg attribute should contain the submit_proposal receive msg as detailed in the schema.

Note that fields with the “Binary” type (example, msg attribute for a WasmMsg “execute”) need to be base64 encoded.

The proposal messages attribute should contain two WasmMsg “execute” calls in any order:

> init_asset call to the red bank with the parameters for how the asset will behave (see schema).
> 
> 
> set_asset call to the oracle with the parameters of how the price will be retrieved (see [schema](https://github.com/mars-protocol/mars-core/blob/4b877ae4bf352a42fd1d1506f054cce0cc824da3/contracts/mars-oracle/schema/execute_msg.json#L30)).
> 

**Licensing**

- Recommended licenses for developed code:
    - MIT: Expat/MIT/X11 license
    - BSD-2-Clause: OSI-approved BSD 2-clause license
    - BSD-3-Clause: OSI-approved BSD 3-clause license
    - CC0-1.0: Creative Commons CC0 1.0 Universal
    - GNU-All-Permissive: GNU All-Permissive License
    - Apache-2.0: Apache License, version 2.0