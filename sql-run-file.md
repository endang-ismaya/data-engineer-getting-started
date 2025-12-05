## Create Table
```sql
create table customers (
	customer_id SERIAL PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	date_of_birth DATE NOT NULL,
	gender VARCHAR(50) NOT NULL,
	city VARCHAR(15) NOT NULL,
	email VARCHAR(50) UNIQUE,
	phone VARCHAR(50)
);
```

## Copy file customers.sql into docker container
```bash
docker cp customers.sql belajar-sql-postgresql:/tmp/customers.sql
```
```bash
❯ docker cp data_sql/customers.sql belajar-sql-postgresql:/tmp/customers.sql
Successfully copied 45.1kB to belajar-sql-postgresql:/tmp/customers.sql
❯
```

## Run thru psql
```sql
\i /tmp/customers.sql
```