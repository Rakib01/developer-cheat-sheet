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
# Insert Update Delete
```
INSERT INTO table1 (field1, field2) VALUES (value1, value2);
```
```
UPDATE table1 SET field1=new_value1 WHERE condition;
UPDATE table1, table2 SET field1=new_value1, field2=new_value2, ... WHERE
  table1.id1 = table2.id2 AND condition;
```
```
DELETE FROM table1 / TRUNCATE table1
DELETE FROM table1 WHERE condition
DELETE FROM table1, table2 FROM table1, table2 WHERE table1.id1 =
  table2.id2 AND condition
```

# Create / Delete / Modify Table

Create:
```
CREATE TABLE table (field1 type1, field2 type2);
```
```

CREATE TABLE table (field1 type1, field2 type2, INDEX (field));
```
```

CREATE TABLE table (field1 type1, field2 type2, PRIMARY KEY (field1));
```
```
CREATE TABLE table (field1 type1, field2 type2, PRIMARY KEY (field1,field2));
```
```
CREATE TABLE table1 (fk_field1 type1, field2 type2, ...,
  FOREIGN KEY (fk_field1) REFERENCES table2 (t2_fieldA))
    [ON UPDATE|ON DELETE] [CASCADE|SET NULL]
```
```

CREATE TABLE table1 (fk_field1 type1, fk_field2 type2, ...,
 FOREIGN KEY (fk_field1, fk_field2) REFERENCES table2 (t2_fieldA, t2_fieldB))
```
```

CREATE TABLE table IF NOT EXISTS;
```
```

CREATE TEMPORARY TABLE table;
```
Drop:
```
DROP TABLE table;
```
```

DROP TABLE IF EXISTS table;
```
```

DROP TABLE table1, table2, ...
```

Alter:
```

ALTER TABLE table MODIFY field1 type1
```
```

ALTER TABLE table MODIFY field1 type1 NOT NULL ...
```
```

ALTER TABLE table CHANGE old_name_field1 new_name_field1 type1
```
```

ALTER TABLE table CHANGE old_name_field1 new_name_field1 type1 NOT NULL ...
```
```

ALTER TABLE table ALTER field1 SET DEFAULT ...
```
```

ALTER TABLE table ALTER field1 DROP DEFAULT
```
```

ALTER TABLE table ADD new_name_field1 type1
```
```

ALTER TABLE table ADD new_name_field1 type1 FIRST
```
```

ALTER TABLE table ADD new_name_field1 type1 AFTER another_field
```
```

ALTER TABLE table DROP field1
```
```

ALTER TABLE table ADD INDEX (field);
```
Change field order:
```

ALTER TABLE table MODIFY field1 type1 FIRST
```
```

ALTER TABLE table MODIFY field1 type1 AFTER another_field
```
```

ALTER TABLE table CHANGE old_name_field1 new_name_field1 type1 FIRST
```
```

ALTER TABLE table CHANGE old_name_field1 new_name_field1 type1 AFTER
  another_field
```
# Users and Privileges
```
CREATE USER 'user'@'localhost';
```
```
GRANT ALL PRIVILEGES ON base.* TO 'user'@'localhost' IDENTIFIED BY 'password';
```
```
GRANT SELECT, INSERT, DELETE ON base.* TO 'user'@'localhost' IDENTIFIED BY 'password';
```
```
REVOKE ALL PRIVILEGES ON base.* FROM 'user'@'host'; -- one permission only
```
```
REVOKE ALL PRIVILEGES, GRANT OPTION FROM 'user'@'host'; -- all permissions
```
```
FLUSH PRIVILEGES;
```
```
SET PASSWORD = PASSWORD('new_pass');
```
```
SET PASSWORD FOR 'user'@'host' = PASSWORD('new_pass');
```
```
SET PASSWORD = OLD_PASSWORD('new_pass');
```
```
DROP USER 'user'@'host';
```
# Reset Root Password
```
$ /etc/init.d/mysql stop
```
```
$ mysqld_safe --skip-grant-tables
```
```
$ mysql # on another terminal
```
```
mysql> UPDATE mysql.user SET password=PASSWORD('new_pass') WHERE user='root';
```
```
## Switch back to the mysqld_safe terminal and kill the process using Control + \
$ /etc/init.d/mysql start
```