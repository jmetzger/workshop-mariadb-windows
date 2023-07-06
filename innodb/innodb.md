# InnoDB 

## Innodb buffer pool

  * How much data fits into memory 
  * Free buffers = pages of 16 Kbytes 
  * Free buffer * 16Kbytes = free innodb buffer pool in KByte  

## How to find out ?

```
# OR: 
MariaDB [(none)]> show status like '%free%';
+-------------------------------+---------+
| Variable_name                 | Value   |
+-------------------------------+---------+
| Innodb_buffer_pool_pages_free | 48083   |
| Innodb_buffer_pool_wait_free  | 0       |
| Innodb_ibuf_free_list         | 0       |
| Qcache_free_blocks            | 1       |
| Qcache_free_memory            | 1031304 |
+-------------------------------+---------+
5 rows in set (0.002 sec)
```

## show engine innodb status 

```
# please use command line 
show engine innodb status \G

```

## Overview innodb server variables / settings 

  * https://dev.mysql.com/doc/refman/5.7/en/innodb-parameters.html

## Change innodb_buffer_pool 

```
# my.ini 
# 70-80% of memory on dedicated mysql
[mysqld]
innodb-buffer-pool-size=6G

# Dienst neu starten 

# 
mysql
mysql>show variables like 'innodb%buffer%';
```

## innodb_flush_method 

```
Ideally O_DIRECT on Linux, but please test it, if it really works well.
- no changes needed in Windows as we are using unbuffered  
```

## 	innodb_flush_log_at_trx_commit

```
When is fliushing done from innodb_log_buffer to log.
Default: 1 : After every commit 
-> best performance 2. -> once per second

# Good to use 2, if you are willing to loose 1 second of data on powerfail 
```

## innodb_flush_neighbors 

```
# on ssd disks set this to off, because there is no performance improvement 
innodb_flush_neighbors=0 

# Default = 1 

```

## skip-name-resolv 

```
# work only with ip's - better for performance 
/etc/my.cnf 
skip-name-resolve
```

  * https://nixcp.com/skip-name-resolve/


## Calculate innodb-log-file-size

```
-- Session 1: LSN abfragen 
-- in mysql client 
pager more;
-- Determine LSN from engine innodb status
--  Log sequence number 21879482
show engine innodb status \G 
select sleep(60);

```

```
# Session 2: Import ausführen (als Beispiel für es finden Veränderungen stand) 
# in command prompt (mariadb)
# ins backup verzeichnis wechseln
C:\Users\vgh-MariaDB\Desktop\Backups
# all-databases.sql einspielen 
mysql -uroot -p<mein password> < all-databases.sql 
```

```
# Wieder in Session 1
# Determine LSN #
# Log sequence number 22279482
pager more;
show engine innodb status \G
pager;
```

```
# letzter (2. Wert - 1.Wert) 
mysql> select (3838334638 - 3836410803) / 1024 / 1024 as MB_per_min;
+------------+
| MB_per_min |
+------------+
| 1.83471203 | 
+------------+
```

  * https://www.percona.com/blog/how-to-calculate-a-good-innodb-log-file-size/


## Ref:

  * https://dev.mysql.com/doc/refman/5.7/en/innodb-buffer-pool-resize.html
  

## Privilegs for show engine innodb status 

```
 show engine innodb status \G
ERROR 1227 (42000): Access denied; you need (at least one of) the PROCESS privilege(s) for this operation

```
