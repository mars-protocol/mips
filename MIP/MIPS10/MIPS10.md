# MIPS-10:  Red Bank deposit caps increase 1

## Description

- Authored by Delphi Labs
- Forum discussion: [link](https://forum.marsprotocol.io/t/mrc-10-red-bank-deposit-caps-increase-1/799) 

## Summary

This proposal aims to increase the Red Bank deposit caps for OSMO, ATOM, and axlUSDC to 10.0M, 350k, and 1.5M, respectively.

## Abstract

Proposal to increase the Red Bank deposit caps for OSMO, ATOM, and axlUSDC to 10.0M, 350k, and 1.5M, respectively. This proposal outlines the underlying motivations and the risks considered that are associated with this action.

## Motivation

Mars Hub and Red Bank have now been launched, initial deposit caps have been hit and the infrastructure deployed is working as intended. As such it is time to increase the deposit caps on Red Bank.

## Specification

We propose the following increases from the current deposit caps for all three assets listed on Red Bank.

| | Current caps on Red Bank | Proposed caps on Red Bank | | ------- | ------------------------ | ------------------------- | | OSMO | 2.5M | 10M | | ATOM | 100k | 350k | | axlUSDC | 500k | 1.5M |

## Risks

The dominant risk associated with this action is that an increase in the caps for a given asset can result in an over-exposure to said asset. Capping exposure allows Mars to reduce risk associated with asset price manipulation, extreme price volatility, and abnormally high swapping fees (lack of liquidity), among others. These issues could be detrimental to Red Bank in terms of insolvencies and liquidations.

## Implementation

This proposal is considered to be "signaling intent" upon successfully being passed, and will require off-chain infrastructure and human resources to implement.

In the event this proposal passes, the Builder Multisig on the Osmosis chain, which is the current owner of the smart contracts deployed, will be utilised. This multisig will dispatch the appropriate smart contract messages that set the new deposit caps at Red Bank such that they are consistent with this proposal.

## Disclaimers / Disclosures

This proposal is being made by Delphi Labs Ltd., a British Virgin Islands limited company. Delphi Labs engages in incubation, investment, research and development relevant to multiple ecosystems and protocols, including the Mars Protocol. Delphi Labs and certain of its service providers and equity holders own MARS tokens and have financial interests related to this proposal. Additionally, Delphi Labs is one of several entities associated with one another under the "Delphi Digital" brand. Delphi Digital's associated entities and/or equity holders or service providers of such entities may hold MARS and may have financial interests related to this proposal. All such entities, service providers, equity holders, and other related persons may also have financial interests in complementary or competing projects or ecosystems, entities or tokens, including Osmosis/OSMO. These statements are intended to disclose relevant facts and to help identify potential conflicts of interest, and should not be misconstrued as a complete description of all relevant interests or conflicts of interests; nor should they be construed as a recommendation to purchase or acquire any token or security.

This proposal is also subject to and qualified by the Mars Disclaimers / Disclosures. Delphi Labs may lack access to all relevant facts or may have failed to give appropriate weighting to available facts. Delphi Labs is not making any representation, warranty, or guarantee regarding the accuracy or completeness of the statements herein, and Delphi Labs shall have no liability in the event of losses or damages ensuing from approval or rejection or other handling of the proposal. Each user and voter should undertake their own research and make their own independent interpretation and analysis of all relevant facts and issues to arrive at their own personal determinations of how to vote on the proposal.