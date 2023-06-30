# Slow Query Log

## General 

  * Slow Query logs is activated with slow_query_log either in my.ini or as with set global
  * But it only triggers when the time is given correctly
    * Default: 10 (only queries slower than 10 seconds are recorded) 

## Easiest way to activate during runtime 

```
# in mysql - client
set global slow_query_log = 1;
show variables like '%slow%';


```




## Variante 1: Aktivieren (minimum) 

```
# auch direkt in 50-server.cnf möglich 
mysql>set global long_query_time=0.5 # 0,5 Sekunden. Alles was >= 0,5 sekunden dauert, wird geloggt 
mysql>set session long_query_time=0.5
mysql>set global slow_query_log=1 

```

## Logge alles wo kein Index verwendet werden kann (egal) wie langsam oder schnell 

```
# damit er wirklich nur die queries logged, die keinen index haben, sollte. der 
# long_query_time - Wert möglichst hoch sein. 
set global long_query_time = 20 
set session long_query_time = 20
set global slow_query_log = 1
set session slow_query_log = 1 
set global log_queries_not_using_indexes = 1
set session log_queries_not_using_indexes = 1 

```

## Bitte slow_query_log bei der ausgabe geschätziger zu sein

```
set global log_slow_verbosity = 'query_plan,explain'
set session log_slow_verbosity = 'query_plan,explain'

```

## Die Anzahl der Ausgabe reduzieren (nur jedes 5.) 

```
## /etc/mysql/mariadb-conf.d/50-server.cnf und mysqld 
log-slow-rate-limit=5;
```

## Best - Practice - Phase 1 

```
# Alle Logs analysieren, die kein Index verwendet 
#/etc/mysql/mariadb.conf.d/50-server.cnf 
# unter [mysqld]

# slow query log 
slow-query-log
log-queries-not-using-indexes
log-slow-rate-limit=5
log-slow-verbosity = 'query_plan,explain'
```


## Ref: 

 * https://mariadb.com/kb/en/slow-query-log-overview/
