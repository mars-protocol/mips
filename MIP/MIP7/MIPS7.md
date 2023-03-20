# MIPS-7: Declare unsecure validator-as-a-service (VaaS) as unwelcome

## Description

- Authored by Jacob Gadikian (@gadikian), larry.stars (@larry0x), and _gabrielShapir0 (@lex_node) with helpful inputs from PFC (@PFC_Validator) and PUPMØS (@pupmos)
- Forum discussion: [link](https://forum.marsprotocol.io/t/mrc-7-declare-unsecure-validator-as-a-service-vaas-as-unwelcome/762)

This proposal aims to seek the community's agreement that entities providing validator-as-a-service (VaaS) with unsecure practices and their customers (a.k.a. "white label" validators) are unwelcome on Mars Hub.

## Context

For the purpose of this proposal, we focus on the following unsecure practice: the VaaS provider, rather than assisting the customer (i.e. the validator) with their own secure key generation and management, generates key(s) on the customer's behalf, or else requires the customer to share the key(s) after they are generated.

**While white label validators take a full share of the staking reward in the same way as other validators do, they do not provide the same level of security; rather, they obscure the network's true level of security.** Two vital properties of a blockchain, namely liveness and censorship resistance, rely on blocks being proposed and validated by many independent actors located in diverse geographical locations and jurisdictions. The inclusion of white label validators into the active set obscures the levels of these properties, because what may appear as multiple independent validators can potentially have their keys held by a single entity (i.e. the VaaS provider).

**In fact, they may reduce the security if non-white label validators are forced out of the active set.** In the case that a single VaaS provider controls a large percentage of the network's consensus voting power (as is the case for the LUNC chain, for example), this provider may have the ability to severely undermine the network's security by forcing a chain halt (which requires 1/3 of total voting power) or forging fraudulent blocks (requires 2/3).

Despite some VaaS providers claim they have deleted the keys shared with them by their customers, there is no credible evidence that they have indeed done so. While it is easy for someone to prove they possess a certain key (simply by producing a signature with the key), it is extremely difficult, if possible at all, to prove that they do NOT possess a key. **Once a key has been known by any party other than the validator themself, it should be considered permanently compromised.**

## Motion

We suggest that the community approve the following signaling proposal:

- Validators with a compromised (as defined above) operator key AND/OR consensus key (whether due to key generation by a VaaS, key sharing with a VaaS, or otherwise), are not welcome on Mars Hub;
- VaaS providers must publish strong evidence of secure key practices that do not leave their customers with compromised keys AT ANY POINT, otherwise they are not welcome to operate their VaaS business or operate as a validator on Mars Hub;
- The community asks that any validators with compromised keys withdraw from the active set, and that their VaaS providers cease providing the VaaS in this unsecure manner.

Note that this proposal does not indicate any enforceable action against VaaS providers or their customers, which may be decided in a separate proposal if the community deems it necessary.