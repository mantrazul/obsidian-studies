

### How to add collumns and values

You have this table.

| E_ID | E_Name | E_Gender | E_Email_Id |
| ---- | ------ | -------- | ---------- |
| 1    | George | F        | fl.com     |
| 2     | Rachel | F       |  ra.com    |


You can `ALTER TABLE` thus adding a new Collumn in SQL

For instance:

```SQL
ALTER TABLE table_name
ADD col_name data_type
```

So using our example we would have:

```SQL
ALTER TABLE Employee
ADD E_LastName VARCHAR(20)
SELECT * FROM Employee;
```

| E_ID | E_Name | E_Gender | E_Email_Id | E_LastName |
| ---- | ------ | -------- | ---------- | ---------- |
| 1    | George | F        | fl.com     | Null       |
| 2    | Rachel | F        | ra.com     | Null       | 

> [!warning] Datatypes:
>`VARCHAR(20)` | INT



To add value:

```SQL
UPDATE Employee
SET E_LastName = 'Smith'
WHERE E_ID = 1;
SELECT * FROM Employee;
```

And we get:

| E_ID | E_Name | E_Gender | E_Email_Id | E_LastName |
| ---- | ------ | -------- | ---------- | ---------- |
| 1    | George | F        | fl.com     | Smith      |
| 2    | Rachel | F        | ra.com     | Null       |

### How to drop collumns

```SQL
ALTER TABLE table_name
DROP COLUMN col_name;
```

### How to rename collumns

```SQL
sp_rename 'table_name.col_name', 'new_col_name', 'COLUMN'
```
