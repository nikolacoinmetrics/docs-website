# Payments (Xfers) Above $X, Sum (native units)

## Definition

The sum of all payments (transfers) that have occured in the measuring interval above a specific USD amount, displayed in native units (e.g. BTC). This family of metric supports $100k, $1M, $10M, and $100M USD value thresholds.

| Name                                                      | MetricID             | Category     | Subcategory  | Type | Unit         | Interval |
| --------------------------------------------------------- | -------------------- | ------------ | ------------ | ---- | ------------ | -------- |
| Transactions, transfers, value, above $100k, native units | TxTfrValAbUSD100kNtv | Transactions | Transactions | Sum  | Native units | 1d       |
| Transactions, transfers, value, above $1M, native units   | TxTfrValAbUSD1MNtv   | Transactions | Transactions | Sum  | Native units | 1d       |
| Transactions, transfers, value, above $10M, native units  | TxTfrValAbUSD10MNtv  | Transactions | Transactions | Sum  | Native units | 1d       |
| Transactions, transfers, value, above $100M, native units | TxTfrValAbUSD100MNtv | Transactions | Transactions | Sum  | Native units | 1d       |

## Details

* This metrics shows the sum of payments above each of the supported thresholds.
* Payments are defined as transfers (xfers) and represent the individual asset transfers _within_ a transaction.
* A transaction may be a collection of transfers which, specially in UTXO-based blockchains, may represent several P2P payments.&#x20;
* A cryptoasset exchange, for example, may engage in _transaction batching_ whereby user withdraws are aggregated in a single transaction comprised of multiple outputs.&#x20;
* Each of the outputs represents a transfer. And while each transfer (output) may be going to different users, they are all processed within the same transaction.
* For this reason, this metric is calculated at the transfer-level so all individual payments are accounted for.
* In this version of this metric, change outputs are not adjusted. This means not only peer-to-peer tranfers are accounted for, but also when a user sends fund to their own wallets.
* For example, if after paying each of the users withdrawing, the exchange still has a remaining balance, the change output is still accounted for in this metric if it falls below the metric's threshold.
* In other words, if the recipients listed in a transaction's output require payments that, when added together, have a value that is _lower_ than the input, a change output that goes back to the sender must be created. In such circumstances, this metric would also account for the change output if it fell under the measuring threshold.

## Interpretation

* The thresholds supported by this metric family can be used to better understand the type of users interacting with a cryptoasset network.
* For example, if a network is predominantly being used by whales, one would expect payments above $1M USD to occur more frequently than payments below $10 USD.
* Similarly, it can show the predominance of different types of investors, such the balance between retail and institutional investors within a network.&#x20;

## Release History

* Released in the 5.1 version of NDP
