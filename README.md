## Real World SQL Questions Based On HackerRank Challenges
```
-- Create employee table
CREATE TABLE Employee (
    employeeID INT PRIMARY KEY,
    name VARCHAR(255),
    managerID INT,
    dateOfJoining DATE,
    city VARCHAR(255)
);

-- Insert data into the employee table
INSERT INTO Employee VALUES
(1, 'John', 768, '2022-01-01', 'New York'),
(2, 'Alice', 657, '2022-02-01', 'Los Angeles'),
(3, 'Bob', 768, '2022-03-01', 'Chicago'),
(4, 'Charlie', 657, '2022-04-01', 'Houston'),
(5, 'David', 768, '2022-05-01', 'Phoenix'),
(6, 'Eva', 657, '2022-06-01', 'Philadelphia'),
(7, 'Frank', 768, '2022-07-01', 'San Antonio'),
(8, 'Grace', 657, '2022-08-01', 'San Diego'),
(9, 'Harry', 768, '2022-09-01', 'Dallas'),
(10, 'Ivy', 657, '2022-10-01', 'San Jose');

-- Create salary table
CREATE TABLE Salary (
    employeeID INT,
    project VARCHAR(255),
    salary DECIMAL(10, 2),
    variable DECIMAL(10, 2)
);

-- Insert data into the salary table
INSERT INTO Salary VALUES
(1, 'P1', 50000, 2000),
(2, 'P2', 45000, 1500),
(3, 'P1', 48000, 1800),
(4, 'P2', 42000, 1200),
(5, 'P1', 55000, 2500),
(6, 'P2', 49000, 1700),
(7, 'P1', 51000, 2100),
(8, 'P2', 46000, 1600),
(9, 'P1', 53000, 2300),
(10, 'P2', 47000, 1400);

-- Display employee table
SELECT * FROM Employee;

-- Display salary table
SELECT * FROM Salary;
```

## Fetch employeeID and name of all employees working under manager with managerID:
Team Hierarchy Query - In a corporate environment, the HR department uses this query to generate a report of all employees working under a specific manager. For example, when the manager with ID 768 wants to review the team members' details, this query provides a concise list of employee IDs and names.
```
SELECT employeeID, name
FROM Employee
WHERE managerID = 768;
```

## Fetch different projects available from the salary table:
Project Overview Query - Project managers use this query to get an overview of all distinct projects employees are working on. It helps in project planning and resource allocation.
```
SELECT DISTINCT project
FROM Salary;
```

## Fetch count of employees working in project P1:
Project Workforce Query - Project leads use this query to determine the number of employees involved in a specific project, such as P1.
```
SELECT COUNT(*) AS employeeCount
FROM Salary
WHERE project = 'P1';
```

## Find maximum, minimum, and average salary from employees:
Salary Statistics Query - The finance department utilizes this query to analyze salary trends within the organization.
```
SELECT MAX(salary) AS maxSalary,
       MIN(salary) AS minSalary,
       AVG(salary) AS avgSalary
FROM Salary;
```

## Find the employee ID whose salary lies in the range of 30000 and 40000:
Salary Range Identification Query - HR uses this query to identify employees with salaries in a specific range, aiding in compensation analysis.
```
SELECT employeeID
FROM Salary
WHERE salary BETWEEN 30000 AND 40000;
```

## Fetch employees who live in Chicago and work under manager with managerID 768:
Location and Manager Query - When the HR department needs to identify employees based in a specific city (Chicago) working under a particular manager (ID 768).
```
SELECT *
FROM Employee
WHERE city = 'Chicago' AND managerID = 768;
```

## Fetch employees who either live in Chicago or work under a manager with managerID 657:
Flexible Criteria Query - In scenarios where HR needs to identify employees based on multiple criteria, this query allows flexibility.
```
SELECT *
FROM Employee
WHERE city = 'Chicago' OR managerID = 657;
```

## Fetch all employees who work on Project other than P1:
Excluding Specific Project Query - In project planning, when a manager wants to see employees not involved in a particular project (P1).
```
SELECT *
FROM Salary
WHERE project <> 'P1';
```

## Display total salary of each employee adding the salary with variable value:
Comprehensive Compensation Query - Finance or payroll department uses this query to calculate total compensation for each employee by adding base salary and variable components.
```
SELECT employeeID, (salary + variable) AS totalCompensation
FROM Salary;
```

## Fetch employees whose name begins with any two characters, followed by "vi" and ending with any sequence of characters:
Name Pattern Matching Query - HR uses this query to find employees with specific name patterns.
```
SELECT *
FROM Employee
WHERE name LIKE '__vi%';
```

## List out employees working in department 10 and draw salaries more than 3500:
Department Salary Criteria Query - HR or management can use this query to identify high-salaried employees in a specific department (e.g., department 10).
```
SELECT *
FROM Employee
WHERE departmentID = 10 AND salary > 3500;
```

## List out employeeID, name in descending order based on salary column:
Salary Sorting Query - HR or management uses this query to generate a list of employees sorted by salary in descending order.
```
SELECT employeeID, name
FROM Employee
ORDER BY salary DESC;
```

## How many employees are working in different departments in the organization:
Department Employee Count Query - HR uses this query to get an overview of the number of employees in each department.
```
SELECT departmentID, COUNT(*) AS employeeCount
FROM Employee
GROUP BY departmentID;
```

## List out the departmentID having at least 3 employees:
Department Size Query - HR uses this query to identify departments with a minimum number of employees, ensuring adequate workforce distribution.
```
SELECT departmentID
FROM Employee
GROUP BY departmentID
HAVING COUNT(*) >= 3;
```

## Display the employees who got the maximum salary:
Top Earner Query - When HR or management wants to recognize the top earner in the organization.
```
SELECT *
FROM Employee
WHERE salary = (SELECT MAX(salary) FROM Employee);
```

## Display the employees who are working in the sales department:
Departmental Employee Query - HR or management uses this query to identify employees in a specific department (e.g., sales).
```
SELECT *
FROM Employee
WHERE department = 'Sales';
```

## Display the employees who are working in New York:
Location-Based Employee Query - HR uses this query to identify employees based in a specific location (e.g., New York).
```
SELECT *
FROM Employee
WHERE city = 'New York';
```

## Update the employees' salaries who are working as managers based on 10%:
Managerial Salary Adjustment Query - In salary adjustments, HR updates the salaries of employees who work as managers, giving them a 10% raise.
```
UPDATE Employee
SET salary = salary * 1.10
WHERE position = 'Manager';
```

## Delete employees who are working in the accounting department:
Department Employee Removal Query - When restructuring, HR can use this query to remove employees from a specific department (e.g., accounting).
```
DELETE FROM Employee
WHERE department = 'Accounting';
```

## Display the highest salary from the employee table:
Top Salary Identification Query - HR or finance uses this query to identify the highest salary paid within the organization.
```
SELECT MAX(salary) AS highestSalary
FROM Employee;
```

## Display the 2nd highest salary from the employee table:
Second Top Salary Identification Query - HR or finance uses this query to identify the second-highest salary paid within the organization.
```
SELECT MAX(salary) AS secondHighestSalary
FROM Employee
WHERE salary < (SELECT MAX(salary) FROM Employee);
```

## Display the nth highest salary from the employee table:
Nth Top Salary Identification Query - HR or finance can adapt this query to find the nth highest salary within the organization.
```
SELECT DISTINCT salary
FROM Employee e1
WHERE n = (SELECT COUNT(DISTINCT salary) FROM Employee e2 WHERE e1.salary <= e2.salary);
```

## Display the nth highest salary from the employee table without using max(), limit or top:
Alternative Nth Top Salary Identification Query - An alternative approach to finding the nth highest salary without using specific functions like `MAX()`, `LIMIT`, or `TOP`.
```
SELECT DISTINCT salary
FROM Employee e1
WHERE n - 1 = (SELECT COUNT(DISTINCT salary) FROM Employee e2 WHERE e1.salary < e2.salary);
```

## Two ways to delete duplicates from a table:
Duplicate Data Cleanup - HR or database administrators can use these queries to remove duplicate entries in the `Employee` table.
```
-- Method 1: Using ROW_NUMBER()
DELETE FROM Employee
WHERE employeeID NOT IN (
SELECT MAX(employeeID)
FROM Employee
GROUP BY name, city);

-- Method 2: Using Common Table Expression (CTE)
WITH Duplicates AS (
SELECT name, city, COUNT(*) AS duplicateCount
FROM Employee
GROUP BY name, city
HAVING COUNT(*) > 1)
DELETE FROM Employee
FROM Employee e
JOIN Duplicates d ON e.name = d.name AND e.city = d.city
WHERE ROW_NUMBER() OVER (PARTITION BY e.name, e.city ORDER BY e.employeeID) > 1;
```

## Two ways to create a table from an existing table, only structure without data:
Table Structure Replication - In scenarios where a similar table structure is needed, these queries create a new table without duplicating data.
```
-- Method 1: Using CREATE TABLE AS
CREATE TABLE NewEmployee AS
SELECT *
FROM Employee
WHERE 1 = 0; -- Ensures no data is copied

-- Method 2: Using SELECT INTO
SELECT *
INTO NewEmployee2
FROM Employee
WHERE 1 = 0; -- Ensures no data is copied
```

## Display country names from the country table that do not start with vowels and do not end with vowels. Results should not contain duplicates:
Country Name Filtering Query - In a scenario where countries need to be filtered based on specific criteria, this query retrieves country names that do not start or end with vowels, excluding duplicates.
```
SELECT DISTINCT countryName
FROM Country
WHERE countryName NOT LIKE '[AEIOU]%' AND countryName NOT LIKE '%[AEIOU]'
```

## Write an SQL query to find the current date:
Current Date Retrieval Query - The query retrieves the current date, which can be useful for timestamping or time-sensitive operations.
```
SELECT CURRENT_DATE AS currentDate;
```

## Write an SQL query to fetch all the departmentIDs present in either of the tables: employees or departments:
DepartmentID Retrieval Query - This query retrieves all distinct departmentIDs from both the `Employee` and `Department` tables.
```
SELECT DISTINCT departmentID
FROM (SELECT departmentID FROM Employee
UNION
SELECT departmentID FROM Department) AS AllDepartments;
```

## Write an SQL query to fetch common records between two tables:
Common Records Identification Query - In cases where identifying common records between two tables is necessary, this query retrieves the intersecting records.
```
SELECT *
FROM Employee
INTERSECT
SELECT *
FROM Department;
```

## Write an SQL query to fetch records that are present in one table but not in another table:
Exclusivity Query - When identifying records that exist in one table but not in another is needed, this query provides the result.
```
SELECT *
FROM Employee
EXCEPT
SELECT *
FROM Department;

