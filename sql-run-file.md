## Create Table customers
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


## Create Table products
```sql
CREATE TABLE products (
    product_id SERIAL PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    brand VARCHAR(50),
    price DECIMAL(10,2) NOT NULL,
    in_stock BOOLEAN NOT NULL DEFAULT TRUE
);
```

## Copy products into docker container
```bash
❯ docker cp data_sql/products.sql belajar-sql-postgresql:/tmp/products.sql
Successfully copied 12.8kB to belajar-sql-postgresql:/tmp/products.sql
```

## Run thru psql
```sql
\i /tmp/products.sql
```
