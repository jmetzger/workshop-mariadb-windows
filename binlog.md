# Binlog

## my.ini aktivieren (binlog) 

```
[mysqld]
# aktiviert binlog in Datenverzeichnis 
log-bin
```

```
Dienst neu starten
```

## Position abfragen, wohin als nächstes geschrieben

```
-- mysql>
show master status;
```
