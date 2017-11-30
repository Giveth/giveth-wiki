# Giveth Deployments

## Giveth Fund Forwarder - 0x5ADF43DD006c6C36506e2b2DFA352E60002d22Dc

@quazia and @griff developed a quick fix to prevent the loss of tokens donated to Giveth.

The source code for the FundForwarder can be found [here](https://github.com/Giveth/fund-forwarder/blob/master/contracts/FundForwarder.sol)

It's ABI and source code can also be found on [etherscan](https://etherscan.io/address/0x5ADF43DD006c6C36506e2b2DFA352E60002d22Dc#code)

It had 3 constructor parameters, which for our purposes are set as:

`_beneficiary` = 0x8702b8D7a1EeFEc7E54636E26A9323Dc96A8Dc25 (The current Giveth campaign address)

`_escapeHatchCaller` = 0x839395e20bbB182fa440d08F850E6c7A8f6F0780 [(Griff's Address)](https://twitter.com/thegrifft/status/755401659606528005)

`_escapeHatchDestination` = 0x8f951903c9360345b4e1b536c7f5ae8f88a64e79 (The Giveth Multisig)



## MyEtherWallet's Giveth Campaign

MyEtherWallet is one of Giveth's biggest supporters and has volunteered to be our first Public Alpha Tester for the Giveth Platform.

### Donation Flow

Donor donates -> Campaign (MYD sent to Donor) -> Vault 

The Main Donation address is the Campaign contract which catches tokens and issues MYD tokens, then sends the ether to the vault. 


### Contracts Deployed


Token Factory: 0x63a5aeb18c893943b6bc72f013f6c4c545182854

Campaign/Token Controller: 0x809Af635bb8f1541EAe4Ecd00351c08700B5b476

MYD Token Contract: 0xa5a8ab2c69c27169a93fb52b8d52072ca61a4cdc

Vault: 0x598ab825d607ace3b00d8714c0a141c7ae2e6822 

MilestoneTracker: [Not yet Deployed]


### Required Set Up Parameters

#### Token Factory 


Allows you to clone the token to upgrade the token, create a vote, offer ICO access, basically give anyone that has this token the ability to do something special… this is permissionless too ;-) anyone can do this :-D


#### Campaign, Token Controller! 


1.  escapeDestination    0x97B47fE3Ed8d68Ee4b930b27598d08097F8eA9C6
2.  escapeCaller    0xDdA882a62600C452419145781e45052fdC06382C
3.  owner    0xDdA882a62600C452419145781e45052fdC06382C
4.  maximumFunding    10000000000000000000000 (Can only collect 1,000,000 ETH!!! MUST BE CHANGED IN THE CODE) 
5.  startFundingTime    1484933219 (the past)
6.  totalCollected    46741000000000000000  (Current balance: 46.741 ETH, 9953.259 to go)
7.  endFundingTime    1742699619 (some time in distant future)

This contract creates MYD and sends it to the Giver  

Special complications

Owner: Will start off as Quazia

Old Campaign will send 46.741 ETH  to new campaign

To keep tokens and total collected consistent, we will destroy the tokens created in step 2

We do a bunch of testing :-D

Owner will be changed to 0xDdA882a62600C452419145781e45052fdC06382C 


#### MYD token Contract

Parent Token: 0xf7e983781609012307f2514f63d526d83d24f466

1.  name    MyEtherWallet Donations Token 
2.  decimals    18
3.  symbol    MYD 
4.  transfersEnabled    NO
5.  controller    Address of the campaign 



#### Vault

1.  maxSecurityGuardDelay    1209600 The amount of time the security guard can delay a payment
3.  owner    0xDdA882a62600C452419145781e45052fdC06382C 
5.  securityGuard    0x839395e20bbb182fa440d08f850e6c7a8f6f0780 (Griff)
6.  escapeDestination    0x97B47fE3Ed8d68Ee4b930b27598d08097F8eA9C6
7.  timeLock    86400 (1 day delayed payment)
9.  absoluteMinTimeLock    3600 (1 hour minimum delay that can be set)
10.  escapeCaller    0xDdA882a62600C452419145781e45052fdC06382C

After the milestoneTracker is deployed, we will add it to the `allowedSpender[]` whitelist; this will need to be handled by owner

#### MilestoneTracker 
4.  donor    0xb8Bed6a570cA87d03E4E386f27D14822179d10f9
5.  recipient    0x839395e20bbb182fa440d08f850e6c7a8f6f0780 
6.  arbitrator    0xDdA882a62600C452419145781e45052fdC06382C 


