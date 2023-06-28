# MySQL vs. MariaDB

## Was ist gleich ? 

  * Gleiche CodeBasis weil Kopie
  * gleiche Tools (weitesgehend) 

## Was ist anders ? 

 * Andere Storage Engine sind möglich
 * physische Onlinebackup ist mit drin in der Community Version (mariabackup)
   * ein absolutes Muss für grosse Datenbestände (Geschwindigkeit ist wesentlich schneller beim zurückspielen
 * Langsame Abfragen protokollieren lassen (hier habt ihr in MariaDB noch mehr Ausgabemöglichkeiten)

## Was ist anders ? (MySQL) 

 * ab MySQL 8 - die Server Konfiguration während der Laufzeit setzen und persistent ändern
