
package database/ldb

#### block.go

* ExistsSha
* FetchBlockBySha
* FetchBlockHeightBySha
* FetchBlockHeaderBySha
* FetchBlockShaByHeight
* FetchHeightRange
* NewestSha
* FetchAddrIndexTip

#### tx.go

* InsertTx
* ExistsTxSha
* FetchTxByShaList
* FetchUnspentTxByShaList
* FetchTxBySha
* FetchTxsForAddr
* UpdateAddrIndexForBlock
* DeleteAddrIndex

#### leveldb.go

* InsertBlock
* DropAfterBlockBySha

* Sync
* RollbackClose
* Close
* OpenDB
* CreateDB
