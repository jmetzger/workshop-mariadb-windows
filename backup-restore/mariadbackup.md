# Mariabackup 

## Installation 

```
Is done through MSI-Installer for MariaDB-Server
```

## Backup Walkthrough (Windows)

### Schritt 1: Backup erstellen 
```
# in der cmd.exe
# Backupfolder
cd C:\Users\vgh-MariaDB
md Backups

 # target-dir needs to be empty or not present 
mariabackup -uroot -p<passwort for root> --target-dir=Backups/20230321 --backup 
```

### Schritt 2:  Prepare durchführen (Änderung für Tablespaces anwenden) 

```
# apply ib_logfile0 to tablespaces 
# after that ib_logfile0 ->  0 bytes 
mariabackup --target-dir=Backups/20230321 --prepare 
```

## Recover Walkhrough  

```
1. Dienst mariadb stoppen 
2. altes Datenverzeichnis move (n) mysql mysql.bkup 
3. In das Elternverzeichnis von backup wechseln
cd C:\Users\vgh-MariaDB
mariabackup --target-dir=Backups/20230321 --copy-back 
4. Rechte anpassen (NTService\MariaDB) 
5. Dienst mariadb starten
```

