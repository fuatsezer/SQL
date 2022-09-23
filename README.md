# SQL
## A seat at the table
* Table rows and columns are reffered to as records and fields
* Fields are set at database creation; there is no limit to the number of records
* Table names should...
    * be lowercase
    * have no spaces - use underscores instead
    * refer to a collective group or be plural
* Field names should...
  * be lowercase
  * have no spaces
  * be singular
  * be different from other fields names
  * be different from the table names

## Selecting one column
```SQL
SELECT name
FROM employees
```
## Selecting all columns
```SQL
SELECT *
FROM employees
```

## Aliasing
```SQL
SELECT name AS first_name, year_hired
FROM employees
```

## Selecting distinct records
```SQL
SELECT DISTINCT year_hired
FROM employees
```

## DISTINCT with multiple fields
```SQL
SELECT DISTINCT dept_id,year_hired
FROM employees
```

## Views
* A view is a virtual table that is the result of a saved SQL `SELECT` statement
* When accessed,views automatically update in response to updates in the underlying data.
```SQL
CREATE VIEW employee_hire_years AS 
SELECT id, name, year_hired
FROM employees
```
Using Views
```SQL
SELECT id, name
FROM employee_hire_years
```




