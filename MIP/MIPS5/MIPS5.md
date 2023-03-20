# MIP-5: Increase validator set size to 75

## Description

- Authored by @traianoverse
- Forum discussion: [link](https://forum.marsprotocol.io/t/mrc-5-increase-validator-set-to-75/754)

## Summary

This proposal is to increase the number of active validators from 50 to 75.

## Abstract

This will provide opportunities for smaller or new validators to get on board and gain support from the community. The Hub has the authority to manage its Outposts and it is crucial for the growth of Mars to have a higher number of active validators who are committed to educating the community and being active participants.

## Motivation

The launch of Mars Hub has been stable and incident-free and we feel that the purpose of having a limited and partial genesis set has accomplished its objectives.

Keeping this path could lead to centralized voting power among those who started validating Mars Hub in its early days.

## Risks

As with all validator expansions, it is possible that expanding the set could have a small effect on the overall block times taking longer, as more validators are required to achieve consensus.

## Implementation

If this proposal is passed, the following parameter change will be executed on-chain:

```json
[
  {
    "subspace": "staking",
    "key": "MaxValidators",
    "value": "75"
  }
]
```