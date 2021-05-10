# User verwalten 

```
# bitte nur im Notfall von überall
# + passworr im klartext 
mysql>create user training@'%' identified by 'meingeheimespasswort'  
mysql>create user training@192.168.2.2; -- von einer bestimmten ip ausschliesslich // ip des zugreifers

# Rechte vergeben *.* -> alle datenbanken.alle tabellen 
# to -> für. 
mysql>grant all on *.* to training@192.168.2.2 
# Rechte entziehn 
mysql>revoke select on *.* from training@192.168.2.2 
# oder alle Rechte enziehen 
mysql>revoke all on *.* from training@192.168.2.2 

# Rechte eines Benutzers anschauen 
mysql>show grants for training@192.168.2.2. // genaue Kombination muss angegeben werden 

# Eigentlich nicht notwendig, aber geht 
mysql>select * from mysql.global_priv \G #  das geht nur im mysql-client und zeigt Spalten in Zeilen an
mysql>select * from mysql.user; 
```
