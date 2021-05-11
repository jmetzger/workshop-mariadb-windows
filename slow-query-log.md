# Slow Query Log

## Variante 1: Aktivieren (minimum) 

```
# auch direkt in 50-server.cnf möglich 
mysql>set global long_query_time=0.5 # 0,5 Sekunden. Alles was >= 0,5 sekunden dauert, wird geloggt 
mysql>set session long_query_time=0.5
mysql>set global slow_query_log=1 
mysql>set session slow_query_log=1 
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

## Ref: 

 * https://mariadb.com/kb/en/slow-query-log-overview/
