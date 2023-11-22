# Database Checking  / Repair / Optimize 

## Check / Repair 

### InnoDB 

  * Automatic crash_recovery_mode triggered on startup
  * Only if you have no backup and nothing else works:
    * https://mariadb.com/kb/en/innodb-recovery-modes/

### MyISAM / Aria 

  * https://mariadb.com/kb/en/repair-table/ (online) 
  * https://mariadb.com/kb/en/aria_chk/ (offline)

## Optimize 

### InnoDB 

  * Attention: Recreates table -> expensive 
  * https://mariadb.com/kb/en/optimize-table/

```
use sakila;
optimize table actor;
```

### Aria 

  * https://mariadb.com/kb/en/optimize-table/
