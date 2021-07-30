# SQL Table Queries

> Default Select
```sql
SELECT {...columnNames} from {tableName};
```

> Select with Data Transformation
```sql
SELECT {transformation} from {tableName};
-- transformation example -> id + 2
```

> Select with Qualifiers
```sql
SELECT {...columnNames} from {tableName} where {qualifier};
-- qualifier example -> name = 'Joe',
--                   -> num  <  2
```

> Ordered Select
```sql
SELECT {...columnNames} from {tableName} ORDER BY {...columnNames};
```

> Select with No Duplicates
```sql
SELECT DISTINCT {...columnNames} from {tableName};
```