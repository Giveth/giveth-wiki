# Ideas, Proposals and Concepts for Future versions

The purpose of this part of the wiki is to list all the ideas, proposals and concepts that might be included in future versions of the Giveth System. However, we do not guarantee that any of these ideas will be included.

## <a name="future-location">Locations of DACs, Campaigns and Milestones</a>
It would be useful to add multiple locations to where the DACs, Campaigns and Milestones are happening or are located.

The proposal is:
  1. Pick exact locations (e.g. Address or GPS coordinates)
  2. Pick a country
  3. Pick a continent

If the user picks an exact location, the country and continent is automatically deduced. If the country is chosen, the continent is also automatically deduced. Because DACs, Campaigns and even some milestones can be in multiple locations, the location field should be a list and not just a single location. However, there should not be an automated 'inheritance' where the DAC would inherit the locations of its Campaigns.

![Map Preview of a Milestone with Location](../images/future/location.svg)

<a name="fig-location-map">Map Preview of a Milestone with Location</a>: Example on how Milestones could be visually represented on the map.

## <a name="future-location-exploration">Location based exploration of DACs & Campaigns</a>
Assuming each DAC, Campaign and Milestone has a location set, as described in [Locations of DACs, Campaigns and Milestones](#future-location), all these entities could be searched on a map or on a 3D globe. In a DAC you could see to which places the delegations goes and in Campaign the user could see where the individual Milestones took place.

![Example of 3D visualised Campaign](../images/future/location-exploration.png)

<a name="fig-location-exploration-campaign">Example of 3D visualisation to see where geographically a Campaign is making a difference.</a> The concept image is taken from D3js [example page](https://bl.ocks.org/mbostock/4183330).

Additionally, we started to play with above implementation to display the origin locations of current [Unicorn DAC team members](https://giveth.io/world/). For contributions, please fork the [GitHub repo of giveth-world ](https://github.com/giveth/giveth-world)

![Example of 3D visualised Milestones](../images/future/location-exploration-dac.png)

<a name="fig-location-exploration-dac">Example of 3D visualisation to track donation flow geographically.</a> The concept image is taken from D3js [example page](http://mbostock.github.io/d3/talk/20111116/airports.html).

## <a name="future-money-exploration">Money flow based exploration of DACs & Campaigns</a>

Giveth already has a lot of information that is not in use yet. By analysing the transactions, we can easily build graphs that would help people understand where the DAC's money go to and where the Campaign money comes from.

![Money flow from DACs](../images/future/money-flow-dac.svg)

<a name="fig-money-flow-DAC">Where is the Education DAC spending money?</a> Each DAC shows which Campaigns and Milestones are funded. By clicking on each of these the user would get a table with all Campaigns and how much % of the DAC money was delegated to them. The blue elements are DACs, red are Campaigns and green Milestones.

Name | Type | Percentage |
-----|------|------------|
We help kids | Campaign | 35% |
Shool in Zambia | Campaign | 20% |
It Teacher Salary | Milestone | 12% |
Learn to code | Campaign | 10% |
Purchase Graphics Software | Milestone | 6% |
Buy equipment for Computer Lab | Milestone | 4% |
Internet bill February | Milestone | 3% |
Internet bill March | Milestone | 3% |
Internet bill April | Milestone | 3% |
Internet bill June | Milestone | 3% |
Installation of new language education software| Milestone | 2% |
IT olympics for High School Students | Campaign | 1% |

<a name="table-money-flow-DAC">Tabular view of all delegations.</a>

![Money flow to Campaign](../images/future/money-flow-campaign.svg)

<a name="fig-money-flow-campaign">Where is the Campaign getting funding from?</a> The blue elements are DACs, red are Campaigns, green Milestones and white starts are users.

## <a name="future-money-conversion">Real-time and Historical Fiat Conversion</a>

For most people, even the ones already invested in cryptocurrencies, it is difficult to evaluate the fiat value of a certain amount of Ether. Therefore, it would be great to provide a way where they can name a second (fiat) currency to Ether, to use alongside or replacing the system's Ether values. When donating, they could say "I want to donate 100 USD", instead of having to put in the value in Ether. Because we know the exact moment a transaction is happening, we could easily (given acceptance for minor rounding errors) display how much money any past donation was in fiat. This is especially necessary if Ether rapidly gains or loses in value as it becomes unclear how much money a Campaign or DAC had and could lead to a confusion where Campaigns could look overfunded due to dramatic price increase.

![Donations in Fiat](../images/future/fiat-donation.svg)

<a name="fig-fiat-donation">Donating an amount of Ether expressed in fiat currency.</a> The actual donation would still be in Ether, but the value could be expressed in Ether based on recent average value from some major exchange.

Amount ETH | Est. Amount USD | Date             |  Name |
-----------|-----------------|------------------|-------|
Ξ0.551     | $155            | 2017-10-15 10:15 | Jen
Ξ1         | $312.15         | 2017-10-15 9:09  | perissology
Ξ1         | $298.11         | 2017-10-09 18:33 | Vojtech
Ξ2.531     | $100            | 2017-04-19 13:14 | Jim

<a name="table-fiat-dac-donation">This example illustrates a snapshot of past donations and how it could look with value estimated in a fiat currency</a>. Note the significant price change between the last and first donation in the list.

![Expenses in Fiat](../images/future/fiat-spent.svg)

<a name="fig-fiat-spent">Comparison between monthly expenses in ETH and in USD</a>. Example on how it can be deceiving to use Ether vs how much money is actually spent. The data shown here is taken from the [Giveth budget](https://docs.google.com/spreadsheets/d/1Qg7OiQ42jmsW3HCgtGA-v5NfxMEAR5SMo_oc7AtEqTE/edit?usp=sharing).

## <a name="future-categories">Categories for Milestones</a>

Currently it is not clear what a Campaign spent their money on. Should users decide to gain this insight, they would have to read through all the Milestones and maybe even then it would not be clear. Adding spending categories could help: Both the Givers and the Makers, gain the ability to evaluate what the money was spent on. The list of categories should be predefined by Giveth and new categories should be created on request. The overhead for the user consists of selecting a category from a list when the milestone is being created. Usage of this feature should be optional.

![Spending Categories for Milestones](../images/future/categories.svg)

<a name="fig-categories">Overview of spending for an example Campaign.</a> The aim is to provide Givers and Makers with a better overview on how this Campaign is spending the money.

## <a name="future-accounting">Accounting, Analytics, Business Intelligence</a>

Even now, the system contains enough information to provide some simple accounting, analytical and business intelligence information. Analytics do not need to be part of the Giveth platform, but could be plugged-in via an external tool. Note that some of these tools work best if the value is expressed in a stable currency. One option to mitigate the stable currency problem is to integrate the [Real-time and Historical Fiat Conversion](future-money-conversion) proposal.

Here are some examples of what could be achieved with this feature:

- Daily cashflow of the Campaign
  - Donation frequency
  - Average amount
  - Target DAC audience
  - Donations and spendings per day/months/years
  - Spending categories (Assumes system has [Categories for Milestones](#future-categories))
  - Recurring Givers
- Spending breakdown at Milestone granularity
  - Amount of time required to raise funds for Milestone
- Future forecasts

![Overtime Balance](../images/future/analytics-overtime.svg)

<a name="fig-analytics-overtime">Example of overtime balance graph.</a> The data is taken from the [Giveth budget](https://docs.google.com/spreadsheets/d/1Qg7OiQ42jmsW3HCgtGA-v5NfxMEAR5SMo_oc7AtEqTE/edit?usp=sharing). Note that this graph does not reflect actual value all that well, as one can easily see the actual value spent in Ether was 60 times lower before March 2017.

![Monthly Spending](../images/future/analytics-monthly-spending.svg)

<a name="fig-analytics-monthly-spending">Example of monthly spending breakdown.</a> The data is taken from the [Giveth budget](https://docs.google.com/spreadsheets/d/1Qg7OiQ42jmsW3HCgtGA-v5NfxMEAR5SMo_oc7AtEqTE/edit?usp=sharing).

## <a name="future-dac-governance">DAC Governance</a>

In the Giveth MVP there is one Delegate per DAC who is the owner and the only person that can delegate donation. The tension is that should the Delegate be unavailable (temporarily or permanently), the DAC will just accumulate donations that could be already making a difference. In addition to that, bigger organisations will need multiple people being able to delegate money. One solution would be to enrich the Delegate role to be able to nominate other Delegates and build a governance system in the DAC. It could then be up to the individual settings of the DAC to define how many votes are necessary to:

1. Nominate a new Delegate
2. Remove a Delegate
3. Change the DAC information (description, DAC's name,...)
4. Delegate Donations
5. Freeze a delegate

As an example, we can assume following setting for DACs:

1. At least 51% of DAC's Delegates to nominate a new Delegate
2. At least 70% to remove a Delegate
3. At least 30% to change the DAC information (description, DAC's name,...)
4. Everyone can delegate without the need to vote (0 votes on donation delegation)
5. Everyone can freeze a delegate and the freeze time is 3 days

**Freeze:** We propose a 'freeze' user action, which can be called by any delegate to temporarily freeze another delegate. Frozen delegates can not take any actions until they are unfrozen.

![Usecase diagram for Delegate](../images/future/dac-governance-delegate.svg)

<a name="fig-dac-governance-delegate-usecase">Use case diagram for Delegate role if the DAC Governance is implemented.</a> The white actions are about changing the DAC's information, green refers to donation delegation, blue are security actions, red are actions to remove delegate and the yellow shows new delegate nomination actions.



![Usecase diagram for Time](../images/future/dac-governance-time.svg)

<a name="fig-dac-governance-time-usecase">Use case diagram for automatic actions if the DAC Governance is implemented.</a> Should there be delegates that did not vote yet, all their votes go to:
  - Support the DAC modification
  - Support donation delegation
  - Support nomination of new Delegate
  - Oppose the removal of a Delegate.

If the delegate is frozen for longer than the time limit, he/she is unfrozen.

## Campaign Governance

## Delegating from DAC to DAC

## Multiple Wallets

## Mobile Wallet integration

## Wallet Recovery System

## Giver Portfolio

## Maker Portfolio

## DAC, Campaign, Milestone Search and Filtering

## Milestone Conversation

## Language Mutations

## Reputation System

## Repetitive Milestones

## Exploration based on Donations and Delegations

## Donation message

## Notifications

### In App

### External
- Email
- Slack
- SMS
- Instant messages..

## If This Then That (IFTTT) Integration

## Push content to external tools
- Facebook
- Twitter

## Video as a proof of work

## Donation Splitting

## Data Import

## Fiat Paygates
