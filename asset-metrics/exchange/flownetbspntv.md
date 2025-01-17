# Bitstamp Net Flows \(native units\)

## Definition

The net native units value sent or withdrawn to/from Bitstamp that interval.

| Name | MetricID | Category | Subcategory | Type | Unit | Interval |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Bitstamp Net Flows \(native units\) | FlowNetBSPNtv | Exchange | Net Flows | Sum | Native units | 1 day |

## Details

* Native units are considered as sent to an exchange if they are sent to an address we identify as being owned by an exchange.
* Native units are considered as withdrawn if they leave the control of an address we identify as being owned by an exchange.
* This metric is the net of the sends and withdrawals that interval.

## Asset-Specific Details

* This metric might not be available for all assets. Either that exchange doesn’t support this asset \(BitMEX only trades in BTC for example\), or we deemed that our coverage of the exchange was not complete enough to release the metric for it.
* For Bitcoin, this metric excludes the effect of change outputs:
  * If a transaction sends 90 BTC to exchange A but also withdraws 50 BTC from it, the flow is +40 BTC, not +90 BTC and -50 BTC.

## Release History

* Released in the 4.0 release of NDP

## Availability for Assets

{% embed url="https://docs.coinmetrics.io/info/metrics/FlowNetBSPNtv" %}



