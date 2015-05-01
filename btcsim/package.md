
Packages for btcsim are located
[here]
(http://godoc.org/github.com/btcsuite/btcsim?imports)

### btcd packages

The following packages from btcd are referenced in btcsim

#### blockchain [comm.go]

```
coinbaseQueue: make(chan *btcutil.Tx, blockchain.CoinbaseMaturity),
```

#### btcjson [actor.go]

```
actor.go:				inputs := []btcjson.TransactionInput{{
actor.go:				inputs := []btcjson.TransactionInput{{
actor.go:func (a *Actor) sendRawTransaction(inputs []btcjson.TransactionInput, amounts map[btcutil.Address]btcutil.Amount) error {
```

#### chaincfg [comm.go]

```
&chaincfg.SimNetParams)
```

#### txscript [comm.go]

```
_, addrs, _, err := txscript.ExtractPkScriptAddrs(vout.PkScript,
```

#### wire

In many places

### btcrpcclient

The following files make RPC calls [actor, comm, miner, node, simulation]

### btcutil

In many places
