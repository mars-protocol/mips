# MIP-3: Enable IBC on Mars Hub

## Proposal Authors

Delphi Labs

## Summary

This proposal aims to get community approval to enable IBC on Mars Hub.

## Abstract

This proposal seeks to get approval to enable the use of IBC on Mars Hub.

## Motivation

Mars Hub’s mainnet from its launch can be seen to have IBC disabled. This doesn’t permit Mars Hub and its users to benefit from being able to transfer assets from one chain to another, nor does it allow Mars Hub to transfer protocol revenues from its outposts, as detailed in the Whitepaper 3.

## Specification

No additional development is required to enable IBC on Mars Hub. All that is required is the change of a flag from False to True

## Risks

The use of IBC is now considered standard practice within the Cosmos ecosystem. Given that no amendments to the SDK will be made as it pertains to IBC, we don’t foresee significant technical risks associated with enabling IBC. Enabling IBC facilitates moving value from Mars Hub to other chains, which could affect the future usage levels, value or security of Hars Hub, but Mars validator/staking rewards should be sufficient to maintain sufficient value and activity on Mars Hub.

## Implementation

This proposal is considered to be binding and enforced upon this proposal being successfully passed, as it requires only on-chain infrastructure and can be implemented automatically upon the voting period elapsing.

A change to the transfer.proto configuration file must be made to changing ibc-transfer module’s send_enabled and receive_enabled parameter from False to True.

## Disclaimers/Disclosures

This proposal is being made by Delphi Labs Ltd., a British Virgin Islands limited company. Delphi Labs engages in incubation, investment, research and development relevant to multiple ecosystems and protocols, including the Mars Protocol. Delphi Labs and certain of its service providers and equity holders own MARS tokens and have financial interests related to this proposal. Additionally, Delphi Labs is one of several entities associated with one another under the “Delphi Digital” brand. Delphi Digital’s associated entities and/or equityholders or service providers of such entities may hold MARS and may have financial interests related to this proposal. All such entities, service providers, equity holders and other related persons may also have financial interests in complementary or competing projects or ecosystems, entities or tokens, including Osmosis/OSMO. These statements are intended to disclose relevant facts and to help identify potential conflicts of interest, and should not be misconstrued as a complete description of all relevant interests or conflicts of interests; nor should they be construed as a recommendation to purchase or acquire any token or security.

This proposal is also subject to and qualified by the Mars Disclaimers/Disclosures. Delphi Labs may lack access to all relevant facts or may have failed to give appropriate weighting to available facts. Delphi Labs is not making any representation, warranty or guarantee regarding the accuracy or completeness of the statements herein, and Delphi Labs shall have no liability in the event of losses or damages ensuing from approval or rejection or other handling of the proposal. Each user and voter should undertake their own research and make their own independent interpretation and analysis of all relevant facts and issues to arrive at their own personal determinations of how to vote on the proposal.