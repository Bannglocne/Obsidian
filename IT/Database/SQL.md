```sql
SELECT column1, column2, ... FROM table_name;
SELECT * FROM table_name; /*Select all*/

SELECT DISTINCT column1  FROM table_name; /*Select distinct (different) values.*/
SELECT COUNT(DISTINCT column1) FROM table_name;
```

# Conditions
**WHERE**
```sql
SELECT column1 FROM table_name WHERE (NOT) condition1 AND|OR condition2; /*=, >, <, >=, <=, <>, BETWEEN, LIKE, IN*/
```

**HAVING**
```sql
SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) HAVING condition ORDER BY column_name(s);
```

**EXISTS**
```sql
SELECT column_name(s) FROM table_name WHERE EXISTS (SELECT column_name FROM table_name WHERE condition);
```

**ORDER BY**
```sql
SELECT column1 FROM table_name ORDER BY column1 ASC|DESC;
```

**LIKE**
- `_`: Single character
- `%`: Any number of characters
	- End: Starts with
	- Beginning: Ends with
	- Before and After: Contains

**CASE**
```sql
CASE
	WHEN condition1 THEN result1
	WHEN condition2 THEN result2
	WHEN conditionN THEN resultN
	ELSE result
END;
```
# Select
**SELECT**: MySQL Syntax
```sql
SELECT column_name(s) FROM table_name WHERE condition LIMIT number;
```

**SELECT INTO**
```sql
SELECT * INTO newtable [IN externaldb] FROM oldtable WHERE condition;
SELECT column1, column2, column3, ... INTO newtable [IN externaldb] FROM oldtable WHERE condition;
```

**AS**
```sql
SELECT column_name AS alias_nam FROM table_name;
SELECT column_name(s) FROM table_name AS alias_name;
/*Space Character: [Ha Ha Ha]*/
```

**GROUP BY**
```sql
SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) ORDER BY column_name(s);
```

**ANY**
```sql
ELECT column_name(s) FROM table_name WHERE column_name operator ANY (SELECT column_name FROM table_name WHERE condition);
```

**ALL**
```sql
SELECT ALL column_name(s) FROM table_name WHERE condition;
SELECT column_name(s) FROM table_name WHERE column_name operator ALL (SELECT column_name FROM table_name WHERE condition);
```

# Update
**INSERT INTO**
```sql
INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2,...);
```

**UPDATE**
```sql
UPDATE table_name SET column1 = value1, column2 = value2, ...  WHERE condition;
```

**DELETE**
```sql
DELETE FROM table_name WHERE condition;
```

**JOIN**
```sql
SELECT column_name(s)FROM table1 
INNER|LEFT|RIGHT|FULL OUTER JOIN table2 ON table1.column_name = table2.column_name;
```

**UNION**
```sql
SELECT column_name(s) FROM table1 UNION (ALL) SELECT column_name(s) FROM table2;
```

# Values
**NULL**
```sql
WHERE Address IS (NOT) NULL;
```

# Functions
**MIN / MAX**
```sql
SELECT MIN|MAX(column_name)  FROM table_name WHERE condition;
```

**COUNT**
```sql
SELECT COUNT( (DISTINCT) column_name) FROM table_name WHERE condition;
```

**SUM**
```sql
SELECT SUM(column_name) FROM table_name WHERE condition;
```

**AVERAGE**
```sql
SELECT AVG(column_name) FROM table_name WHERE condition;
```

**STORED PROCEDURE**
```sql
CREATE PROCEDURE procedure_name AS sql_statement GO;

EXEC procedure_name;
```

# DATABASE
```sql
CREATE DATABASE databasename;

DROP DATABASE databasename;

BACKUP DATABASE databasename TO DISK = 'filepath';
```

**CREATE TABLE**
```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
   ....
);

CREATE TABLE new_table_name AS
    SELECT column1, column2,...
    FROM existing_table_name
    WHERE ....;
```

**ALTER TABLE**
```sql
DROP TABLE table_name;

--Delete the data inside a table, but not the table itself
TRUNCATE TABLE table_name;

-- Add, delete, or modify columns in an existing table.
ALTER TABLE table_name ADD column_name datatype;
ALTER TABLE table_name DROP COLUMN column_name;
ALTER TABLE table_name RENAME COLUMN old_name to new_name;
ALTER TABLE table_name ALTER COLUMN column_name datatype;
```

**CONSTRAINT**
```sql
-- Specify rules for data in a table.
CREATE TABLE table_name (
    column1 datatype constraint,
    column2 datatype constraint,
    ....
);
```

| **Constraint**   | **Description**                                                                                 |
| ---------------- | ----------------------------------------------------------------------------------------------- |
| `NOT NULL`       | Ensures that a column cannot have a NULL value                                                  |
| `UNIQUE`         | Ensures that all values in a column are different                                               |
| `PRIMARY KEY`    | A combination of a `NOT NULL` and `UNIQUE`. Uniquely identifies each row in a table             |
| `FOREIGN KEY`    | Prevents actions that would destroy links between tables                                        |
| `CHECK`          | Ensures that the values in a column satisfies a specific condition                              |
| `DEFAULT`        | Sets a default value for a column if no value is specified                                      |
| `CREATE INDEX`   | Used to create and retrieve data from the database very quickly                                 |
| `AUTO_INCREMENT` | allows a unique number to be generated automatically when a new record is inserted into a table | 

```sql
-- CREATE INDEX
CREATE INDEX index_name ON table_name (column1, column2, ...);
```

**VIEW**
```sql
-- A virtual table based on the result-set of an SQL statement.
CREATE VIEW view_name AS SELECT column1, column2, ... FROM table_name WHERE condition;
```