## Problem 1: Revising the Select Query I

### Problem Description
Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

### Example Data
```sql
CREATE TABLE CITY (
    ID INT,
    NAME VARCHAR(50),
    COUNTRYCODE VARCHAR(3),
    DISTRICT VARCHAR(50),
    POPULATION INT
);

INSERT INTO CITY (ID, NAME, COUNTRYCODE, DISTRICT, POPULATION) VALUES
(1, 'New York', 'USA', 'New York', 8008278),
(2, 'Los Angeles', 'USA', 'California', 3694820),
(3, 'Chicago', 'USA', 'Illinois', 2896016);

### Initial Solution with Mistakes
SELECT *
FROM CITY
WHERE COUNTRYCODE == 'USA' && POPULATION > 100000;

### Analysis of Mistakes
1. Equality Operator:
- Used '==' instead of '='. In SQL, the equality operator is '='.
- Correction: Replace '==' with '='.

2. Logical AND Operator:
- Used '&&' instead of 'AND'. In SQL, the logical AND operator is 'AND'.
- Correction: Replace '&&' with 'AND'.

### Correct Solution
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'USA' AND POPULATION > 100000;

### Lessons Learned
- Always use 'AND' for logical conjunction in SQL.
- Use '=' for equality comparison in SQL.
