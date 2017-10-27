# <h3 style="text-align: center;" markdown="1">Giveth Technical White Paper<h3>

<p style="text-align: center;" markdown="1">(Assumes basic knowledge of Ethereum)</p>

The purpose of our technology is to give Cryptocurrency users the ability to donate effortlessly to Campaigns focused on making the world a better place. They can use the Giveth platform to find those Campaigns and donate directly or they can pledge their ether to a cause and have a Delegate choose for them. As an alternative to traditional donation systems, our Liquid Pledging contract allows Givers to take back their pledge if they disagree with how their donations were allocated, or for whatever reason, as long before it has been locked in to a Campaign, for a specific purpose.

To make this new way of giving possible, we have to overcome a few challenges.

The 1st challenge is how to securely offer a means for Givers to donate without losing ownership of their funds. The 2nd challenge is how to allow third parties to distribute these owned ether donations to individuals who can use them effectively. Lastly, how do we securely transfer ownership to the individuals who are making the world a better place.

However, baked into that 3rd challenge, there is a 4th challenge of how to determine whether ownership of distributed ether should be transferred or not. In other words, how can we be sure a recipient deserves the donated ether before we transfer it?

For clarity, the 4 challenges are briefly restated here:

1. Safely donate ether without losing ownership
2. Allocate donated funds to individuals who can use it for good
3. Safely transfer ownership of ether to said individuals
4. Determine whether ownership should be transferred

#### Safely donate ether without losing ownership
Challenge #1 is handled by our [vault](https://github.com/Giveth/vaultcontract) contract. This is a solidity smart contract that can safely store ether on behalf of the ether’s owner. This is how and why a giver may control or take back their donations. When a giver donates ether through Giveth, it is actually stored in a vault with them as the owner.

Once stored, ether is stuck and cannot be moved without the owners permission.

#### Allocate donated funds to individuals who can use it for good
Challenge #2 is partly handled by our [minime](https://github.com/Giveth/minime) contract. This is a solidity smart contract that can represent ether with tokens.

Instead of transferring actual ether to individuals for their efforts to do good, we can distribute minime tokens with the assurance that the real ether is stored in the vault. Minime tokens are used by a number of big projects in the the ethereum space.

Our latest dapp uses another strategy for flexible transfers. [Liquid pledging](https://github.com/Giveth/liquidpledging) is our solidity smart contract that allows us to redistribute ether in a myriad of networked permutations (aka a graph). It's a bit like liquid democracy, but there is no voting (unless you add that as a plugin).

At it's core, liquid pledging maintains a list of ether transfers and owners. These two lists serve as the data structure for the graph. The contract's api provides the means to donate, delegate, and transfer ether stored in the vault. Its other major innovation is "contract plugins."

#### Safely transfer ownership of ether to said individuals
Challenge #3 is again resolved by our [vault](https://github.com/Giveth/vaultcontract) contract. Ether is only ever released to addresses whitelisted with original donors permission. However, in order to fully meet the requirements of challenge #3, we must set some sort of approval process.

#### Determine whether ownership should be transferred
The rules for how transfers are approved, challenge #4, are handled by liquid pledging plugins (lpp). These plugins are separate contracts reference by the liquid pledging contract (see challenge #2).

For example, you could use our [lpp-milestone](https://github.com/Giveth/lpp-milestone) plugin to require reviewer approval as a condition to releasing ether from its original donor. In this case, the reviewer is another ethereum address. If "acceptMilestone" is called from this approved reviewer address, then the ownership of donated ether can be released to the milestone recipient address.

You don’t have to use our lpp-milestone plugin. You can make your own with whatever you want. Use a contract that mandates the rules you need for your community.

This concludes the Giveth Technical White Paper for now. Reach out to us on [Slack](https://github.com/Giveth/vaultcontract) if you have something you want to do with the ideas listed. We are an opensource project and it's our mission to help communities.
