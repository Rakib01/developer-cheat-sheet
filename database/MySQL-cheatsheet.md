# Create / Open / Delete Database
```
CREATE DATABASE DatabaseName;
```
```

CREATE DATABASE DatabaseName CHARACTER SET utf8;
```
```

USE DatabaseName;
```
```

DROP DATABASE DatabaseName;
```
```

ALTER DATABASE DatabaseName CHARACTER SET utf8;
```

# Browsing
```
SHOW DATABASES;
```
```
SHOW TABLES;
```

```
SHOW FIELDS FROM table / DESCRIBE table;
```
```

SHOW CREATE TABLE table;
```
```

SHOW PROCESSLIST;
```
```

KILL process_number;
```

# Select
```
SELECT * FROM table;
```
```

SELECT * FROM table1, table2;
```
```

SELECT field1, field2 FROM table1, table2;
```
```

SELECT ... FROM ... WHERE condition
```
```

SELECT ... FROM ... WHERE condition GROUPBY field;
```
```

SELECT ... FROM ... WHERE condition GROUPBY field HAVING condition2;
```
```

SELECT ... FROM ... WHERE condition ORDER BY field1, field2;
```
```

SELECT ... FROM ... WHERE condition ORDER BY field1, field2 DESC;
```
```

SELECT ... FROM ... WHERE condition LIMIT 10;
```
```

SELECT DISTINCT field1 FROM ...
```
```

SELECT DISTINCT field1, field2 FROM ...
```

# Backup Database to SQL File
```
mysqldump -u Username -p dbNameYouWant > databasename_backup.sql
```
# Restore from backup SQL File
```
mysql - u Username -p dbNameYouWant < databasename_backup.sql;
```