# Materialized Views 

A cross between a table and a view. Unlike a view, it has table storage and can have its own indexes and so on.
Useful for caching. 

```sql
postgres=# CREATE MATERIALIZED VIEW aam AS SELECT * FROM aa WHERE a <= 500000;
```

[Postgres 9.3 feature highlight: Materialized views] [1]

[1]: http://michael.otacoo.com/postgresql-2/postgres-9-3-feature-highlight-materialized-views/
