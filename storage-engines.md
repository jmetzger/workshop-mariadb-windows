# Storage Engines 

## In Detail: MyISAM - Storage Engine

```
1. table locks → Locks are done table-wide
2. no automatic data-recovery (Aria hat das !) 
3. you can loose more data on crashes than with e.g. InnoDB
4. no transactions
5. only indices are save in memory through MySQL
6. compact saving (data is saved really dense)
7. table scans are quick
```

## In Detail: InnoDB - Storage Engine

```
1. support hot backups (because of transactions)
2. transactions are supported
3. foreign keys are supported
4. row-level locking
5. multi-versioning
```

## Welches sind die wichtigsten ? 

```
MyISAM/Aria
InnoDB
Memory
CSV 
Blackhole (/dev/null) 
Archive 
FederatedX 
```

