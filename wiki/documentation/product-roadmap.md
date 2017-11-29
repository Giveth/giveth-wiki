# Roadmap for Giveth
This chapter details the Giveth platform roadmap until release (= open for the general public on the Main Ethereum Network). We aim to reach this state by 1st of March 2018.

## As Soon as Possible
**Contributors** -
Allow for meaningful external contributions to application development. We need to create and mark issues suitable for external contributors (=fully defined and clear requests), write contribution guidelines and continuously review and merge the contributors pull requests. The responsible people on the Giveth team are:

- `@perissology` for Smart Contracts and Plugins
- `@perissology` and `@satyaVH` for FeathersJS
- `@satyaVH` and `@vojtech` for Reactjs

**User Experience Review** -
Review the platform screen by screen and improve the overall user experience. The workflow consists of proposals for improvement, reviews of proposals and implementation.

## Launching Giveth on the Ethereum main net - (planned for 2017 November 23)
In order to successfully launch the Giveth donation platform on the Ethereum Main Network, following steps are necessary:

![Done](../images/roadmap/done.svg)
[**Minime Integration**](https://github.com/Giveth/giveth-dapp/issues/143)
![Smart Contracts](../images/roadmap/smart-contracts.svg)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Write a Minime plugin and add the plugin to Liquid Pledging. Add display of the token to UI, which allows Delegates and Campaign managers to name the token to be issued and to all the Givers see how much of which tokens they have. We agreed that tokens are issued only in the following cases:

1. Giver donates to Campaign -> Giver receives Campaign tokens
2. Giver donated to DAC, the DAC delegated the donation to Campaign and the delegation is committed. Only then the Giver receives both: DAC tokens and Campaign tokens. Once we allow delegation from DAC to DAC, only the DAC to which the Giver donated in the first place will issue tokens for them.

![Done](../images/roadmap/done.svg)
**Whitelist of Plugins**
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Creating a white list of plugins that are allowed to be added to Liquid Pledging for the Giveth Platform.

![Done](../images/roadmap/done.svg)
**Whitelist of Reviewers**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Build a white list of Reviewers that can be used by the devteam, as well as modifying the UI to support the whitelist https://github.com/Giveth/giveth-dapp/issues/47.

![Done](../images/roadmap/done.svg)
**Whitelist of Campaign Managers**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Build a white-list of addresses that can create Campaigns. Any Campaign that is not created with these addresses will not be visible in the Giveth Platform before release.

![Done](../images/roadmap/done.svg)
**Whitelist of Delegates**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Build a white-list of addresses that can create DACs. Any DAC that is not created with these addresses will not be visible in the Giveth Platform before release.

![Done](../images/roadmap/done.svg)
[**Role Definitions**](https://github.com/Giveth/giveth-dapp/issues/148)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Adding the Campaign Reviewer. The roles should comply with the [Product Definition](https://wiki.giveth.io/documentation/product-definition/), especially with the [Milestone State Diagram](https://wiki.giveth.io/documentation/product-definition/#product-definition-fig-milestone-statediagram).

![Done](../images/roadmap/done.svg)
[**Propose New Milestones (offchain)**](https://github.com/Giveth/giveth-dapp/issues/147)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Allow anyone to propose a new milestone to a Campaign. The proposal will not be visible to anyone except the Campaign Manager.

![Postponed](../images/roadmap/postponed.svg)
**Gas Price input**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Allow users to set a gas price for Ethereum blockchain transactions.

![Done](../images/roadmap/done.svg)
**Verify Feathers Data Permisions**
![Feathers](../images/roadmap/feathers.svg) -
Verify that there are no permission problems in with our FeathersJS middle-layer.

![Done](../images/roadmap/done.svg)
[**Donate without Registering**](https://github.com/Giveth/giveth-dapp/issues/145)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg)
Add functionality to the Donate button which would give you an option to donate through MyEtherWallet (just like on our [website](https://giveth.io)). The smart contracts need to be altered as well to allow donations from un-registered users.

![Planned](../images/roadmap/planned.svg)
**In House Testing**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
All team members get to test the MVP on the Ropsten test network and provide us with feedback. `@vojtech` will facilitate the testing and collecting feedback.

![Done](../images/roadmap/done.svg)
[**Money Transfer from Dapp**](https://github.com/Giveth/giveth-dapp/issues/149)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
Allow users to transfer money from Giveth DApp to any other address.

![Planned](../images/roadmap/planned.svg)
**Deploy Contracts to Main Network**
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Deploy and verify all the smart contracts and plugins to the Main Ethereum Network.

![Planned](../images/roadmap/planned.svg)
**Deploy Feathers.js**
![Feathers](../images/roadmap/feathers.svg) -
Deploy final clean production version of FeathersJS.

![Planned](../images/roadmap/planned.svg)
**Deploy DApp UI**
![React](../images/roadmap/react.svg) -
Deploy final version of UI and freeze it on Netlify.

## First Campaign - (2018 January 15)
[**DAC Approval for Adding Campaign**](https://github.com/Giveth/giveth-dapp/issues/169)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
The DAC has to approve that it wants to be associated with a Campaign. For now we will only do that in the frontend by not showing unapproved Campaigns as part of a DAC.

[**External Notifications**](https://github.com/Giveth/giveth-dapp/issues/170)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Adding email notifications to the DApp and hooking it to events like new donation, new delegation, milestone status change and others.

**On-boarding 1st Campaign** -
A dedicated person who will be in contact with the first Campaign to use our system. This includes gathering requirements, guided introduction to the platform and collecting feedback.

**Tutorials, Videos, Documentation** -
Preparing tutorials, video and other documentation for the launch based on the feedback from the first Campaign.

[**Link to Dashboard/Milestone Workflow in Campaign**](https://github.com/Giveth/giveth-dapp/issues/171)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Milestone Workflow added to the Campaign (all the buttons right in the milestones).

[**User Customisation - Logo, Page Color**](https://github.com/Giveth/giveth-dapp/issues/172)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Allow users to customise their Campaign page by changing background-color and adding a custom logo.

[**Mist Integration**](https://github.com/Giveth/giveth-dapp/issues/173)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Allow signing up with a Mist Address and interacting with the DApp through Mist.

[**Metamask Integration**](https://github.com/Giveth/giveth-dapp/issues/174)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Allow signing up with a Metamask Address and interacting with the DApp through Metamask.

[**Allow Executing Transactions from MEW**](https://github.com/Giveth/giveth-dapp/issues/175)
![React](../images/roadmap/react.svg) -
Add an option to every transaction button to redirect to MyEthereumWallet with the data and addresses pre-filled.

[**External Testing**](https://github.com/Giveth/giveth-dapp/issues/176)
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg)
All team members of Giveth, as well as pre-approved Campaigns get to test Giveth on the Ropsten test network and provide us with a feedback. `@vojtech` will facilitate the testing and collect feedback.

## First DAC - (2018 February 15)
**Gathering DACs (and Campaigns)** -
On-going process of gathering and on-boarding other DACs and Campaigns.

**Multiple Delegates in DAC**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Allow multiple delegates that can propose delegation and can approve/reject the delegation (just the green actions in the [DAC governance diagram](https://wiki.giveth.io/documentation/future/fig-dac-governance-delegate-usecase))

## Official Release - (2018 March 1)
**Gathering DACs and Campaigns**
On-going process of gathering and on-boarding other DACs and Campaigns for main release.

## At earliest opportunity
**Verify Feathers**
![Feathers](../images/roadmap/feathers.svg) -
Fully verify FeathersJS models and restrictions

**Tests**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg) -
Add frontend and backend tests.

**Anonymous Donations from Exchanges**
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Allow donating from exchanges and receiving donation tokens.

**Mutual DAC an Campaign Linking**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Allow bi-directional linking of DACs and Campaigns (currently only Campaigns can link with DACs).

**Token Support**
![Feathers](../images/roadmap/feathers.svg)
![React](../images/roadmap/react.svg)
![Smart Contracts](../images/roadmap/smart-contracts.svg) -
Support using the ERC20 and ERC223 token standard in the Giveth platform for all possible actions.
