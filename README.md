# MariaDB Performance Training (deutsch)   

## Agenda 

  1. Performance / Theorie - Aspekte der MariaDB - Architektur 
     * [Architektur Server (Schritte)](performance/mysql-server-architecture.md)
     * [CPU oder io-Last klären](top-cpu-io-load.md)
     * [Storage Engines](storage-engines.md) 
     * [InnoDB - Struktur](/innodb/innodb-structure.md)
     * [InnoDB - Optimierung](/innodb/innodb.md) 
     * [Query - Cache](/performance/query-cache.md)
     * [3-Phasen-Datengröße](3-phases-of-data-size-and-performance-impact.md)
  1. Installation
     * [Installation (Debian)](installation-debian.md)
  1. Konfiguration 
     * [Slow query log](slow-query-log.md) 
  1. Administration 
     * [Standard storage engine bestimmen](default-storage-engine.md)
     * [Show status](show-status.md)
     * [Server System Variablen - show variables](show-variables.md)
     * [systemctl/jorunalctl - Server starten,stoppen/Logs](systemctl-journalctl.md) 
     * [User verwalten](user.md)
  1. Performance und Optimierung von SQL-Statements 
     * [Do not use '*' whenever possible](/performance/select-no-star-please.md) 
     * [Indexes](indexes/index.md)
     * [profiling-get-time-for-execution-of.query](/indexes/profiling.md)
     * [Kein function in where verwenden](no-function-in-where.md)
     * [Optimizer-hints (and why you should not use them)](performance/optimizer-hints.md)
     * [Query-Plans aka Explains](performance/query-plans.md)
     * 
  1. Tools 
     * [Percona Toolkit](/tools/percona-toolkit.md) 
     * [pt-query-digest - analyze slow logs](/tools/pt-query-digest.md)
     * [pt-online-schema-change howto](/tools/pt-online-schema-change.md)
     * [Example sys-schema and Reference](/tools/sys.md)
  1. Beispieldaten
     * [Verleihdatenbank - sakila](sakila.md)
     * [Setup training data "contributions"](/indexes/setup-training-data-contributions.md)
  1. Managing big tables 
     * [Using Partitions - Walkthrough](partitions/partitions-explain.md)
  1. Replication
     * Replikation mit GTID :: https://www.admin-magazin.de/Das-Heft/2017/02/MySQL-Replikation-mit-GTIDs
     * Replikation Read/Write - Split: https://proxysql.com/blog/configure-read-write-split/
  1. Dokumentation 
     * [MySQL - Performance - PDF](http://schulung.t3isp.de/documents/pdfs/mysql/mysql-performance.pdf)
     * [Effective MySQL](https://www.amazon.com/Effective-MySQL-Optimizing-Statements-Oracle/dp/0071782796)

## Agenda2 
  
  1. Diagnosis and measurement of performance 
     * [Best practices to narrow down performance problems](performance/best-practice-analyze.md
     
  1. Performance and optimization of SQL statements 
     * [Be aware of subselects - Example 1](/performance/subselects-1.md)
    
    
     
  1. Optimal use of indexes
     
     * Index-Types 
       * [Describe and indexes](/indexes/describe-table.md)
       * [Find out indexes](indexes/findout-indexes.md) 
     * [Index and Functions (Cool new feature in MySQL 5.7)](index-and-functions.md) 
     * [Index and Likes](/indexes/like-index-not-index.md)
    

     * [Find out cardinality without index](/indexes/cardinality.md)
         
  1. Performance 
     * [Best Practices](/performance/best-practices.md)
     * [Optimizer-Hints](performance/optimizer-hints.md) 
        
   
   1. [Questions and Answers](q-and-a.md)
    
   1. [mysql-do-nots](/performance/mysql-do-nots.md)
   
