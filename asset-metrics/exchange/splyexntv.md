# Exchange Supply \(native units\)

## Definition

The sum of all native units held in hot or cold exchange wallets that day.

| Name | MetricID | Category | Subcategory | Type | Unit | Interval |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Exchange Supply \(native units\) | SplyExNtv | Supply | Held on exchange | Sum | Native units | 1 day |

## Details

* All wallets \(hot and cold\) are considered to count towards the supply held by exchanges.
* This metric should be seen as an underestimation of the actual figure, as our heuristics and sources might not discover all addresses owned by exchanges.
* This metric includes the balances of all addresses we have flagged as being controlled by an exchange, even if our coverage of the exchange is not complete.

## Release History

* Released in the 4.0 release of NDP

## Availability for Assets

{% embed url="https://docs.coinmetrics.io/info/metrics/SplyExNtv" %}



