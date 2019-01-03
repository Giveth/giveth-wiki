# Roadmap for Giveth
This chapter details the Giveth Donation Application (DApp) roadmap for the imminent future until the official release (= open for the general public). There are no dates nor deadlines in this roadmap, only a list of milestones and set of goals.

## 1. Adding Missing Features
The only DApp users for the foreseeable future is Giveth team and projects within Giveth. We have identified several features that are currently missing and are preventing us from using the DApp's full potential. [See all still open feature issues on GitHub](https://github.com/Giveth/giveth-dapp/issues?q=is%3Aissue+is%3Aopen+label%3A%22on+roadmap%22).

**Pagination, Sorting & Filtering**
[[#256](https://github.com/Giveth/giveth-dapp/issues/256)]
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg) -
The tables in views like My Milestones, My Communities, My Donations... currently don't have any pagination and once user creates certain amount of the given entities they are hidden. Add support for a pagination of the content and multiple column sorting & filtering. The currently applied filters and sorting should be saved in the user preference.

**ScalingNOW Bridge**
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg)
![Smart Contracts](../../images/roadmap/smart-contracts.svg) -
Allow receiving donations and paying out recipients on the mainnet but keep all the DApp logic on the sidechain with linked tokens.

**Token Integration**
[[#257](https://github.com/Giveth/giveth-dapp/issues/257)]
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg)
![Smart Contracts](../../images/roadmap/smart-contracts.svg) -
Add support for donating and working with any ERC20 tokens. The aim is to integrate tokens like DAI to decrease value fluctuation.

**IPFS Integration**
[[#258](https://github.com/Giveth/giveth-dapp/issues/258)]
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg)
![Smart Contracts](../../images/roadmap/smart-contracts.svg)

1. Set up the IPFS consortium node(s) that we can run with Swarm City.
2. Modify the DApp to store profile data in there rather than on chain/just feathers.
3. Create components for uploading, replacing and viewing pictures, videos and other files uploaded to IPFS. Bonus points for integrating the uploads to wall of fame.

**Support Injected web3 Instances**
[[#173](https://github.com/Giveth/giveth-dapp/issues/173),
 [#174](https://github.com/Giveth/giveth-dapp/issues/174)]
![React](../../images/roadmap/react.svg) -
Allow signing up and using the DApp with Metamask and other web3 instances.

**Donation Splitting**
[[#177](https://github.com/Giveth/giveth-dapp/issues/177)]
![React](../../images/roadmap/react.svg) -
Delegate should be able to just define how much money should be delegated to a Campaign or Milestone and the system should figure out which donations will be used and split them if necessary.

**Milestone Conversation**
[[#99](https://github.com/Giveth/giveth-dapp/issues/99)]
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg) -
Right now it is difficult to understand what is the status of Milestones, Campaings and DACs and what exactly happened when. Adding comments and status change reporting (similar to GitHub) should greatly improve the transparency.

**Deleting Proposed Milestone by Proposer**
[[#259](https://github.com/Giveth/giveth-dapp/issues/259)]
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg) -
The proposer of a milestone should be able to delete the milestone when it is in the state `proposed` or `rejected`.

## 2. Performance Optimisation & Design Review
Once all the features are implemented, we would like to show the product to other projects and charities. The aim is to see how they can use the system and what functionality are they missing. During this period the devteam will focus on improving the platform reliability and designing new UI to improve user experience.

**Models and Services**
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg) -
Simplifying the architecture and externalising the logic from components. The aim is to have a set of models that can be shared between frontend and backend to guarantee data consistency. The component model should be reviewed and systems like Redux used to simplify the workflow.

**Tests & Testing Data**
![Feathers](../../images/roadmap/feathers.svg)
![React](../../images/roadmap/react.svg) -
Writing automatised tests for the frontend and backend. There is no plan to write UI regression tests but rather verify the models, services and create automated integration tests. A set of testing data will be created such that all the 5 testrpc keystore addresses play all the roles and can perform any action. A script will be created to clear the `/data` folder and deploy the test data.

**User Experience Review** -
Review the platform screen by screen and improve the overall user experience. The idea is to create a graphical interface overhaul in some prototyping tool and review it with the team. The aim is to create single view for exploring DACs, Campaigns and Milestones and redesigning the user profiles as well as milestone workflow.

## 3. Release of v1.0, Planning v2.0
Once the system has been battle tested by Giveth and shown to several projects and charities outside of Giveth, the team selects new set of features that are necessary for version 1.0 and finalises the UI redesign for v1.0. The v1.0 is released once the new design and features are implemented and work on v2.0 starts.
