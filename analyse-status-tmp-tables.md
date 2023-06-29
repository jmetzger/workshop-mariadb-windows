# Temporäre create_tmp_disk_tables herausfinden 

## Warum ? 

```
Temporäre Tabellen die auf die Platte geschrieben
create_tmp_disk_tables sind generell für die Performance schlecht
```

## Wie kann ich herausfinden, ob das bei mir auf meinem Server der Fall ist ?

```
show global status like '%Created_tmp_disk_tables%';
show global status like '%Created_tmp_files%';
```

## Wie kann ich herausfinde, welche Queries das genau sind ?

  * Information steht bei mariadb im slow_query_log 
