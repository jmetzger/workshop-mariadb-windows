# Welche Logs gibt es ?

## general_log 

  * Alle Anfrage gegen den Server (Abgesetzte SQL-Statements)

## error_log 

   * Protokolliert nicht nur Fehler, sondern den kompletten Startup (auch warning und notes)
   * Log - Level kann angepasst werden (Standard: 2, in der Regel ausreichend)
     * log_error_verbosity 

## Ereignisprotokoll (Windows) 

  * Falls ich im error_log keinen ausreichenden Informationen finde, kann ich auch nochmal nachschauen.

## slow_query_log 

  * Langsame Queries die Bedingung long_query_time erfüllen, werden mitgeloggt, wenn eingeschaltet
    * im Datenverzeichnis unter *-slow - Datei 
