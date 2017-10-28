# Giveth Deployments

## Giveth Fund Forwarder

@quazia and @griff developed a quick fix to prevent the loss of tokens donated to Giveth.

The source code for the FundForwarder can be found [here](https://github.com/Giveth/fund-forwarder/blob/master/contracts/FundForwarder.sol)

It requires 3 constructor parameters, which for our purposes are set as:

`_beneficiary` = 0x8702b8D7a1EeFEc7E54636E26A9323Dc96A8Dc25 (The current Giveth campaign address)
`_escapeHatchCaller` = 0x839395e20bbB182fa440d08F850E6c7A8f6F0780 [(Griff's Address)](https://twitter.com/thegrifft/status/755401659606528005)
`_escapeHatchDestination` = 0x8f951903c9360345b4e1b536c7f5ae8f88a64e79 (The Giveth Multisig)

More will be added upon the deployment
