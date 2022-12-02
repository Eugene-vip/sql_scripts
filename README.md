# sql_scripts
useful sql scripts

# Размер таблицы
```sql
select
    t.table_name
    ,pg_size_pretty(pg_total_relation_size(t.table_name))
from information_schema.tables t
where t.table_schema = 'table_schema_name'
    and t.table_catalog = 'database_name';
```

#Размер БД
```sql
select
    pd.datname
    ,pg_size_pretty(pg_database_size(pd.datname)) 
from pg_database pd;
```
