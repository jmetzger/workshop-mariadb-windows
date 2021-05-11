# Slow Query Log

## Aktivieren (minimum) 

```
# auch direkt in 50-server.cnf möglich 
mysql>set global long_query_time=0.5 # 0,5 Sekunden. Alles was >= 0,5 sekunden dauert, wird geloggt 
mysql>set session long_query_time=0.5
mysql>set global slow_query_log=1 
mysql>set session slow_query_log=1 
```

## Ref: 

 * https://mariadb.com/kb/en/slow-query-log-overview/
