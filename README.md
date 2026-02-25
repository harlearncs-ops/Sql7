 ## 1. Introduction

A VIEW in DBMS is a virtual table created using a SQL SELECT statement.  
It does not store data physically.  
Instead, it stores the query and shows the result when accessed.

A view helps users see only the required data from one or more tables.

---

## 2. Syntax

```sql
CREATE VIEW view_name AS
SELECT column1, column2
FROM table_name
WHERE condition;
```

---

## 3. Example

### Create Table

```sql
CREATE TABLE Students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    marks INT
);
```

### Insert Data

```sql
INSERT INTO Students VALUES
(1, 'Arun', 'CSE', 85),
(2, 'Priya', 'ECE', 65),
(3, 'Kiran', 'CSE', 90);
```

### Create View

```sql
CREATE VIEW High_Marks AS
SELECT name, department, marks
FROM Students
WHERE marks > 70;
```

### Use View

```sql
SELECT * FROM High_Marks;
```

---

## 4. Advantages and Limitations

### Advantages
- Improves security  
- Simplifies complex queries  
- Hides sensitive data  
- Reusable query  

### Limitations
- Not always updatable  
- Depends on base table  
- Does not store data physically  

---

## 5. Conclusion

A VIEW is a saved SQL query that works like a virtual table.  
It helps in simplifying database operations and improving data security.# Sql7
