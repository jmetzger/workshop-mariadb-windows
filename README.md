# Workshop MariaDB Windows 

## Agenda 

  1. Grundsätzliches
     * [Historie MySQL/MariaDB](historie-mysql-mariadb.md)
     * [Aufbau MariaDB](aufbau-mariadb.md)
     * [MySQL vs. MariaDB](mysql-vs-mariadb.md)
  1. Performance / Theorie - Aspekte der MariaDB - Architektur 
     * [Architektur Server (Schritte)](performance/mysql-server-architecture.md)
     * [CPU oder io-Last klären](top-cpu-io-load.md)
     * [Storage Engines](storage-engines.md) 
     * [InnoDB - Struktur](/innodb/innodb-structure.md)
     * [InnoDB - Optimierung](/innodb/innodb.md) 
     * [Query - Cache](/performance/query-cache.md)
     * [3-Phasen-Datengröße](3-phases-of-data-size-and-performance-impact.md)
  1. Performance / Konfiguration 
     * [Slow query log](slow-query-log.md) 
  1. Administration / Logging
     * [Standard storage engine bestimmen](default-storage-engine.md)
     * [Datenbank-Namen performant umbenennen](database-rename.md)
     * [Show status](show-status.md)
     * [Server System Variablen - show variables](show-variables.md)
     * [Arbeiten mit dem information_schema](working-with-information_schema.md)
     * [User verwalten](user.md)
     * [Einstellungsmöglichkeiten für ErrorLogs](https://mariadb.com/kb/en/error-log/)
  1. Backup und Restore
     * [Wann binlog ?](backups/binlogs-what-for.md)
     * [Backup with mysqldump - best practices](backup-restore/mysqldump.md)
     * [PIT Exercise - point in time recovery](backup-restore/pit-exercise.md)
     * [Mariabackup](backup-restore/mariadbackup.md)
  1. Performance und Optimierung von SQL-Statements
     * [Performance tmp_disk_tables problem](/performance/analyse-status-tmp-tables.md)
     * [Explain verwenden](/indexes/explain.md)
     * [Do not use '*' whenever possible](/performance/select-no-star-please.md) 
     * [Indexes](indexes/index.md)
     * [profiling-get-time-for-execution-of.query](/indexes/profiling.md)
     * [Kein function in where verwenden](/performance/no-function-in-where.md)
     * [Optimizer-hints (and why you should not use them)](performance/optimizer-hints.md)
     * [Query-Plans aka Explains](performance/query-plans.md)
     * [Query Pläne und die Key-Länge](query-plans-explain-keylen.md)
     * [Index und Likes](indexes/like-index-not-index.md)
     * [Index und Joins](indexes/join-index.md)
     * [Find out cardinality without index](/indexes/cardinality.md)
     * [Index and Functions](index-and-functions.md) 
  1. Tools 
     * [Percona Toolkit - only pt-query-digest](/tools/percona-toolkit.md) 
     * [pt-query-digest - analyze slow logs](/tools/pt-query-digest.md)
     * [pt-online-schema-change howto](/tools/pt-online-schema-change.md)
     * [Example sys-schema and Reference](/tools/sys.md)
  1. Beispieldaten
     * [Verleihdatenbank - sakila](sakila.md)
     * [Setup training data "contributions"](/indexes/setup-training-data-contributions.md)
  1. Managing big tables 
     * [Using Partitions - Walkthrough](partitions/partitions-explain.md)
  1. Replication
     * [Aufbau Master/Slave - Replication](replication/auf-master-slave.md)
     * [Replikation mit GTID](replication/01-master-slave-gtid.md)
     * [Replikation Read/Write - Split: ](https://proxysql.com/blog/configure-read-write-split/)
  1. MariaDB (Galera Cluster) - Linux Only !!
     * [Aufbau Galera Cluster](galera/aufbau-galera.md)
  1. Fragen und Antworten 
     * [Fragen und Antworten](q-and-a.md)
  1. Projektarbeit/-optimierung 
     * [Praktisch Umsetzung in 3-Schritten](project-3-steps.md)
  1. Dokumentation 
     * [MySQL - Performance - PDF](http://schulung.t3isp.de/documents/pdfs/mysql/mysql-performance.pdf)
     * [Effective MySQL](https://www.amazon.com/Effective-MySQL-Optimizing-Statements-Oracle/dp/0071782796)
     * [MariaDB Downloaden](https://mariadb.org/download/)
     * [MariaDB - Releases - including long - term releases](https://mariadb.com/kb/en/mariadb-server-release-dates/)       
     

