# Troubleshooting Windows 

## Übersicht: Was sind typische Szenarien ? 

  * Server stoppt plötzlich und startet nicht mehr
    * Dienst will garnicht starten (Windows)
    * Server fängt an zu starten, bricht aber ab (Error) 
  * Dienst/Server startet nach Aufsetzen nicht.
  * Bestimmte Features funktionieren nicht
  * Verbindung zum Server funktioniert nicht

## 1. Server stoppt plötzlich und startet nicht mehr 

### 1.1 Dienst will garnicht starten (Windows) 

  * Oftmals deutet dies auf einen Berechtigungsproblem hin

#### Lösung: Was sagt die Ereignisanzeige 

  * Ereignisanzeige -> Windows-Protokolle -> Anwendung (jetzt kann man rechts nach mariadb suchen)

### 1.2 Server fängt an zu starten, bricht aber ab (Error) 

   * Es ist wichtig, herauszufinden, ob es Fehler im error-log gibt

#### Lösung: Error-log (liegt im Datenverzeichnis mit Endung .err analysieren

   * Hier kann man nach Eintragen mit [Error] schauen.

## 2. Dienst/Server startet nach Aufsetzen nicht 

### Lösung: Entweder Probleme Rechte oder es fehlen Dateien 

  * Analyse 1.1. und 1.2.

## 3. Bestimmte Features funktionieren nicht

  * Fehler im error-log (Analyse 1.2)
  * Wird entsprechend notwendiges Plugin geladen
    * show plugins;

## 4. Verbindung zum Server funktioniert nicht 

### Lösung 
  * Analyse Error-log (1.2.)
  * Es kann z.B. ein Hinweis darauf sein, dass Max-Connections erlaubt.

### Lösung 2: 
  * Schrittweises Debuggen:
    1. Verbindung zum Server und Port möglich ? (z.B. mit telnet oder mit mysqladmin ping
    1. Falls ich lokal drauf komme: Ist der User richtig eingerichet.(HeidiSQL) 
    1. Falls ich lokal drauf komme: (Habe ich Berechtigungen zur Datenbank)
