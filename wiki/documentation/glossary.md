# Glossary

This page explains some of the terms commonly used within the Giveth system.

## <a name="campaign">Campaign</a>
A Campaign is a minimal entity that allows [Fundraisers](#fundraiser) to collect [Donations](#donation) for a project. The donated money can be withdrawn from the Giveth system through [Milestones](#milestone). The funds donated directly to a Campaign are locked in the Campaign and the [Giver](#giver) can no longer withdraw them.

## <a name="campaign-reviewer">Campaign Reviewer</a>
The function of a Campaign Reviewer has been integrated as a safety feature to protect [Givers](#giver) from fraudulent [Campaigns](#campaign). The Campaign Reviewer can reject completion of any [Milestone](#milestone) and can, as a strong security measure, even cancel a whole Campaign. For the MVP the list of Campaign Reviewers is limited to Giveth trusted addresses.

## <a name="Dapp">DApp</a>
A DApp is in the context of Giveth the 'Donation Application', which is the Giveth platform<!--, currently available in alpha stage at [mvp.giveth.io](https://mvp.giveth.io)-->. It also refers to a more widely known meaning - 'Decentralized Application'. The Giveth DApp is decentralized as you can host your own instance, in the future it will be possible to just open the compressed html file from decentralised storage like [Swarm](http://swarm-gateways.net).

## <a name="DAC">Decentralized Altruistic Community (DAC)</a>
A DAC (pronounced D-A-C) is a minimal entity within the Giveth system allowing users to create a community around a cause. A DAC is created by a single [Delegate](#delegate) who has the power of [delegating](#delegation) the DAC's funds to any [Campaign](#campaign) they find best fullfils the DAC's goals. The money donated to a DAC can be re-called by the [Giver](#giver) at any time.

## <a name="delegate">Delegate</a>
A Delegate is an administrator of a [DAC](#DAC) he/she created and is the only person who can [delegate](#delegation) donated money from the [DAC](#DAC) to a [Campaign](#campaign).

## <a name="delegation">Delegation</a>
A delegation is a process where a [Delegate](#delegate) transfers the money from his/her [DAC](#DAC) to a [Campaign](#campaign). The [Giver](#giver) who donated that money to the [DAC](#DAC) and whose money has been delegated has a certain amount of time (by default 3 days) to disagree with the delegation and cancel it. If no action is taken, the delegated money will be locked in the [Campaign](#campaign).

## <a name="donation">Donation</a>
A Donation is any non-zero amount of [Ether](#ether) that a user of the Giveth [DApp](#Dapp) sends to a [DAC](#DAC), [Campaign](#campaign) or to a [Milestone](#milestone).

## <a name="ether">Ether</a>
Ether is the currency of the [Ethereum Project](https://ethereum.org) blockchain which we are using to build our system. Ether is used in our system to both give money to Causes and to pay a small fee for any transaction that happens in the process (these are transaction fees native to the Ethereum blockchain, Giveth will never charge any fees whatsoever).

## <a name="fundraiser">Fundraiser</a>
A Fundraiser is an administrator of a [Campaign](#campaign) he/she created and is the only person who can create [Milestones](#milestone) and send the donated money locked in the [Campaign](#campaign) to these [Milestones](#milestone).

## <a name="giver">Giver</a>
A Giver is any user who donates money to a [DAC](#DAC), [Campaign](#campaign) or to a [Milestone](#milestone). In the future we plan to allow users to give money directly to a [Milestone](#milestone).

## <a name="giveth">Giveth</a>
The term Giveth refers to the open-source donation system developed by the [Giveth DAC](#giveth-DAC). You can find more information on our [Website](https://giveth.io) and our [Github Page](https://github.com/Giveth).

## <a name="giveth-DAC">Giveth DAC</a>
The Giveth DAC is a Decentralised Altruistic Community working on developing, maintaining and promoting the [Giveth system](#giveth).

## <a name="maker">Maker</a>
A Maker is appointed by the [Fundraiser](#fundraiser) to a [Milestone](#milestone) within the [Fundraiser's](#fundraiser) [Campaign](#campaign). The role of the Maker is to make sure the state and/or actions described in the [Milestone](#milestone) are achieved.

## <a name="milestone">Milestone</a>
Milestones are created within a [Campaign](#campaign) by the [Fundraiser](#fundraiser). The purpose of the Milestones is to provide a secure, transparent way of withdrawing the [Campaign's](#campaign) donations from the Giveth [DApp](#Dapp) to be able to use them for the purpose set in the Milestone description. The funds donated to a Milestone are locked in the Milestone and the [Giver](#giver) can no longer withdraw them. However, should the Milestone be cancelled, the funds are returned to the [Givers](#giver).

## <a name="MVP">Minimum Viable Product (MVP)</a>
The MVP is a minimal version of the Giveth system that has all the basic functionalities a [Giver](#giver) and change [Maker](#maker) would need. You can read more in the [MVP chapter](../documentation/mvp).

## <a name="PoC">Proof of Concept (PoC)</a>
The Giveth Proof of Concept system is the first [DApp](#Dapp) developed by the [Giveth DAC](#giveth-DAC). It is often referred to as the Milestone Tracker and can be accessed on [dapp.giveth.io](https://dapp.giveth.io). Currently it is used by the [Giveth DAC](#giveth-DAC) to fund the development of [Giveth](#giveth). The system is no longer maintained and as of now only works on Google Chrome with the [Metamask](#giveth-DAC) extension.

## <a name="reviewer">Reviewer</a>
A Reviewer is appointed by the [Fundraiser](#fundraiser) to a [Milestone](#milestone) within the [Fundraiser's](#fundraiser) [Campaign](#campaign). The role of the Reviewer is to confirm that the [Maker](#maker) really achieved the proposed goal or action described in the [Milestone](#milestone). Only after the Reviewer's approval the Milestone funds will be paid to the [Spender](#spender).

## <a name="spender">Spender</a>
A Spender is the final recipient of funds from a successfully completed [Milestone](#milestone).
