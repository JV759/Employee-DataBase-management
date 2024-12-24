# Employee-DataBase-management
Overview

#This SQL file contains queries and commands designed to manage and analyze employee, department, project, and timesheet data for a fictitious organization. It includes table creation, data insertion, updates, and advanced queries for analytics and insights.


# Database Structure

# Database Name: emp_details

Tables Created:

Departments: Stores department details such as name and location.

Employees: Stores employee details including name, contact info, hire date, job title, department, and salary.

Projects: Stores project details including name, description, dates, and associated department.

Timesheets: Tracks employee hours worked on projects.

SQL Instructions

1. Database Initialization

Create the database using:

CREATE DATABASE emp_details;
USE emp_details;

2. Table Creation

Four tables: Departments, Employees, Projects, and Timesheets.

Primary keys are auto-incremented.

Foreign keys establish relationships between Employees, Departments, and Projects.

3. Data Insertion

Pre-populated example data for:

Departments: 9 departments.

Employees: 14 employees.

Projects: 10 projects.

Timesheets: Hours logged for specific projects by employees.

Key Queries and Their Purposes

Queries for Analysis and Updates

# Working Location of Employees:
Retrieves the department location for each employee.

# SELECT e.first_name, e.last_name, d.location
FROM Employees e
JOIN Departments d ON e.department_id = d.id;

# Adding and Updating Salaries:
Adds a salary column and updates salaries based on department.

# ALTER TABLE Employees ADD COLUMN salary DECIMAL(10, 2);
UPDATE Employees SET salary = ...;

# Projects Assigned to Employees:
Lists the projects employees are working on.

# Total Hours Worked per Project:
Summarizes hours worked by each employee for every project.

# Employees Not Assigned Any Projects:
Identifies employees without project allocations.

# Maximum Hours Worked Project:
Finds the project with the highest total hours logged.


# Employee Department Salaries:
Combines employee names, department names, and salaries into a view for simplified access.

# Employee Projects:
Stores details of projects assigned to employees.

# Advanced Queries:

# Employees Working Over 40 Hours on a Single Project:
Identifies employees exceeding 40 hours on any project.

# Employee Classification by Job Title:
Classifies employees as 'Manager', 'Developer', or 'Other'.

# Employees Working on Multiple Projects:
Lists employees assigned to more than one project.

# Ranking Employees by Hours Worked:
Ranks employees based on total hours logged across projects.

# Employees with Hours Above Average:
Identifies employees whose total hours exceed the average hours worked by all employees.
