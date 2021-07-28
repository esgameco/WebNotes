# SQL Language Basics

[Docs](https://www.postgresql.org/docs/13/sql.html)

## Concepts

- Relational == Tabular
- Columns are ordered, rows are not
- A sql database is a collection of tables

## Syntax

- Semicolon-terminated
- Extra whitespace ignored
- `--` designates the rest of a line to be a comment
- Strings are c-like -- they are an array of chars called `varchar`
- `real` == float

## Table Operations

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

## Table Queries

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