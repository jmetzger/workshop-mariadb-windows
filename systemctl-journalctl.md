# Systemctl/journalctl (Server starten und stoppen etc. / Logs) 

```
systemctl TAB TAB -> zeigt alle Unterbefehle an
systemctl status mariadb.service 
systemctl start mariadb # .service darf man weglassen bei start/status/stop/restart 
systemctl stop mariadb 
systemctl restart  mariadb 
```

```
journalctl -u mariadb.service  # Zeigt alle Logs an seit dem letzten Serverstart (Debian 10)
```
