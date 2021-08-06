# Binance Deposits \(native units\)

## Definition

The sum in native units sent to Binance that interval.

| Name | MetricID | Category | Subcategory | Type | Unit | Interval |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Binance Deposits \(native units\) | FlowInBNBNtv | Exchange | Deposits | Sum | Native units | 1 block, 1 day |

## Details

* Native units are considered as sent to an exchange if they are sent to an address we identify as being owned by an exchange.

## Asset-Specific Details

* This metric might not be available for all assets. Either that exchange doesn’t support this asset, or we deemed that our coverage of the exchange was not complete enough to release the metric for it.
* For Bitcoin, this metric excludes the effect of change outputs:
* * If a transaction sends 90 BTC to exchange A but also withdraws 50 BTC from it, the flow is +40 BTC, not +90 BTC and -50 BTC.

## Release History

* Released in the 4.0 release of NDP

## Availailbity for Assets

{% embed url="https://docs.coinmetrics.io/info/metrics/FlowInBNBNtv" %}



| Asset | Available in [Community](https://docs.coinmetrics.io/api/tiers/community) tier | Available in [Pro](https://docs.coinmetrics.io/api/tiers/pro) tier |
| :--- | :--- | :--- |
| [BTC](https://docs.coinmetrics.io/info/assets/btc) |  |  |
| [ETH](https://docs.coinmetrics.io/info/assets/eth) |  |  |
