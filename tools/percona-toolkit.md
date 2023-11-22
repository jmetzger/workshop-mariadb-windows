# Install percona - toolkit (only pt-query-digest)

## Walkthrough (Windows) 

```
# 1. Install strawberry perl 
https://strawberryperl.com/

# 2. Download pt-query-digest and save with .pl suffix
https://www.percona.com/get/pt-query-digest

# 3. copy file to bin - folder of mariadb

# 4. Open mariadb Command Prompt as ADMINISTRATOR 
# Navigate to data - dir

# 5. as Admin: Execute once to get right connection to perl
pt-query-digest.pl <name-of-slow-query-log> > analyse.txt

# 6. once more  5.
pt-query-digest.pl <name-of-slow-query-log> > analyse.txt

# 7. Digest analyse.txt and be happy or not ;o)

# Referenz
# http://www.jonathanlevin.co.uk/2012/01/query-digest-on-windows.html
```


