# MIP-6: Lower minimum proposal deposit amount to 5,000 MARS

## Description

- Authored by @traianoverse
- Forum discussion: [link](https://forum.marsprotocol.io/t/mrc-6-lower-minimum-proposal-deposit-amount/760)

## Summary

The current deposit amount of 100,000 MARS prohibits valuable governance activity from small holders. We propose lowering the requirement to 5,000 MARS.

## Abstract

The current deposit requirement is 100,000 MARS, which roughly translates to $50,000 in USD as of today. We propose a deposit amount of 5,000 MARS (approximately $2,500 USD). This initial deposit amount was deemed necessary due to the fact that, at the time of launch, MARS had no value. A lower deposit amount could have facilitated the submission of spam proposals during the early stages of the network's development before its core principles were established.

## Motivation

Now that MARS has been listed and found a price, we feel comfortable in asking to lower the deposit amount as it could:

Enable community members with good ideas but little capital to participate in governance and request resources from the community pool treasury

Improve the governance UX for holders who keep most of their MARS staked or in DeFi activities (providing liquidity, trading activity, etc.)

Increase utilization of treasury (64% of the total supply is allocated to the community pool)

Accelerate Mars Hub development and growth (as for the vision of Mars' Whitepaper, the objective it's to deploy outposts across several blockchains, this will require active participation from the community)

## Risks

This change makes it easier to submit spam proposals.

## Implementation

If this proposal is passed, the following parameter change will be executed on-chain:

```json
[
  {
    "subspace": "gov",
    "key": "depositparams",
    "value": "{\"min_deposit\":[{\"denom\":\"umars\",\"amount\":\"5000000000\"}]}"
  }
]
```