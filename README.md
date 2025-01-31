**Employee Management System**

**Overview**

This project is an Employee Management System designed to manage employee data, departments, and performance reviews. It includes CRUD operations for employees, department management, and performance review features. The system is built with an ASP.NET Core backend and a React.js frontend, ensuring a full-stack solution for managing employee data efficiently.

**Features**

1. Employee CRUD Operations
Create: Add a new employee with all required fields.

Read: List all employees with pagination.

Update: Edit employee details.

Delete: Soft delete an employee by marking them as "Deleted".

2. Department Management
Manage departments with fields such as Department Name, Manager, and Budget.

Each employee is assigned to a department with a foreign key relationship.

3. Employee Performance Review
Implement quarterly performance reviews for employees.

Store performance reviews in a separate table with a one-to-many relationship to employees.

Calculate the average performance score for each department, optimized for large datasets.

4. Search Functionality
Full-text search for employees by name.

Paginated results for efficient loading.

**Database Design**

Tables
Employee: Contains fields like Name, Email, Phone, Position, JoinDate, DepartmentID (Foreign Key), Status (active/inactive).

Department: Contains DepartmentName, ManagerID (Employee foreign key), and Budget.

PerformanceReview: Contains EmployeeID, ReviewDate, ReviewScore, ReviewNotes.

**Indexes**

Indexes are created for fields that are frequently queried (e.g., Employee Name, Department, Position, PerformanceScore).

**Constraints**
Foreign Key constraints for relational integrity (e.g., Employee → Department, Employee → PerformanceReview).

Soft Delete: Employees are marked as deleted, not physically removed.

Normalization: Employee-Department relationship is one-to-many, Employee-PerformanceReview is one-to-many.

**Performance Considerations**

Optimized queries for listing employees, filtering, and aggregating (like calculating the average performance score).

Pagination for listing employees and performance reviews to avoid performance hits on large datasets.

Use of indexes on columns that are commonly searched or filtered.

**Frontend**

Built with React.js for a responsive and interactive user interface.

Supports viewing, adding, updating, and deleting employee records.

Search and filter capabilities for employees by name, department, and performance score.

Displays average performance score per department.
