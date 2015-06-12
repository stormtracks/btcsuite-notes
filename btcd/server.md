
The Servers Start method starts 7 services including

* listenHandler
* peer
* upnpUpdateThread
* rebroadcastHandler
* rpcServer
* cpuMiner
* addrIndexer

For more details see the Servers Start method code.

When the peerHandler inside the Server starts up it also goes ahead and starts

* addrManager
* blockManager

The server is located in **server.go**

##### listenHandler



In config.go there is a parameter called *activeNetParams* which sets up **cfg.Listeners**

The interface/port to listen for connections is a function of the type of network
{Mainnet, Testnet, Regnet, Simnet}
which is defined
[here]
(https://github.com/btcsuite/btcd/blob/master/chaincfg/params.go#L103)

in server.go **newServer**

```
func newServer(listenAddrs []string, db database.Db, chainParams *chaincfg.Params) (*server, error)
```

sets up the **listenAddrs** which then get passed on to the

```
func (s *server) listenHandler(listener net.Listener) {
```

Note that listenHandler is the main listener which accepts incoming connections for the
server.  It must be run as a goroutine.  This is how the node communicates
with its Peers via the peer connections by setting up these connections in listenHandler.
