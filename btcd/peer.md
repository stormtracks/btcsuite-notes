peer provides a bitcoin peer for handling bitcoin communications.  The
overall data flow is split into 3 goroutines and a separate block manager.

The 3 goroutines are
* inHandler
* outHandler
* queueHandler

Inbound messages are read via the inHandler go routine and generally
dispatched to their own handler.  For inbound data-related messages such as blocks, transactions, and inventory, the data is passed on to the block
manager to handle it.

Outbound messages are queued via QueueMessage or QueueInventory.  
QueueMessage is intended for all messages, including responses to data such as blocks and transactions.  QueueInventory, on the other hand, is only intended for relaying inventory as it employs a trickling mechanism to batch the inventory together.  

The data flow for outbound messages uses two goroutines, queueHandler and outHandler.  The first, queueHandler, is used as a way for external entities (mainly block manager) to queue messages quickly regardless of whether the peer is currently sending or not.  It acts as the traffic cop between the external world and the actual goroutine which writes to the network socket.  In addition, the peer contains several functions which are of the form pushX, that are used to push messages to the peer.  Internally they use QueueMessage.
