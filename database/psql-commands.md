## A list of common psql commands that help you query data from the PostgreSQL database server faster and more effectively.

Connect to PostgreSQL database:
```
psql -U postgres
```
Switch connection to a new database:
```
\c dbname username
```
List available databases:
```
\l
```
List available tables:
```
\dt
```
Describe a table:
```
\d table_name
```
List available schema:
```
\dn
```
List available functions:
```
\df
```
List users and their roles:
```
\du
```
Command history:
```
\s
```
If you want to save the command history to a file:
```
\s filename
```
Execute psql commands from a file:
```
\i filename
```
Quit psql:
```
\q
```
