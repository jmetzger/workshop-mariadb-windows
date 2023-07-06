# Mariabackup 

## Installation 

```
Is done through MSI-Installer for MariaDB-Server
```

## Backup Walkthrough (Windows)

### Schritt 1: Backup erstellen 
```
# Command Prompt (mariadb)
# Backupfolder C:\Users\vgh-MariaDB\Desktop\Backups
# Going to parent folder 
cd C:\Users\vgh-MariaDB\Desktop\

 # target-dir needs to be empty or not present 
mariabackup -uroot -p<passwort-for-root> --target-dir=Backups/20230321 --backup 
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
```

```
2. Im Datenverzeichnis - altes Datenverzeichnis verschieben 
cd C:\Program Files\MariaDB 10.6\
rename data data.bkup

```

```
3. In das Elternverzeichnis von backup wechseln
cd C:\Users\vgh-MariaDB\Desktop
mariabackup --target-dir=Backups/20230321 --copy-back
3.5 my.ini in data - ordner reinkopieren (aus data.bkup ordner)
4. Rechte anpassen (NT Service\MariaDB) für den Ordner data -> Vollzugriff 
5. Dienst mariadb starten
```

