# Mariabackup 

## Installation 

```
Is done through MSI-Installer for MariaDB-Server
```

## Walkthrough (Ubuntu/Debian)

### Schritt 1: Backup erstellen 
```
# Backupfolder
C:\Users\vgh-MariaDB
md Backups

 # target-dir needs to be empty or not present 
mariabackup -uroot -p --target-dir=Backups/20230321 --backup 
```

### Schritt 2:  

```
# apply ib_logfile0 to tablespaces 
# after that ib_logfile0 ->  0 bytes 
mariabackup --target-dir=Backups/20230321 --prepare 
```

## Recover 
systemctl stop mariadb 
mv /var/lib/mysql /var/lib/mysql.bkup 
mariabackup --target-dir=/backups/20230321 --copy-back 
chown -R mysql:mysql /var/lib/mysql
chmod 755 /var/lib/mysql # otherwice socket for unprivileged user does not work
systemctl start mariadb 
```

## Walkthrough (Redhat/Centos/Rocky Linux 8 mit mariadb for mariadb.org)

```
# user eintrag in /root/.my.cnf
[mariabackup]
user=root 
# pass is not needed here, because we have the user root with unix_socket - auth 
# or generic 
# /etc/my.cnf.d/mariabackup.cnf
[mariabackup]
user=root

mkdir /backups 
# target-dir needs to be empty or not present 
mariabackup --target-dir=/backups/20210120 --backup 
# apply ib_logfile0 to tablespaces 
# after that ib_logfile0 ->  0 bytes 
mariabackup --target-dir=/backups/20210120 --prepare 

## Recover 
systemctl stop mariadb 
mv /var/lib/mysql /var/lib/mysql.bkup 
mariabackup --target-dir=/backups/20200120 --copy-back 
chown -R mysql:mysql /var/lib/mysql
chmod 755 /var/lib/mysql # otherwice socket for unprivileged user does not work
systemctl start mariadb 

## important for selinux if it does not work 
## does not start
restorecon -vr /var/lib/mysql 
systemctl start mariadb 
```
