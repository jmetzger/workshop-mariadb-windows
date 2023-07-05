# Working with the information schema 

```
-- im mysql - client
use information_schema;
show tables;
select * from global_variables \G
-- show all buffer vars
select * from global_variables like variable_name like '%buffer%';
```
