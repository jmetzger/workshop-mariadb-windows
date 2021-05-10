# Show server/session status 

## with mysql -> show status 

```
mysql> show status;
-- global status für den gesamten Server seit er läuft 
mysql> show global status;
mysql> # setzt session status zurück 
mysql> flush status; 
mysql> show status;
```

## Spezielle status variablen 

```
show status like 'Com%';
show status like 'Com_select ';

```

## Aus information_schema 

```
select * from information_schema.global_status;
select * from information_schema.session_status;
```
