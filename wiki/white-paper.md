<h3 style="text-align: center;" markdown="1">Giveth Technical White Paper<h3>

<p style="text-align: center;" markdown="1">(Assumes basic knowledge of ethereum)</p>

The purpose of our technology is to enable ethereum holders to donate ether without losing ownership. As an alternative to traditional donation, our smart contracts allow givers to take back their ether if they disagree with how their donations were allocated. Or, if they just feel like it.

To make this new way of giving possible, we have to overcome a few challenges.

The 1st challenge is how to securely offer a means for givers to donate without losing ownership of their funds.

The 2nd challenge is how to allow third parties to distribute these owned ether donations to individuals who can use them effectively.

Lastly, how do we securely transfer ownership to the individuals who are making the world a better place.

But baked into challenge #3, there is a 4th challenge of how to determine whether ownership of distributed ether should be transferred or not. In other words, how can we be sure a giver deserves the donated ether before we transfer it.

For clarity, the 4 challenges are briefly restated here:
1. Safely give ether without losing ownership
2. Allocate donated funds to individuals
3. Safely transfer ownership of ether to said individuals
4. Determine whether ownership should be transferred

Challenge #1, "Safely give ether without losing ownership," is handled by our [vault](https://github.com/Giveth/vaultcontract) contract. This is a solidity smart contract that can safely store ether on behalf of the ether’s owner. This is how and why a giver may control or take back their donations. When a giver donates ether through Giveth, it is actually stored in a vault with them as the owner.

Once stored, ether is stuck and cannot be moved without the owners permission.

Challenge #2, "Allocate donated funds to individuals," is partly handled by our [minime](https://github.com/Giveth/minime) contract. This is a solidity smart contract that can represent ether with tokens.

Instead of transferring actual ether to individuals for their efforts to do good, we can distribute minime tokens with the assurance that the real ether is stored in the vault.

This combined power of safe (vault) and flexible (minime) transfers allows us to redistribute ether in a myriad of networked permutations (aka a graph). Which is where [liquid pledging](https://github.com/Giveth/liquidpledging) comes into play.

Liquid pledging is our solidity smart contract that allocates donated ether in a representative fashion. It's a bit like liquid democracy, but there is no voting (unless you add that as a plugin).

At it's core, liquid pledging maintains a list of ether transfers and list of owners. These two lists serve as the data structure for the graph. The contract's api provides the means to donate, delegate, and transfer ether from the vault.

Challenge #3, "Safely transfer ownership of ether to said individuals," is again resolved by our vault contract. Ether is only ever released to addresses whitelisted with original donors permission. However, in order to fully meet the requirements of challenge #3, we must set some sort of approval process.

The rules for how transfers are approved, challenge #4, are handled by liquid pledging plugins (lpp). These plugins are separate contracts reference by the liquid pledging contract mentioned above.

For example, you could use our [lpp-milestone](https://github.com/Giveth/lpp-milestone) plugin to require reviewer approval as a condition to releasing ether from it's original donor. In this case, the reviewer is another ethereum address. If "acceptMilestone" is called from this approved reviewer address, then the ownership of donated ether can be released to the milestone recipient address.

But you don’t have to use our lpp-milestone plugin, you can make your own with whatever you want. Use a contract that mandates the rules you need for your community.

This concludes the Giveth Technical White Paper for now. Reach out to us on [Slack](https://github.com/Giveth/vaultcontract) if you have something you want to do with the ideas listed. We are an opensource project and it's our mission to help communities.
