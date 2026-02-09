# Assignment 1

This repository contains the SQL commands for the assignment. It includes table creation, data insertion, and various conditional queries using MySQL.

## 1. Database Setup

### Create Tables
Two tables were created: `Authors` and `Books`.

```sql
CREATE TABLE Authors (
    author_id INT PRIMARY KEY,
    name VARCHAR(100),
    country VARCHAR(50)
);

CREATE TABLE Books (
    book_id INT PRIMARY KEY,
    title VARCHAR(100),
    genre VARCHAR(50),
    price INT,
    author_id INT
);
```

### Insert Data
Sample data was inserted into both tables.

```sql
INSERT INTO Authors VALUES (1, 'J.K. Rowling', 'UK');
INSERT INTO Authors VALUES (2, 'George R.R. Martin', 'USA');
INSERT INTO Authors VALUES (3, 'Agatha Christie', 'UK');

INSERT INTO Books VALUES (101, 'Harry Potter', 'Fantasy', 20, 1);
INSERT INTO Books VALUES (102, 'Game of Thrones', 'Fantasy', 25, 2);
INSERT INTO Books VALUES (103, 'Murder on the Orient Express', 'Mystery', 15, 3);
INSERT INTO Books VALUES (104, 'Death on the Nile', 'Mystery', 12, 3);
INSERT INTO Books VALUES (105, 'A Clash of Kings', 'Fantasy', 22, 2);
```

## 2. Conditional Queries

### WHERE with AND
Selects books where the genre is 'Fantasy' and the price is greater than 20.

```sql
SELECT * FROM Books 
WHERE genre = 'Fantasy' AND price > 20;
```

### WHERE with OR
Selects books where the genre is 'Mystery' or the price is exactly 25.

```sql
SELECT * FROM Books 
WHERE genre = 'Mystery' OR price = 25;
```

### WHERE with NOT
Selects authors who are not from the UK.

```sql
SELECT * FROM Authors 
WHERE NOT country = 'UK';
```

## 3. Sorting and Pattern Matching

### ORDER BY
Sorts the books by price in descending order.

```sql
SELECT * FROM Books 
ORDER BY price DESC;
```

### LIKE
Selects books where the title starts with 'Harry'.

```sql
SELECT * FROM Books 
WHERE title LIKE 'Harry%';
```

##### Name: Ayan Parashar
##### Date: February 9, 2026
##### Internship Start Date: January 28, 2026