# SQL Table Operations

> Create a Table
```sql
CREATE TABLE {tableName} (
    {property} {type};
);
```

> Delete a Table
```sql
DROP TABLE {tableName};
```

> Insert into a Table
```sql
-- Implicit typing
INSERT INTO {tableName} VALUES ({...values});
```
`or`
```sql
-- Explicit typing
INSERT INTO {tableName} ({...rows}) VALUES ({...columns});
```

> Copy into a Table
```sql
COPY {tableName} from '{txtPath}';
```

> Delete from a Table
```sql
DELETE FROM {tableName} WHERE {qualifier};
```