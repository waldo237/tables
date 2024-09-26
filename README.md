### **Database Schema:**

You are given a simplified human resources database consisting of the following tables:

1. **employees**

   | Column        | Data Type       | Description                      |
   |---------------|-----------------|----------------------------------|
   | employee_id   | INT, Primary Key| Unique identifier for each employee |
   | first_name    | VARCHAR(50)     | Employee's first name            |
   | last_name     | VARCHAR(50)     | Employee's last name             |
   | department_id | INT             | References departments(department_id) |
   | salary        | DECIMAL(10, 2)  | Employee's salary                |
   | hire_date     | DATE            | Date the employee was hired      |

2. **departments**

   | Column         | Data Type       | Description                     |
   |----------------|-----------------|---------------------------------|
   | department_id  | INT, Primary Key| Unique identifier for each department |
   | department_name| VARCHAR(100)    | Name of the department          |

3. **projects**

   | Column      | Data Type       | Description                      |
   |-------------|-----------------|----------------------------------|
   | project_id  | INT, Primary Key| Unique identifier for each project |
   | project_name| VARCHAR(100)    | Name of the project              |
   | start_date  | DATE            | Project start date               |
   | end_date    | DATE, Nullable  | Project end date (if completed)  |

4. **employee_projects**

   | Column       | Data Type       | Description                             |
   |--------------|-----------------|-----------------------------------------|
   | employee_id  | INT             | References employees(employee_id)     |
   | project_id   | INT             | References projects(project_id)       |
   | assigned_date| DATE            | Date the employee was assigned to the project |
   | role         | VARCHAR(50)     | Employee's role in the project          |

