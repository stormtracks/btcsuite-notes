

These are called in simulation.go and miner.go

[NotifyBlocks]
(http://godoc.org/github.com/btcsuite/btcrpcclient#Client.NotifyBlocks)

[OnBlockConnected]
(http://godoc.org/github.com/btcsuite/btcrpcclient#NotificationHandlers)

// utxoQueue is the queue of utxos belonging to a actor
// utxos are queued after a block is received and are dispatched
// to their respective owner from com.poolUtxos
// they are dequeued from simulateTx and splitUtxos
