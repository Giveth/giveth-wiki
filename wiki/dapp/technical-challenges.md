# <h3 style="text-align: center;" markdown="1">DApp Technical Challenges<h3>

<p style="text-align: center;" markdown="1">(Assumes basic knowledge of Ethereum)</p>

The purpose of our technology is to give Cryptocurrency users the ability to donate effortlessly to Campaigns focused on making the world a better place. They can use the Giveth platform to find those Campaigns and donate directly or they can pledge their Ether to a cause and have a Delegate choose an appropriate Campaign or Milestone for them. As an alternative to traditional donation systems, our Liquid Pledging contract allows Givers to take back their pledge if they disagree with how their donations were allocated, or for whatever other reason, before it has been locked in to a Campaign for a specific purpose.

To make this new way of giving possible, we have to overcome a few challenges:

1. How do we offer a means for Givers to donate without losing ownership of their funds.
2. How do we allow third parties to distribute these Ether donations to individuals who can use them effectively.
3. How do we securely transfer ownership to the individuals who are making the world a better place.
4. How to determine whether ownership of distributed Ether should be transferred or not. In other words: How can we be sure a recipient deserves the donated Ether before we transfer it?

#### Donate without losing ownership
Challenge #1 is handled by our [vault](https://github.com/Giveth/vaultcontract) contract. This is a solidity smart contract that can safely store Ether on behalf of the Ether’s owner. This is how and why a Giver may control or take back their donations. When a giver donates Ether through Giveth, the coins are actually stored in a vault with the Giver as the owner.

Once stored in the Vault, the Ether gets stuck and cannot be moved further without the owners permission.

#### Distribute collected funds
Challenge #2 is partly handled by our [Minime](https://github.com/Giveth/minime) contract. This is a solidity smart contract that can represent Ether with tokens.

Instead of transferring actual Ether to individuals for their efforts to do good, we can distribute Minime tokens with the assurance that the real Ether is stored in the vault. Minime tokens are used by a number of well-known projects in the Ethereum space.

Our latest DApp uses another strategy for flexible transfers. [Liquid pledging](https://github.com/Giveth/liquidpledging) is a solidity smart contract that allows us to redistribute Ether in a myriad of networked permutations (aka a graph). It's a bit like liquid democracy, but there is no voting (unless you add that as a plugin).

At its core, liquid-pledging maintains a list of Ether transfers and owners. These two lists serve as the data structure for the graph. The contract's API provides the means to donate, delegate, and transfer Ether stored in the Vault. Its other major innovation is 'contract plugins'.

#### Transfer ownership
Challenge #3 is again resolved by our [vault](https://github.com/Giveth/vaultcontract) contract. Ether is only ever released to addresses whitelisted with the permission of the original donor. However, in order to fully meet the requirements of challenge #3, we must set some sort of approval process.

#### Determine if should transfer
The rules for how transfers are approved (challenge #4), are handled by liquid-pledging plugins (lpp). These plugins are separate contracts reference by the liquid pledging contract (see challenge #2).

For example, you could use our [lpp-milestone](https://github.com/Giveth/lpp-milestone) plugin to require reviewer approval as a condition to releasing Ether from its original donor. In this case, the reviewer is another Ethereum address. If 'acceptMilestone' is called from this approved reviewer address, then the ownership of donated Ether can be released to the Milestone recipient address.

You don’t have to use our lpp-milestone plugin. You can make your own with whatever you want. Use a contract that mandates the rules you need for your community.

This concludes the Giveth Technical White Paper for now. Reach out to us on [Riot](http://riot.giveth.io) if you have something you want to do with the ideas listed. We are an open-source project and it is our mission to help communities.
