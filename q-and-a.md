# Questions and answers.


## 1. Archive Data 

```

https://www.percona.com/doc/percona-toolkit/LATEST/pt-archiver.html
```

## 2. Does innodb do defragmentation by itself ?

```
# Some background while doing research.
# Nil performance benefits of defragmentation in index.
https://stackoverflow.com/questions/48569979/mariadb-table-defragmentation-using-optimize
```

## 3. Defragmentation 

```
# Optimize table 
ALTER TABLE contributions engine = InnoDB 


# mariadb has a patch for defragmentation  
https://mariadb.org/defragmenting-unused-space-on-innodb-tablespace/

# alter table xyz engine=InnoDB - defragements 
# but is also invasive.
# with ibdata1 innodb_file_per_table it lets the size grow


```

## 4. Is it possible to do select, update, deletes without using innodb_buffer in specific 

```
No, this is not possible 
```

## 8. MariaDB (Features/Vorteile)

  * flashback 
  * Verschlüsselung von Tabellen // mariabackup 
  * Einige Storage Engine (Aria -> MyISAM - crash-recovery) 
  * JSON anders implementiert 
  * galera 
  * feature: defragementation 
  
  ```
  MysqL 8 does not:
  decode 
  set profiling (still available but deprecated )
  ```
  
## 9. Select without locking 

  ``` 
  SET TRANSACTION ISOLATION LEVEL READ UNCOMMITTED ;
  BEGIN ;
  SELECT * FROM TABLE_NAME ;
  COMMIT ;
  ```

