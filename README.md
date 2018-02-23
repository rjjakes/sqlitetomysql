
# sqlite3 to mysql

A simple Python script to convert sqlite dump files to MySQL for Drupal 8.

Based heavily on the script here (too all credit to those authors): 
http://www.redmine.org/boards/2/topics/12793?r=24999

Modified to convert SQLite dump files to MySQL for Drupal 8.

## Usage

Dump your SQLite database.:

```
sqlite3 site.sqlite .dump > dump.sql 
```

Convert to MySQL and pipe to a file:

```
./sqlite3-to-mysql.py dump.sql > dump-mysql.sql
``` 

Import to an empty MySQL database:

```
mysql -u someusername -psomepassword databasename < dump-mysql.sql
```

