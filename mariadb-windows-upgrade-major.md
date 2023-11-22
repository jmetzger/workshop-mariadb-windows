# Mariadb (Windows) Upgrade Major (e.g. 10.6 - 10.11) 

## Steps 

```
1. Install new version, while still retaining the old one
2. Stop old service 
3. Upgrade services one by one, like described later in the document (e.g with mysql_upgrade_service). It is recommeded to have services cleanly shut down before the upgrade.
4. Uninstall old version when previous step is done.
```

## Reference 

https://mariadb.com/kb/en/upgrading-mariadb-on-windows/
