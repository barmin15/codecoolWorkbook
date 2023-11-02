# Advanced Data module

## General SQL

### What are relational databases? Explain the theory behind them!
A relational database includes tables containing rows and columns.

### Why SQL is important these days?
Because nowadays, everyone, even if you just have a phone, you have a lot of data, and relational databases such as SQL can handle 
a LOT of data.

### All the new GUI tools enable me to click a button to write SQL. Why should I spend time learning to write SQL manually?
Because although tools allow you to write most queries, there may come a time, when the perfect query you want can only 
be written by hand.

### If SQL is standardized, should you be able to program with SQL on any databases?
Pls elaborate.

### What makes SQL a nonprocedural language?
Because Sql queries are not specified enough to be procedural. (it doesn't require you to specify opening and closing tables fo example).

### What can you do with SQL?
CRUD operations and manage connections between tables.

---

## DQL

### Do the following statements return the same or different output? Why?

```sql
SELECT * FROM CHECKS;
select * from checks;
```
it returns the same. Capital letters are a convention.

### The following queries do not work when entered into the command line psql console. Why not?

```sql
Select *
Select * from checks
Select amount name payee FROM checks;
```

first needs to specify the from. 
second should end with a semicolon.
third should seperate column names with comas.

### What shorthand could you use instead of `WHERE a >= 10 AND a <=30`?
the BETWEEN keyword

### Which function capitalizes the first letter of a character string and makes the rest lowercase?
the INITCAP() function.

### Will this query work? Why?

```sql
SELECT COUNT(LASTNAME) FROM CHARACTERS;
```
It will work, because the count will only be activated after all the characters are returned.

### Assuming that they are separate columns, which function(s) would splice together FIRSTNAME and LASTNAME?
the CONCAT() function

### Why are so few functions defined in the ANSI standard and so many defined by the individual implementations?
            PÉTER

### What is the function of the GROUP BY clause?
            PÉTER

### When using the HAVING clause, do you always have to use a GROUP BY also?
            PÉTER

### Can you use ORDER BY on a column that is not one of the columns in the SELECT statement? You can, but you have to specify
It works, because it works with the whole table, and then only shows what we want to see.

---

## Joins

### Explain the different kind of joins! (outer, inner, left, right, natural, etc.)
They join on different criteria, concerning what type of elements from which table to join together.

### How many tables can you join on?
You can join 3, 4, or even more! The possibilities are limitless.

### Would it be fair to say that when tables are joined, they actually become one table?
No it only creates a view table in sql.

### How many rows would a two-table join produce if one table had 50,000 rows and the other had 100,000?
Depends on the join type, and how many common rows they have.
MAX 150000
MIN 0

### What type of join appears in the following SELECT statement?

```sql
select e.name, e.employee_id, ep.salary  
from employee_tbl e, employee_pay_tbl ep  
where e.employee_id = ep.employee_id;
```

Inner join, UNION because only the common id's will appear in the view table.

### In joining tables are you limited to one-column joins, or can you join on more than one column?
You arent limited.

---

## DML

### Does SQL have a statement for file import/export operations?
yes (IMPORT TABLE [IF EXISTS] table_reference), the IMPORT TABLE statement

### Can you copy data from a table into itself using the INSERT command? You would like to make duplicate copies of all the existing records and change the value of one field.
INSERT...SELECT states helps you do this.

### What would happen if you issued the following statement?

```sql
DELETE * FROM COLLECTION;
```
nothing, because with delete you can only delete a selected few elements, you can use the DROP table if you want to delete the 
whole table.

### Can you remove columns with the ALTER TABLE statement?
yes, with teh ALTER TABLE ... DROP COLLUMN

### Is the DROP TABLE command functionally equivalent to the DELETE FROM <table_name> command?
no becasue drop command drops the whole table, the delete deletes the values

### What is the difference between the functionality of the DELETE FROM <table_name> and the TRUNCATE TABLE command?
delete command deletes some values it applies to, truncate deletes all values in table.

### When a table is created, who is the owner?
the user who created the table.

### If data in a character column has varying lengths, what is the best choice for the data type?
VARCHAR is great for storing data types with huge sizes.
