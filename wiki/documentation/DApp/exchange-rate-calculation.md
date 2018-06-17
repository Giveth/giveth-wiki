# How we calculate Ether - Fiat exchange rates

When Giveth needs exchange rates outside of the Giveth DApp, we use this [social coding project](https://giveth.github.io/xchange-rates/) which follows the same methodolagy as the DApp and should give the same result.

When you create a milestone within the [Giveth DApp](https://alpha.giveth.io), you can enter an amount in ether or in fiat. Our system then automatically calculates the conversion rate based on the date of the milestone. 

This is how it works:

In our Feathers backend we keep a cache of the daily average exchange rate for each date. We use Crypto Compare to fetch these rates as we found it the most reliable api. Another plus is that it aggregates data from 80+ exchanges. This is how [Crypto Compare](https://www.cryptocompare.com/api/#-api-data-price) calculates the daily average:

> Our index uses a  **VWAP**  approach  **(Volume Weighted Average
> Price)**  taking into account the **past 24 hours**  **volume**. So
> taking two exchanges,  **A**  and  **B**, where  **A**  has  **75%** 
> of the volume in the past  **24 hours**  we calculate our  **index** 
> as follows:
> 
> > 0.75 x (Last Trade on A) + 0.25 x (LastTrade on B)
> 
> To work out the percentage of volume that an exchange has we only sum
> exchanges that we include in the price calculation (i.e. we don't
> include exchanges that have poor pricing).
> 
> The price index also has a volume reduction when taking it into
> account in the average value (CryptoCompare Index). The reduction
> applies only on volumes over 0.01 so it does not affect smaller coins.

When you enter a milestone amount, we fetch the cached conversion rate from Feathers and calculate the result in the UI. When you save the milestone we check that conversion again to make sure all is correct.

Currently we support 5 different fiat currencies. **Please Note** that native trading pairs are only used for EUR and USD, all other fiat currencies are calculated through BTC-USD pair. This does enable us to support projects using fiat currency other than EUR or USD, but mind that additional conversion is taking place on through CryptoCompare.
