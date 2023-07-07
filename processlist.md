# Processlist 

## Prozesse (Threads) 

## Über show 

```
show processlist;
```

## Über information_schema 

```
select * from information_schema.processlist;
-- oder
use information_schema;
select * from processlist;
```

## Process beenden

```
-- kill <thread_id-die-wir-über-die-processliste-sehen>
-- z.B.
kill 314 
```
