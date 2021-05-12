# 3-Schritte der Projekt-Optimierung (Performance) 

## Schritt 1: Hardware 

```
1) Arbeitsspeicher erhöhen/nachkaufen und mindestens 50% der Nutzdaten 
2) Extra Maschine für Applikation und für Datenbank (möglichst gute Anbindung untereinander)
   d.h. Maschinen stecken am besten gleichen Serverschrank 
```

## Schritt 2: Konfiguration 

  1. [Optimierung des InnoDB Buffers (Größe)](innodb/innodb.md) 
  1. [innodb_flush_log_at_trx_commit](innodb/innodb.md) auf 0 setzen (jede Sekunde statt bei jedem Commit) 

## Schritt 3: Optimierung der Anfragen 

  1. [Vorbereitung Ausgabe Slow Log für die Analyse](slow-query-log.md)
  1. [Installation percona-toolkit](tools/percona-toolkit.md)
  1. [Analyse slow-log-file mit pt-query-digest](tools/pt-query-digest.md)

## Extra: Der Ausweg bei großen Tabellen 

  1. Falls es keine andere LÖsung gibt, könnte u.U. Partitionierung helfen. [Hier](partitions/partitions-explain.md)
