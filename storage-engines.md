# Storage Engines 

## Why ?

```
Let's you choose:
How your data is stored
```

## What ?

  * Performance, features and other characteristics you want

## Where ? 

  * Theoretically you can use a different engine for every table 
  * But: For performance optimization and future, it is better to concentrate on one 

## What do they do ?

  * In charge for: Responsible for storing and retrieving all data stored in MySQL
  * Each storage engine has its:
    * Drawbacks and benefits
  * Server communicates with them through the storage engine API 
    * this interface hides differences
    * makes them largely transparent at query layer
    * api contains a couple of dozen low-level functions e.g. “begin a transaction”, “fetch the row that has this primary key”

## Storage Engine do not ....

  * Storage Engines do not parse SQL
  * Storage Engines do not communicate with each other

## They simply .....

  * They simply respond to requests from the server

## Which are the most important one ?

  * InnoDB (currently default engine) 
  * MyISAM/Aria
  * Memory
  * CSV
  * Blackhole (/dev/null)
  * Archive
  * Partition
  * (Federated/FederatedX)

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
4. row-level locking (only single lines are locked)
5. multi-versioning
```


