## Create Table
```sql
CREATE TABLE customers (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age SMALLINT CHECK (age>17),
    email TEXT UNIQUE NOT NULL,
    address TEXT DEFAULT 'no address'
);
```

