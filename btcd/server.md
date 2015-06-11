
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
