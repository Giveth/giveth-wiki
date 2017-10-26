# MVP

The Giveth system is a minimal product that allows users to give money to communities around causes and to build these communities. The system is a set of [smart contracts]() living on [Ethereum Project blockchain](https://ethereum.org), [caching server]() and [graphical user interface (GUI)](). Currently we are in a closed alpha testing phase, should you be interested to help us test the system, please contact `@vojtech` on the [Giveth Slack](http://slack.giveth.io/).

## Executive Summary

The system consists of:
- **DACs** short for Decentralised Altruistic Communities. Every DAC is community around cause to which users can donate money. DAC is owned by a Delegate who can delegate the donations to Campaigns linked to the DAC.
- **Campaigns** are individual projects with owned by a Campaign Manager. These projects have Milestones through which the people behind the Campaign can get funding.
- **Milestones** can be created within a Campaign and are the only way how to get money out of the Giveth system. The Milestones can be proposed by the Campaign Manager and follow a workflow where multiple people can interact with it to ensure the milestone has been accomplished.

There are also 7 roles:
- **Campaign Reviewer** who can cancel Campaign and who can review completion of any Milestone within the Campaign.
- **Campaign Manager** who is a sole owner of a Campaign and can fund a Milestone with campaign money.
- **Delegate** who is a sole owner of a DAC and can delegate money from the DAC to a Campaign or a Milestone within the Campaign.
- **Giver** who can give (donate) money to a DAC, Campaign or a Milestone.
- **Milestone Manager** who is responsible for making sure that a Milestone is accomplished.
- **Milestone Reviewer** who reviews the completion of a Milestone.
- **Recipient** who receives the money from a completed Milestone.

## Giveth in Depth

Lets have a second, more in depth look on the Giveth system. There are 3 distinct entities build in the system which are handling the donated money. The relations between them is depicted in [Figure 1](#mvp-fig-relations). Each of the 3 entities corresponds to one or more smart contracts.

![Relations between DACs, Campaigns and Milestones](../images/mvp-relations.svg)

<a name="mvp-fig-relations">Figure 1</a>: Relations between DACs, Campaigns and Milestones. The DACs and Campaigns can be linked with each other, but can also stand completely alone. On the other hand, every milestone can be linked to exactly one Campaign, but multiple Milestones can exist in one Campaign.

### Givers

Before we dive in the different entities, lets briefly talk about arguably the most important users in our system - Givers. Under the term Giver we understand anyone who used our platform to give money to a DAC, Campaign or a Milestone. Givers can interact with these 3 entities, but are not explicitely part of any unless they fullfill some other role as well. You can see the roles locality in [Figure 2](#mvp-fig-role-locality).

![Relations between DACs, Campaigns and Milestones](../images/mvp-role-locality.svg)

<a name="mvp-fig-role-locality">Figure 2</a>: The locality of roles, all the roles have a limited scope and once the entity seize to exist so do the roles. Every DAC contains exactly one Delegate, every Campaign a Fundraiser and Campaign Reviewer and every milestone has a Reviewer, Maker and Spender. The Giver is not associated with any entity explicitely but may interact with all of them.

### DACs
Decentralised Altruistic Communities are the most general entity in the Giveth System. The purpose of a DAC is to provide Givers a mean to give money to a cause without having to research the projects making the change. Any money donated to a DAC can be retrieved by the Giver, however we strongly discourage Givers to do so. The funds remain in the DAC until they are delegated to a Campaign or a Milestone.

#### Delegate
Delegate is the owner of a DAC and can delegate the funds donated to it. Any delegation

### Campaigns

### Milestones


You can see a graphical representation in this presentation https://drive.google.com/file/d/0B60avMx-H9BCTGszU2VNcEhzdTA/view?usp=sharing and in this use case diagram https://drive.google.com/file/d/0B60avMx-H9BCZmxJX3VaQkEzTWM/view?usp=sharing


 The donation to the Campaign will not be capped, but there will be a warning shown if the campaign already has as much money as is the sum of its milestones.
