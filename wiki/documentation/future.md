# Ideas, Proposals and Concepts for Future versions

The purpose of this part of wiki is to list all the ideas, proposals and concept that could be included in future versions of the Giveth System. However, we do not guarantee that any of these ideas will be included.

## <a name="future-location">Locations of DACs, Campaigns and Milestones</a>
It would be useful to add multiple locations where the DACs, Campaigns and Milestones are happening. The proposal would be to:

1. Pick exact location (e.g. Address or GPS coordinates)
2. Pick a Country
3. Pick a Continent

If the user picks exact location, the Country and Continent is automatically deduced. If the Country is chosen, Continent is also autoatically deduced. Because DACs, Campaigns and even some milestones can be in multiple locations, the location field should be a list and not just single location. However, there should not be inheritance where the DAC would inherit the locations of its Campaigns.

![Map Preview of a Milestone with Location](../images/future/location.svg)

<a name="fig-location-map">Map Preview of a Milestone with Location</a>: Example on how Milestones could be visually represented on the map.

## <a name="future-location-exploration">Location based exploration of DACs & Campaigns</a>
Assuming each DAC, Campaing and Milestone has a as described in [Locations of DACs, Campaigns and Milestones](#future-location), all these entities could be searched on a map or on a 3D globe. In a DAC you could see to which places the delegations goes and in Campaign the user could see where the individual milestones took place.

![Example of 3D visualised Campaign](../images/future/location-exploration.png)

<a name="fig-location-exploration-campaign">Example of 3D visualisation to see where geographically a Campaign is making difference.</a> The concept image is taken from D3js [example page](https://bl.ocks.org/mbostock/4183330).

![Example of 3D visualised Milestones](../images/future/location-exploration-dac.png)

<a name="fig-location-exploration-dac">Example of 3D visualisation to see where  geographically does a DAC money go to.</a> The concept image is taken from D3js [example page](http://mbostock.github.io/d3/talk/20111116/airports.html).

## <a name="future-money-exploration">Money flow based exploration of DACs & Capaigns</a>

Giveth already has a lot of information that it is not using at all. By analysing the transactions, we can easily build graphs that would help people understand wheir the DACs money go through and where the Campaign money comes from. This could be an important ascpect that Givers could consider.

![Money flow from DACs](../images/future/money-flow-dac.svg)

<a name="fig-money-flow-DAC">Each DAC could show what are the Campaigns and Milestones that are being funded. By clicking on the Other the user would get a table with all Campaigns and how much % of the DAC money was delegated to them.</a>

![Money flow to Campaign](../images/future/money-flow-campaign.svg)

<a name="fig-money-flow-campaign">This view would show where does all the Campaign funding come from.</a>

## <a name="future-money-conversion">Real-time and Historical Fiat Conversion</a>

For most People, even the ones already invested in crypto, it is difficult to evaluate how much money certain Ether amount is. Therefore, it would be great to provide a way where they can name a second (fiat) currency to Ether, that would be displayed and used. When donating, they could say "I want to donate 100 USD", instead of having to put in the value in Ether. Because we know when every transaction happen, we could easily (up to small error) display how much money any past donation was in fiat. This is especially necessary if Ether rapidly gains or loses in value as it becomes unclear how much money Campaign or DAC had and could lead to a confusion where Campaigns could look overfunded due to dramatic price increase.

![Donations in Fiat](../images/future/fiat-donation.svg)

<a name="fig-fiat-donation">Donating amount of Ether expressed in fiat currency.</a> The actual donation would still be in Ether, but the value could be expressed in Ether based on recent average value from some major exchange.

Amount ETH | Est. Amount USD | Date             |  Name |
-----------|-----------------|------------------|-------|
Ξ0.551     | $155            | 2017-10-15 10:15 | Jen
Ξ1         | $312.15         | 2017-10-15 9:09  | perissology
Ξ1         | $298.11         | 2017-10-09 18:33 | Vojtech
Ξ2.531     | $100            | 2017-04-19 13:14 | Jim

<a name="table-fiat-dac-donation">Example how could past donation look with value estimated in fiat currency</a>. Note the significant price change between the last and first donation in the list.

## <a name="future-categories">Categories for Milestones</a>

Currently it is not clear what a Campaign spent their money on. Should users decide to gain this insight, they would have to read through all the Milestones and maybe even then it would not be clear. Adding spending categories could help, both the Givers and the Makers, evaluate what were the money spent on. The list of categories should be predefined by Giveth and any new category should be created on request. The overhead for the user consists of selecting a category from a list when the milestone is being created. Of course, setting spending category should be optional.

![Spending Categories for Milestones](../images/future/categories.svg)

<a name="fig-categories">Overview of spending for a Campaign.</a> The aim is to provide Givers and Makers with better idea how is the Campaign spending the money.

## <a name="future-accounting">Accounting, Analytics, Business Inteligence</a>

Even now, the system contains enough information to provide some simple accounting, analytical and business inteligence information. This does not need to be part of the Giveth platform, but could be external tool. Note that these tools, however, work best if the value is expressed in relatively stable currency. One option is to use the [Real-time and Historical Fiat Conversion](future-money-conversion) concept. Below are some examples of what could be achieved.

- Daily cashflow of the Campaign
  - Donation frequency
  - Average amount
  - Target DAC audience
  - Donations and spendings per days/months/years
  - Spending categories (Assumes system has [Categories for Milestones](#future-categories))
  - Recurring Givers
- Spending breakdown at Milestone granularity
  - How much time it takes to raise funds for Milestone
- Future forecasts

![Overtime Balance](../images/future/analytics-overtime.svg)

<a name="fig-fiat-donation">Example of overtime balance graph.</a> The data are taken from Giveth budget. Note that id does not reflect the real spending well as ether was 60 times lower before march 2017.

![Monthly Spending](../images/future/analytics-monthly-spending.svg)

<a name="fig-fiat-donation">Example of monthly spending breakdown.</a> The data are taken from Giveth budget. Note that id does not reflect the real spending well as ether was 60 times lower before march 2017.

## DAC Governance

## Campaign governance

## Delegating from DAC to DAC

## Multiple Wallets

## Giver Portfolio

## Maker Portfolio

## DAC, Campaign, Milestone Search and Filtering

## Milestone Conversation

## Language Mutations

## Reputation

## Repetative Milestones

## Exploration based on Donations and Delegations
