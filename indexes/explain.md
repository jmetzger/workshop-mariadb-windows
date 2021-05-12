# Explain verwenden 

## Einfacher Fall 

```
explain select * from actor 
```

## Erweiterter Fall
```
explain extended select * from user 
show warnings 
```

## Anzeigen der Partitions 

```
explain partitions select * from actor 
```


## Ausgabe im JSON-Format 

```
# Hier gibt es noch zusätzliche Informationen 
explain format=json select * from actor 
```
