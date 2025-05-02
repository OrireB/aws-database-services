# AWS Database Services

This project demonstrates basic database services on AWS using Amazon RDS and DynamoDB.

---

## 1. RDS Setup (MySQL)

- **Engine:** MySQL
- **Instance Type:** db.t3.micro (Free Tier eligible)
- **Storage:** 20 GB
- **Public Access:** Enabled
- **Client Used:** MySQL Workbench

### SQL Operations

```sql

-- Create database
CREATE DATABASE aws_demo;
USE aws_demo;

-- Create table
CREATE TABLE Students (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

-- Insert data
INSERT INTO Students (id, name, email) VALUES
(1, 'Angel', 'angel@example.com'),
(2, 'Anthony', 'anthony@example.com'),
(3, 'Alicia', 'alicia@example.com');

-- Read data
SELECT * FROM Students;

-- Update data
UPDATE Students: To change Anthony’s email:
SET email = 'anthony@example.com'
WHERE id = 2;
Then run: SELECT * FROM Students;
**Client Used:**
**This shows Bob’s updated email.**


-- Delete data
DELETE FROM Students: To remove Angel from the table:
WHERE id = 1;
Then check again: SELECT * FROM Students;



## RDS Setup

- **Engine:** MySQL/PostgreSQL
- **Host:** [your RDS endpoint]
- **Client:** DBeaver / MySQL Workbench
- **SQL Queries:**
  - Create, Read, Update, Delete operations on a `users` table.

## DynamoDB Setup

- Table: `Products`
- Partition Key: `ProductID`
- Sample Items:
  - `ProductID`: "1001", `Name`: "Laptop", `Price`: 1299

## Screenshots

Here are the key screenshots:

- **Screenshot 1**: RDS instance
  ![RDS instance dashboard showing the status as “Available”](https://raw.githubusercontent.com/OrireB/aws-database-services/ae1d9ac30ea39892268b982dae29934a245812c5/RDS%20instance.png)

---

- **Screenshot 2**: MySQL Connected Successfully
  ![Connected MySQL with database overview](https://raw.githubusercontent.com/OrireB/aws-database-services/ae1d9ac30ea39892268b982dae29934a245812c5/MySQL%20Connected%20Successfully.png)

---

## Architectural Diagram

![Architecture](architecture-diagram.png)
