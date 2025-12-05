## Create Table employee

```sql
CREATE TABLE employee (
    id SMALLINT,
    name VARCHAR(100),
    date_joined DATE,
    active BOOLEAN
);
```

```bash
electronic_store=#
electronic_store=# CREATE TABLE employee (
    id SMALLINT,
    name VARCHAR(100),
    date_joined DATE,
    active BOOLEAN
);
CREATE TABLE
electronic_store=#
```

## show detail table
```sql
electronic_store=# \d employee
                        Table "public.employee"
   Column    |          Type          | Collation | Nullable | Default
-------------+------------------------+-----------+----------+---------
 id          | smallint               |           |          |
 name        | character varying(100) |           |          |
 date_joined | date                   |           |          |
 active      | boolean                |           |          |

electronic_store=#
```

## Insert Data
#### Commands
```sql
INSERT INTO employee (id, name, date_joined, active) VALUES 
    (1, 'Andi Pratama', '2022-03-15', TRUE),
    (2, 'Budi Santoso', '2021-07-10', TRUE),
    (3, 'Citra Lestari', '2020-12-05', FALSE),
    (4, 'Deni Kurniawan', '2023-01-20', TRUE),
    (5, 'Eka Wulandari', '2019-09-25', TRUE);
```
#### Terminal
```bash
electronic_store=#
electronic_store=# INSERT INTO employee (id, name, date_joined, active) VALUES
    (1, 'Andi Pratama', '2022-03-15', TRUE),
    (2, 'Budi Santoso', '2021-07-10', TRUE),
    (3, 'Citra Lestari', '2020-12-05', FALSE),
    (4, 'Deni Kurniawan', '2023-01-20', TRUE),
    (5, 'Eka Wulandari', '2019-09-25', TRUE);
INSERT 0 5
electronic_store=#
```

## Show Data
```sql
electronic_store=# SELECT * FROM employee;
 id |      name      | date_joined | active
----+----------------+-------------+--------
  1 | Andi Pratama   | 2022-03-15  | t
  2 | Budi Santoso   | 2021-07-10  | t
  3 | Citra Lestari  | 2020-12-05  | f
  4 | Deni Kurniawan | 2023-01-20  | t
  5 | Eka Wulandari  | 2019-09-25  | t
(5 rows)

electronic_store=#
```