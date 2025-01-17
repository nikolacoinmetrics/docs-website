# Kraken Withdrawal Cnt

## Definition

The sum count of transfers from any address belonging to exchange Kraken in that interval. If the recipient address also belongs to Kraken, the transfer is not counted.

| Name | MetricID | Category | Subcategory | Type | Unit | Interval |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Kraken Withdrawal Cnt | FlowTfrOutKRKCnt | Exchange | Withdrawals | Sum | Native units | 1 block, 1 day |

## Details

* Coinbase \(i.e., miner reward\) transactions are not counted.

## Asset-Specific Details

* For account-based protocols, if both sender and recipient belong to Kraken, then the transfer is not counted.
* For UTXO-based protocols, this metric applies the following logic:
  * If the input addresses belong to Kraken, then only the outputs where the address doesn’t belong to Kraken are counted as transfers from Kraken.

## Release History

* Version 4.2 of CM Network Data Pro Daily Macro \(End of Day\)

## Availability for Assets

{% embed url="https://docs.coinmetrics.io/info/metrics/FlowTfrOutKRKCnt" %}

