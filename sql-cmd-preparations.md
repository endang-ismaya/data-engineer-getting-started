# Preparation

1. Download or pull postgres image
```bash
docker pull postgres:17.4
```

2. Create and run container
```bash
docker run --name belajar-sql-postgresql -e POSTGRES_PASSWORD=secret -d postgres:17.4
```

3. Enter the container
```bash
docker exec -it belajar-sql-postgresql psql -U postgres
```


## SQL Commands
- Clear the terminal
```sql
\! clear;
```

- Quit the terminal
```sql
\q;
```

