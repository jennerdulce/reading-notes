## SQLBolt NOTES (Structured Query Language)
### General Notes
- SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data 
from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.
- Designed to work with databases
- commonly used for blogs, enterprise corp level
- is scalabale
- There are multiple SQL databases each with the standard SQL with their own additional features/storage types
- Relational Database represents a collection of related (2-D) tables. TABLES ARE ALSO KNOWN AS RELATIONS.
  - These tables are similar to excel spreadsheets
  - have fixed names for the columns which are similar to attributes/properties of the tables
  - can accomodate any number of rows of data
- The goal of learning SQL is to learn how to answer SPECIFIC QUESTIONS about DATA

### Lesson 1: Select Queries
- to retrieve data, you use `SELECT` statements
- `SELECT`  statements are also referred as queries
  - a 'query' is a statement which delcares what data we are looking for, where to find it, transform it, and return it
  
#### Examples:
`
SELECT column1, column2
FROM table_name
`
`
SELECT *
FROM table_name
`

### Lesson 2: Queries with Constraints
- WHERE clauses specify CONSTRAINTS
- it would be very difficult to read a table with a million rows
- we use the `WHERE` clause to filter results from being returned
  - the CLAUSE is applied to all rows of data by checking specific coluumn values to determine whether it should be included or not
- clauses are in the form of expressions like in languages: >=, <=, =, <, >, !
- other clauses:
  - `column_name BETWEEN ... AND ...`
  - `column_name NOT BETWEEN ... AND ...`
  - `column_name IN(...)`
  - `column_name NOT IN(...)`
  
#### Examples:
 ```
 SELECT column1, column2
 FROM table_name
 WHERE year = #
 ```
 ```
 SELECT *
 FROM table_name
 WHERE year BETWEEN 2000 AND 2020
 ```
 ```
 SELECT *
 FROM table_name
 WHERE year > 2000
       AND year < 2020
 ```

### Lesson 3: Queries with Constraints *TEXT DATA*
- These constraints are useful when writing clauses for text data
- *_STRINGS MUST BE QUOTES_*
- *=* - Case-sensitive EXACT string match
- *!=* - Case-sensitive INEQUALITY string match
- *LIKE* - Case-insensitive EXACT string match
- *NOT LIKE* - Case-insensitive INEQUALITY string match
- *%* - Matches ANYWHERE in a string
- *_* - Matches single missing character

#### Examples:
`
SELECT *
FROM table_name
WHERE col_name LIKE 'AbC' // will match; 'abC', 'ABC', 'abc', 'aBc'
`
`
SELECT column_name
FROM table_name
WHERE col_name LIKE '%AT%' // will match; 'BAT', 'cat', 'attIC', 'MAttreSS'
`
`
SELECT *
FROM table_name
WHERE col_name = 'AN_' // will match; 'AND', 'ANT', 'AMY', 'ANY'
`

### Lesson 4: Filtering and Sorting Query Results
- results of particularly queries may not be completely unique.
- many movies may have the same director or are released ont he same year
- `DISTINCT` keyword will blindly removes duplicate rows
- `ORDER BY column_name ASC/DESC` clause is specified, each row is sorted alpha-numerically based on the specified column's value.
- `LIMIT num_limit OFFSET num_offset` clause limits how many rows/entries you would like to display
  - Reddit displays popular items on its front page. these posts can probably be sorted by views/likes, and each page can only contain 20 posts at a time.
  - `LIMIT` is commonly used with ORDER BY
- Using these clauses, a database can execute queries faster and more efficiently by processing and returning ONLY the requested content
  
#### Examples:
```
SELECT DISTINCT column_name
FROM table_name
```
```
SELECT *
FROM table_name
ORDER BY column_name ASC
```
```
SELECT *
FROM table_name
WHERE column_name > 2000
ORDER BY column_name ASC
LIMIT 5 OFFSET 5
```

### Lesson 13: Inserting Rows
- 'query for data' = to search for data
- in SQL, 'database Schema' describes the structure of each table as well as datatypes that each colummn of the table can contain
  - values in a 'year' column may need NUMBER datatypes
  - values in a 'title' column may need CHARCTER or a 'STRING' datatype
- `INSERT` statement describes which table to write into
  - columns of data we are filling
  - one or more rows of data to insert (you can insert multiple rows at a time)
    - must be separated by commas
  - in general, each ROW of data should contain values for every corresponding column in the table.
- End with a semi-colon

#### Examples
```
INSERT INTO table_name
(column_name1, column_name2)
VALUES (value1, value2), // row 1
       (value1, value2), // row 2
       (value1, value2); // row 3
```

### Lesson 14: Updating Rows
- `UPDATE` updates row data under the specified column
- 3 Parts:
```
UPDATE table_name // 1. choose table
SET column_name = new_value // set new values
    column_name2 = new_value // set new values
WHERE specified_row // WHERE clause specifies which row.
```
- *_IMPORTANT_* DO NOT FORGET TO ADD THE WHERE CLAUSE.
  - Forgetting to add the where clause will result in ALL the rows being updated
  - To prevent this. Use a `SELECT` Query and `WHERE` clause to check and see if you select the correct data


#### Examples
```
SELECT *
FROM table_name
WHERE column_name = value

UPDATE table_name
SET column_name = value
WHERE column_name = value
```
```
SELECT *
FROM Movies
WHERE Title = 'Movie Name'

// Setting a new year
UPDATE Movies
SET Year = 'New Year'
WHERE Title = 'Movie Name'
```
```
SELECT *
FROM People
WHERE first_name = 'first_name'
      AND last_name = 'last_name'
      
// Changing Multiple Columns
UPDATE Movies
SET column_name1 = new_value, // DONT FORGET THE COMMA
    column_name2 = new_value
WHERE first_name = 'first_name'
      AND last_name = 'last_name'
```
### Lesson 15: Deleting Rows
- `DELETE` statement to DELETE data from a table.
- `WHERE` clause specifies the row(s) to delete
  - Leaving out the `WHERE` will remove ALL rows
  - It is recommended just like when updating. that you use a SELECT query and WHERE clause to see if you have
  chosen the correct row you want to delete

#### Example
```
DELETE FROM table_name
WHERE condition = value
```
```
DELETE FROM table_name
WHERE year > 2005
```
```
DELETE FROM table_name
WHERE days_not_loggedin > 365
```

### Lesson 16: Create a Table
REFERENCE: https://sqlbolt.com/lesson/creating_tables
- There are different data types and table constraints

#### Example
```
DROP TABLE IF EXISTS table_name

CREATE TABLE table_name (
    id INTEGER PRIMARY KEY,
    title TEXT,
    director TEXT,
    year INTEGER, 
    length_minutes INTEGER
); // DO NOT FORGET TO ADD SEMI-COLON
```
```
CREATE TABLE IF NOT EXISTS table_name (
    column DataType table_constraint DEFAULT default_value,
    another_column DataType table_constraint DEFAULT default_value,
);
```
- setting default values will fill in missing data when users INSERT data into the table

### Lesson 17: Alter Tables
- `ALTER TABLE` Allows you to... alter the table..
#### Adding Columns
```
ALTER TABLE table_name
ADD column_name dataType constraint_here
    Default default_value //if you want
```
```
ALTER TABLE Movies
ADD Language TEXT
    DEFAULT English
```

#### Removing Columns
```
ALTER TABLE table_name
DROP column_name // will delete the column name
```

#### Renaming the TABLE
```
ALTER TABLE table_name
RENAME TO new_table_name
```

### Lesson 18: Drop Tables
```
DROP TABLE IF EXISTS mytable;
```

