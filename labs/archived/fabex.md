---
layout: default
title: Fabex
parent: Archived Labs
---
# Lab Name
[Fabex](https://github.com/hyperledger-labs/fabex)

# Short Description
The aim of this tool is to provide microservice which augments and index the ledger of Hyperledger Fabric and to provide additional set of complex queries APIs to extract provenance information out of the ledger.

# Scope of Lab
Fabex exposes set of GRPC APIs to execute provenance queries over ledger data, moreover it provides an abstract DB interface allowing to integrate different DB engines, whereas out of box supported:

   - MongoDB

   - CassandraDB

DB storage interface:

```
type Manager interface {
	Connect() error
	Insert(Tx) error
	QueryBlockByHash(string) ([]Tx, error)
	GetByTxId(string) ([]Tx, error)
	GetByBlocknum(uint64) ([]Tx, error)
	GetBlockInfoByPayload(string) ([]Tx, error)
	QueryAll() ([]Tx, error)
	GetLastEntry() (Tx, error)
}
```

This tool could be integrated and deployed as a microservice, at the same time could be compiled into stand-alone command line tool.

# Initial Committers
- https://github.com/vadiminshakov
- https://github.com/Mikelle

# Sponsor
- https://github.com/C0rWin - HLF maintainer

# Pre-existing repository
- https://github.com/vadiminshakov/fabex
