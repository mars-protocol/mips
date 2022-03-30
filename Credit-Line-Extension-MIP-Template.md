# Credit Line Extension MIP Template

## Preamble

    MIP#: <# to be assigned>
    Title: <MIP title>
    Author(s): <list of authors' names and/or email addresses and GitHub handles>
    Contributors: <list of contributors’ names and/or email addresses and GitHub handles>
    Tags: <Name of protocol or project seeking a credit line>
    Type: MIP Type (Credit Line Extension MIP)
    Category: Binding (Executable Purely On-Chain) vs. Signaling (Non-Binding Social Consensus Signal)
    Status: <Assigned by MIP Editor>
    Date Proposed: <yyyy-mm-dd>
    Date Ratified: <yyyy-mm-dd>
    Dependencies: <List of dependent MIPs if applicable>
    Replaces: <List of MIP it is replacing if applicable>

## References

- A list of supporting materials referenced by this MIP.

## Summary

- A short description of how the credit line extension will be used. Suggest 30 words max.

## Abstract

- A 2-4 sentence description of the full MIP going through the use case for the credit line and who will and how it will be implemented.

## Motivation

- A short description of the motivation behind the MIP.

## Basic Information

For the Base SC, the other SCs and the assets the strategy interacts with, links to the following:

- Project website.
- Whitepaper.
- Project documentation.
- Communities.

## Technical Risk

For the Base SC, the other SCs and the assets the strategy interacts with, links to the following:

- Audits.
- GitHub page where source code is hosted.
    - Must contain unit tests and integration tests.
- On-chain contract.
    - The hash of the contract binary must match the code on GitHub.
- Testnet contract (only applies for Base SC).

## Centralization Risk

For the Base SC:

- SC upgradability: How is the SC upgradable? Is it immutable, DAO upgradable or controlled by a multisig? If it’s a multisig, what does it control and who are the signers?
- Is the SC always in control of the borrowed assets?
- Is there an emergency trigger that would allow strategy assets to be unstaked from the protocol they’re ultimately staked in?
- What oracle is used for the strategy?

For the other SCs and assets the Base SC interacts with:

- SC upgradability: How is the SC upgradable? Is it immutable, DAO upgradable or controlled by a multisig? If it’s a multisig, what does it control and who are the signers? Is there a timelock in place?

## Risk Parameters Suggestion

For each parameter suggestion, all relevant information used to determine that parameter should be provided, following the methodology described in the [Credit Line Extension Risk Framework](https://github.com/mars-protocol/mips/Credit-Line-Extension-Risk-Framework.md). The suggested parameters should be:

- Maximum Leverage
- Liquidation Threshold
- Liquidation Bonus
- Requested Credit Line Size
- Minimum Position Size
- TWAP Oracle Implementation (if TWAP is used for the strategy)

## Poll

- The MRC should contain a link to a pre-existing poll to gather community sentiment for the MRC.

## Implementation

- Describes how the MIP can be implemented or if it was already implemented, how it was done.

## Technical Instructions for Submitting a Credit Line Extension Proposal

To submit a proposal a send call needs to be done to the MARS token, sending at least the proposal_required_deposit amount stored (as uMARS or 10 ^ -6 MARS) in config. The msg attribute should contain the submit_proposal receive msg as detailed in the schema.

Note that fields with the “Binary” type (example, msg attribute for a WasmMsg “execute”) need to be base64 encoded.

The proposal messages attribute should contain a single WasmMsg “execute” call:

    'update_uncollateralized_loan_limit' call with the address of the receiver of the credit and the corresponding limit (see schema). ​

## Licensing

- Recommended licenses for developed code:
    - MIT: Expat/MIT/X11 license
    - BSD-2-Clause: OSI-approved BSD 2-clause license
    - BSD-3-Clause: OSI-approved BSD 3-clause license
    - CC0-1.0: Creative Commons CC0 1.0 Universal
    - GNU-All-Permissive: GNU All-Permissive License
    - Apache-2.0: Apache License, version 2.0