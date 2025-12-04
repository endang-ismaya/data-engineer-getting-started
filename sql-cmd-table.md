## Create Database 'electronic_store'
```sql
postgres=# CREATE DATABASE electronic_store;
CREATE DATABASE
postgres=#
postgres=# \c electronic_store
You are now connected to database "electronic_store" as user "postgres".
electronic_store=#
```

## Create Table employee
```sql
CREATE TABLE employee (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    date_of_birth DATE NOT NULL,
    email TEXT UNIQUE,
    phone VARCHAR(50) UNIQUE NOT NULL,
    active BOOLEAN NOT NULL,
    other_info TEXT DEFAULT 'no information'
);
```

## Show table
```sql
postgres=# \dt
          List of relations
 Schema |   Name   | Type  |  Owner
--------+----------+-------+----------
 public | employee | table | postgres
(1 row)

postgres=#
```