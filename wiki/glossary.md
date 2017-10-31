# Glossary

This page explains some of the terms commonly used within the Giveth system.

## <a name="glossary-campaign"></a>Campaign
A Campaign is a minimal entity that allows [Campaign Managers](#glossary-campaign-manager) to collect [Donations](#glossary-donation) for a project. The donated money can be withdrawn from the Giveth system through [Milestones](#glossary-milestone). The funds donated directly to a Campaign are locked in the Campaign and the [Giver](#glossary-giver) can no longer withdraw them.

## <a name="glossary-campaign-manager"></a>Campaign Manager
A Campaign Manager is an administrator of a [Campaign](#glossary-campaign) he/she created and is the only person who can create [Milestones](#glossary-milestone) and send the donated money locked in the [Campaign](#glossary-campaign) to these [Milestones](#glossary-milestone).

## <a name="glossary-campaign-reviewer"></a>Campaign Reviewer
The function of a Campaign Reviewer has been integrated as a safety feature to protect [Givers](#glossary-giver) from fraudulent [Campaigns](#glossary-campaign). The Campaign Reviewer can reject completion of any [Milestone](#glossary-milestone) and, if it comes to the worse, can cancel a whole Campaign. For the MVP the list of Campaign Reviewers is limited to Giveth trusted addresses.

## <a name="glossary-Dapp"></a>DApp
A DApp is in the context of Giveth the 'Donation Application', which is the Giveth platform<!--, currently available in alpha stage at [mvp.giveth.io](https://mvp.giveth.io)-->. It of course also refers to a 'Decentralized Application': the Giveth DApp is decentralised as you can host your own instance, in the future it will be possible to just open the compressed html file from decentralised storage like [Swarm](http://swarm-gateways.net).

## <a name="glossary-DAC"></a>Decentralised Altruistic Community (DAC)
A DAC (pronounced D-A-C) is a minimal entity within the Giveth system allowing users to create a community around a Cause. A DAC is created by a single [Delegate](#glossary-delegate) who has the power of [delegating](#glossary-delegation) the DAC's funds to any [Campaign](#glossary-campaign) they find best fullfils the DAC's goals. The money donated to a DAC can be re-called by the [Giver](#glossary-giver) at any time.

## <a name="glossary-delegate"></a>Delegate
A Delegate is an administrator of a [DAC](#glossary-DAC) he/she created and is the only person who can [delegate](#glossary-delegation) donated money from the [DAC](#glossary-DAC) to a [Campaign](#glossary-campaign).

## <a name="glossary-delegation"></a>Delegation
A delegation is a process where a [Delegate](#glossary-delegate) transfers the money from his/her [DAC](#glossary-DAC) to a [Campaign](#glossary-campaign). The [Giver](#glossary-giver) who donated that money to the [DAC](#glossary-DAC) and whose money has been delegated has a certain amount of time (by default 3 days) to disagree with the delegation and cancel it. If no action is taken, the delegated money will be locked in the [Campaign](#glossary-campaign).

## <a name="glossary-donation"></a>Donation
A Donation is any non-zero amount of [Ether](#glossary-ether) that a user of the Giveth [DApp](#glossary-Dapp) sends to a [DAC](#glossary-DAC), [Campaign](#glossary-campaign) or to a [Milestone](#glossary-milestone).

## <a name="glossary-ether"></a>Ether
Ether is the currency of the [Ethereum Project](https://ethereum.org) blockchain which we are using to build our system. Ether is used in our system to both give money to Causes and to pay a small fee for any transaction that happens in the process (these are transaction fees native to the Ethereum blockchain, Giveth will never charge any fees whatsoever).

## <a name="glossary-giver"></a>Giver
A Giver is any user who donates money to a [DAC](#glossary-DAC), [Campaign](#glossary-campaign) or to a [Milestone](#glossary-milestone). In the future we plan to allow users to give money directly to a [Milestone](#glossary-milestone).

## <a name="glossary-giveth"></a>Giveth
The term Giveth refers to the open-source donation system developed by the [Giveth DAC](#glossary-giveth-DAC). You can find more information on our [Website](https://giveth.io) and our [Github Page](https://github.com/Giveth).

## <a name="glossary-giveth-DAC"></a>Giveth DAC
The Giveth DAC is a Decentralised Altruistic Community working on developing, maintaining and promoting the [Giveth system](#glossary-giveth).

## <a name="glossary-milestone"></a>Milestone
Milestones are created within a [Campaign](#glossary-campaign) by the [Campaign Manager](#glossary-campaign-manager). The purpose of the Milestones is to provide a secure, transparent way of withdrawing the [Campaign's](#glossary-campaign) donations from the Giveth [DApp](#glossary-Dapp) to be able to use them for the purpose set in the Milestone description. The funds donated to a Milestone are locked in the Milestone and the [Giver](#glossary-giver) can no longer withdraw them. However, should the Milestone be cancelled, the funds are returned to the [Givers](#glossary-giver).

## <a name="glossary-milestone-manager"></a>Milestone Manager
A Milestone Manager is appointed by the [Campaign Manager](#glossary-campaign-manager) to a [Milestone](#glossary-milestone) within the [Campaign Manager's](#glossary-campaign-manager) [Campaign](#glossary-campaign). The role of the Milestone Manager is to make sure the state and/or actions described in the [Milestone](#glossary-milestone) are achieved.

## <a name="glossary-milestone-reviewer"></a> Milestone Reviewer
A Milestone Reviewer is appointed by the [Campaign Manager](#glossary-campaign-manager) to a [Milestone](#glossary-milestone) within the [Campaign Manager's](#glossary-campaign-manager) [Campaign](#glossary-campaign). The role of the Milestone Reviewer is to confirm that the [Milestone Manager](#glossary-milestone-manager) really achieved the proposed goal or action described in the [Milestone](#glossary-milestone). Only after the Milestone Reviewer's approval the Milestone funds will be paid to the [Recipient](#glossary-recipient).

## <a name="glossary-MVP"></a>Minimum Viable Product (MVP)
The MVP is a minimal version of the Giveth system that has all the basic functionalities a [Giver](#glossary-giver) and change [Milestone Manager](#glossary-milestone-manager) would need. You can read more in the [MVP chapter](./MVP.md).

## <a name="glossary-PoC"></a>Proof of Concept (PoC)
The Giveth Proof of Concept system is the first [DApp](#glossary-Dapp) developed by the [Giveth DAC](#glossary-giveth-DAC). It is often referred to as the Milestone Tracker and can be accessed on [dapp.giveth.io](https://dapp.giveth.io). Currently it is used by the [Giveth DAC](#glossary-giveth-DAC) to fund the development of [Giveth](#glossary-giveth). The system is no longer maintained and as of now only works on Google Chrome with the [Metamask](#glossary-giveth-DAC) extension.

## <a name="glossary-recipient"></a> Recipient
A Recipient is the final recipient of funds from a successfully completed [Milestone](#glossary-milestone).
