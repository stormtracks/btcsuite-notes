

#### utxo : unspent transaction output

A single transaction can create multiple outputs, as would be the case when sending to multiple addresses, but each output of a particular transaction can only be used as an input once in the block chain. Any subsequent reference is a forbidden double spend—an attempt to spend the same satoshis twice.

Outputs are tied to transaction identifiers (TXIDs), which are the hashes of signed transactions.

Because each output of a particular transaction can only be spent once, the outputs of all transactions included in the block chain can be categorized as either Unspent Transaction Outputs (UTXOs) or spent transaction outputs. For a payment to be valid, it must only use UTXOs as inputs.

[reference utxo]
(https://bitcoin.org/en/developer-guide#block-chain-overview)

*Notes about only the two core files actor and comm, all the methods listed here are called from within the file*

### actor.go

* queueUtxos [goroutine only]
* splitUtxos [goroutine only]
* simulateTx [goroutine only]

##### sendRawTransaction
is called by simulateTx, splitUtxos


### comm.go

* queueblocks [goroutine only]
* poolUtxos [goroutine only]
* Communicate [goroutine only]

##### getUtxo & getActor
are called by poolUxos
