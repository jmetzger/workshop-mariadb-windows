# Database Rename 

# Walkthrough 

```
# im mysql - client 
create schema sakilanew
rename table sakila.actor to sakilanew.actor

# Attention, does not work views
# You have to dump and import views
# DOES NOT WORK BECAUSE OF VIEW
rename table sakila.actor_info to sakilanew.actor_info

# Also if there are triggers on a table it does not also not work.
# Eventually Delete triggers and set them again 
rename table sakila.film to sakilanew.film;
ERROR 1435 (HY000): Trigger in wrong schema
``` 
