# SQL Basics for QA Testing

## Overview

This document contains basic SQL queries practiced as part of my QA learning journey. The objective was to understand how QA engineers use SQL to retrieve, filter, and validate data stored in databases.

## Topics Covered

* SELECT
* WHERE
* AND
* OR
* LIKE
* BETWEEN
* ORDER BY
* LIMIT
* NULL Handling



## Query 1 – Retrieve All Users


SELECT * FROM users;


**Purpose:** Retrieve all records from the users table.



## Query 2 – Retrieve All Orders


SELECT * FROM orders;


**Purpose:** Retrieve all records from the orders table.



## Query 3 – Retrieve Active Users


SELECT * FROM users
WHERE status = 'active';


**Purpose:** Filter users based on their account status.



## Query 4 – Retrieve Completed Orders


SELECT * FROM orders
WHERE status = 'completed';


**Purpose:** Verify completed orders.



## Query 5 – Retrieve Orders Above a Specific Amount


SELECT * FROM orders
WHERE amount > 100;


**Purpose:** Filter orders based on order value.



## Query 6 – Retrieve Users with Missing Email Addresses


SELECT * FROM users
WHERE email IS NULL;


**Purpose:** Identify records with missing data.

**QA Use Case:** Data validation and defect investigation.



## Query 7 – Retrieve Orders for a Specific User


SELECT * FROM orders
WHERE user_id = 2;


**Purpose:** Verify orders associated with a specific user.



## Query 8 – Sort Orders by Amount (Descending)


SELECT * FROM orders
ORDER BY amount DESC;


**Purpose:** Display orders from highest to lowest amount.



## Query 9 – Retrieve the First Five Orders


SELECT * FROM orders
ORDER BY id ASC
LIMIT 5;


**Purpose:** Practice pagination and result limiting.



## Query 10 – Retrieve Users Whose Name Starts with "A"


SELECT * FROM users
WHERE name LIKE 'A%';


**Purpose:** Practice pattern matching and filtering.



## Key Learning Outcomes

Through these exercises, I learned how to:

* Retrieve data from database tables.
* Apply filters using SQL conditions.
* Work with NULL values.
* Sort and limit query results.
* Use SQL to support QA testing activities.
* Understand the relationship between API responses and database records.

## QA Relevance

SQL is an essential skill for QA engineers because it helps validate backend data, investigate defects, verify API responses, and ensure data integrity across systems.
