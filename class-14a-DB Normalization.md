# DB Normalization
ref:
- https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/

## GENERAL
- Process used to organize a database into tables and columns
- table should be specific topics
- columns should only support the topic introduced
- Intersection Table:
  - Only contains KEYS
  - useful to model many-to-many relationshoips
  - FOREIGN KEY correlates to a different table's PRIMARY KEY
  - The column referring to the keys may be named differently across table
  - Need to be link VIA SQL

### Benefits
- limit errors during modification
  1. Duplication Anomalies
  2. Modification Anomalies
  3. Deletion Anomalies
- limit duplicate data
- organized efficiently!

## 1NF
- searching, filtering, and sorting immediatebly become easier
- `FOREIGN KEY` is a value that matches a `PRIMARY KEY` in a different table
  - this is how tables are linked together
1. Unique Columns
2. Atomic (single) values within rows/values of columns

## 2 NF
- Narrow forms to a single purpose making it easier to describe and use
1. Be in 1NF
2. All non-key columns must be dependent on the PRIMARY KEY or TOPIC OF TABLE
- ask yourself, "Does this column serve to describe what the primary key identifies? 
  - Yes? Keep in table
  - No? Remove from table and place in a new table

## 3 NF
- other columns should not be dependent on each other
- when updating a column, should not affect the value of another.
  - creates update anomolies and error
  - extra unecessary work
- only dependency columns should have it to the PRIMARY KEY or table/topic
