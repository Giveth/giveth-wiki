# Glossary

This page tries to explain some of the terms commonly used within the Giveth system.

## <a name="glossary-campaign"></a>Campaign
Campaign is a minimal entity that allowing [Fundraisers](#glossary-fundraiser) to collect [donations](#glossary-donation) for a project. The donated money can be withdrawn from the giveth system throug [milestones](#glossary-milestone). The money donated to a Campaign are locked in the Campaign and the [Donor](#glossary-donor) can no longer withdraw them.

## <a name="glossary-campaign-reviewer"></a>Campaign Reviewer
Is a safety feature to protect [Donors](#glossary-donor) from fraudent [Campaigns](#glossary-campaign). The Campaign Reviewer can reject completion of any milestone and if it comes to the worsed can cancel whole campaign. For the MVP the list of Campaign Reviewers is limited to Giveth trusted addresses.

## <a name="glossary-Dapp"></a>Decentralised Application (Dapp)
Dapp refers to the Giveth platform available at [mvp.giveth.io](https://mvp.giveth.io). It is called decentralised because if you can host your own instance and in future it will be possible to just open the compressed html file from decentralised storage like [Swarm](http://swarm-gateways.net).

## <a name="glossary-DAC"></a>Decentralised Autruistic Community (DAC)
(Pronounced D-A-C) is a minimal entity within the Giveth system allowing users to create a community about a Cause. DAC is created by a single [Delegate](#glossary-delegate) who has the power of [delegating](#glossary-delegation) the DAC's funds to any [Campaign](#glossary-campaign) they find best fulfils the DAC's goals. The money donated to a DAC can be re-called by the [Donor](#glossary-donor) at any time.

## <a name="glossary-delegate"></a>Delegate
Delegate is an administrator of a [DAC](#glossary-DAC) he/she created and is the only person who can [delegate](#glossary-delegation) donated money from the [DAC](#glossary-DAC) to a [Campaign](#glossary-campaign).

## <a name="glossary-delegation"></a>Delegation
Is a process where [Delegate](#glossary-delegate) transfers the money from his/her [DAC](#glossary-DAC) to a [Campaign](#glossary-campaign). The [Donor](#glossary-donor) who donated that money to the [DAC](#glossary-DAC) and whose money has beed delegated has a certain amount of time (by default 3 days) to disagree with the delegation and cancel it. If no action is taken, the delegated money will be locked in the [Campaign](#glossary-campaign).

## <a name="glossary-donation"></a>Donation
Donation is any non-zero amount of [Ether](#glossary-ether) that a user of the Giveth [Dapp](#glossary-Dapp) send to a [DAC](#glossary-DAC), [Campaign](#glossary-campaign) or to a [Milestone](#glossary-milestone).

## <a name="glossary-donor"></a>Donor
Donor is any user who donated money to a [DAC](#glossary-DAC), [Campaign](#glossary-campaign) or to a [Milestone](#glossary-milestone). In future we plan to allow users to donate money directly to a [Milestone](#glossary-milestone).

## <a name="glossary-ether"></a>Ether
Ether is the currency of the [Ethereum Project](https://ethereum.org) blockchain which we are using to build our system. Ether is used in our system to both give money to causes and to pay small fee for any transaction that happens in the process (these are native transactions to the Ethereum blockchain and Giveth does not get any commision of the transaction fee).

## <a name="glossary-fundraiser"></a>Fundraiser
Fundraser is an administrator of a [Campagin](#glossary-campaign) he/she created and is the only person who can create [Milestones](#glossary-milestone) and sent the donated money locked in the [Campaign](#glossary-campaign) to these [Milestones](#glossary-milestone).

## <a name="glossary-maker"></a>Maker
Maker is appointed by the [Fundraiser](#glossary-fundraiser) to a [Milestone](#glossary-milestone) within the [Fundraiser's](#glossary-fundraiser) [Campaign](#glossary-campaign). The role of the Maker is to make sure the state and/or actions described in the [Milestone](#glossary-fundraiser) are achieved.

## <a name="glossary-milestone"></a>Milestone
Milestones are created within a [Campaign](#glossary-campaign) by the [Fundraiser](#glossary-fundraiser). The Milestones are  is the only way

The money donated to a Milestone are locked in the Milestone and the [Donor](#glossary-donor) can no longer withdraw them. However, should the Milestone be cancelled, the money are returned to the [Donors](#glossary-donor).

## <a name="glossary-MVP"></a>Minimal Viable Product (MVP)
Is a minimal version of Giveth system that has all the basic functionality a [Donor](#glossary-donor) and change [Maker](#glossary-maker) would need. You can read more in the [MVP chapter](./MVP.md).

## <a name="glossary-PoC"></a>Proof of Concept (PoC)

## Reviewer
