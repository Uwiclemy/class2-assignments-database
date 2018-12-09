# Week Two Assignments
Figure out the appropiate sql queries for the following operation on the hr dataset and add your answers. For your first week you will be writing queries to query the hr database. The data and the structre of the database are present in the Data floder of this repo.


## Create Table

- Write a SQL statement to create a simple table countries including columns country_id,country_name and region_id. 


- Write a SQL statement to create a simple table countries including columns country_id,country_name and region_id which already exist.


- Write a SQL statement to create the structure of a table dup_countries similar to countries.


- Write a SQL statement to create a duplicate copy of countries table including structure and data by name dup_countries.


- Write a SQL statement to create a table countries set a constraint NULL.


- Write a SQL statement to create a table named jobs including columns job_id, job_title, min_salary, max_salary and check whether the max_salary amount exceeding the upper limit 25000. 


- Write a SQL statement to create a table named countries including columns country_id, country_name and region_id and make sure that no countries except Italy, India and China will be entered in the table.


- Write a SQL statement to create a table named countries including columns country_id,country_name and region_id and make sure that no duplicate data against column country_id will be allowed at the time of insertion.


- Write a SQL statement to create a table named jobs including columns job_id, job_title, min_salary and max_salary, and make sure that, the default value for job_title is blank and min_salary is 8000 and max_salary is NULL will be entered automatically at the time of insertion if no value assigned for the specified columns.

- Write a SQL statement to create a table named countries including columns country_id, country_name and region_id and make sure that the country_id column will be a key field which will not contain any duplicate data at the time of insertion. 


- Write a SQL statement to create a table countries including columns country_id, country_name and region_id and make sure that the column country_id will be unique and store an auto-incremented value. 


- Write a SQL statement to create a table countries including columns country_id, country_name and region_id and make sure that the combination of columns country_id and region_id will be unique. 


- Write a SQL statement to create a table job_history including columns employee_id, start_date, end_date, job_id and department_id and make sure that, the employee_id column does not contain any duplicate value at the time of insertion and the foreign key column job_id contain only those values which exist in the jobs table.

Here is the structure of the table jobs;

   Column   |         Type          |               Modifiers
------------+-----------------------+----------------------------------------
 job_id     | character varying(10) | not null default ''::character varying
 job_title  | character varying(35) | not null
 min_salary | numeric(6,0)          | default NULL::numeric
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)

- Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, email, phone_number hire_date, job_id, salary, commission, manager_id and department_id and make sure that, the employee_id column does not contain any duplicate value at the time of insertion and the foreign key columns combined by department_id and manager_id columns contain only those unique combination values, which combinations exist in the departments table.

Assume the structure of departments table below.

     Column      |         Type          |           Modifiers
-----------------+-----------------------+--------------------------------
 department_id   | numeric(4,0)          | not null
 department_name | character varying(30) | not null
 manager_id      | numeric(6,0)          | not null default NULL::numeric
 location_id     | numeric(4,0)          | default NULL::numeric
Indexes:
    "departments_pkey" PRIMARY KEY, btree (department_id, manager_id)

-  Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, email, phone_number hire_date, job_id, salary, commission, manager_id and department_id and make sure that, the employee_id column does not contain any duplicate value at the time of insertion, and the foreign key column department_id, reference by the column department_id of departments table, can contain only those values which are exist in the departments table and another foreign key column job_id, referenced by the column job_id of jobs table, can contain only those values which exist in the jobs table.

Assume that the structure of two tables departments and jobs.

     Column      |         Type          |       Modifiers
-----------------+-----------------------+-----------------------
 department_id   | numeric(4,0)          | not null
 department_name | character varying(30) | not null
 manager_id      | numeric(6,0)          | default NULL::numeric
 location_id     | numeric(4,0)          | default NULL::numeric
Indexes:
    "departments_pkey" PRIMARY KEY, btree (department_id)



   Column   |         Type          |               Modifiers
------------+-----------------------+----------------------------------------
 job_id     | character varying(10) | not null default ''::character varying
 job_title  | character varying(35) | not null
 min_salary | numeric(6,0)          | default NULL::numeric
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)


- Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, job_id, salary and make sure that, the employee_id column does not contain any duplicate value at the time of insertion, and the foreign key column job_id, referenced by the column job_id of jobs table, can contain only those values which exist in the jobs table. The specialty of the statement is that the ON UPDATE CASCADE action allows you to perform the cross-table update and ON DELETE RESTRICT action rejects the deletion. The default action is ON DELETE RESTRICT.

Assume that the following is the structure of the table jobs.

CREATE TABLE IF NOT EXISTS jobs ( 
JOB_ID INTEGER NOT NULL UNIQUE PRIMARY KEY, 
JOB_TITLE varchar(35) NOT NULL DEFAULT ' ', 
MIN_SALARY decimal(6,0) DEFAULT 8000, 
MAX_SALARY decimal(6,0) DEFAULT NULL
);

   Column   |         Type          |                Modifiers
------------+-----------------------+-----------------------------------------
 job_id     | integer               | not null
 job_title  | character varying(35) | not null default ' '::character varying
 min_salary | numeric(6,0)          | default 8000
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)


- Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, job_id, salary and make sure that, the employee_id column does not contain any duplicate value at the time of insertion, and the foreign key column job_id, referenced by the column job_id of jobs table, can contain only those values which exist in the jobs table. The specialty of the statement is that the ON DELETE CASCADE that lets you allow to delete records in the employees(child) table that refers to a record in the jobs(parent) table when the record in the parent table is deleted and the ON UPDATE RESTRICT actions reject any updates.

Assume that the following is the structure of the table jobs.

CREATE TABLE IF NOT EXISTS jobs ( 
JOB_ID INTEGER NOT NULL UNIQUE PRIMARY KEY, 
JOB_TITLE varchar(35) NOT NULL DEFAULT ' ', 
MIN_SALARY decimal(6,0) DEFAULT 8000, 
MAX_SALARY decimal(6,0) DEFAULT NULL
);



   Column   |         Type          |                Modifiers
------------+-----------------------+-----------------------------------------
 job_id     | integer               | not null
 job_title  | character varying(35) | not null default ' '::character varying
 min_salary | numeric(6,0)          | default 8000
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)


- Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, job_id, salary and make sure that, the employee_id column does not contain any duplicate value at the time of insertion, and the foreign key column job_id, referenced by the column job_id of jobs table, can contain only those values which exist in the jobs table. The specialty of the statement is that the ON DELETE SET NULL action will set the foreign key column values in the child table(employees) to NULL when the record in the parent table(jobs) is deleted, with a condition that the foreign key column in the child table must accept NULL values and the ON UPDATE SET NULL action resets the values in the rows in the child table(employees) to NULL values when the rows in the parent table(jobs) are updated.

Assume that the following is the structure of two table jobs.

CREATE TABLE IF NOT EXISTS jobs ( 
JOB_ID INTEGER NOT NULL UNIQUE PRIMARY KEY, 
JOB_TITLE varchar(35) NOT NULL DEFAULT ' ', 
MIN_SALARY decimal(6,0) DEFAULT 8000, 
MAX_SALARY decimal(6,0) DEFAULT NULL
);



   Column   |         Type          |                Modifiers
------------+-----------------------+-----------------------------------------
 job_id     | integer               | not null
 job_title  | character varying(35) | not null default ' '::character varying
 min_salary | numeric(6,0)          | default 8000
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)

- Write a SQL statement to create a table employees including columns employee_id, first_name, last_name, job_id, salary and make sure that, the employee_id column does not contain any duplicate value at the time of insertion, and the foreign key column job_id, referenced by the column job_id of jobs table, can contain only those values which exist in the jobs table. The specialty of the statement is that, The ON DELETE NO ACTION and the ON UPDATE NO ACTION actions will reject the deletion and any updates.

Assume that the following is the structure of two table jobs.

CREATE TABLE IF NOT EXISTS jobs ( 
JOB_ID INTEGER NOT NULL UNIQUE PRIMARY KEY, 
JOB_TITLE varchar(35) NOT NULL DEFAULT ' ', 
MIN_SALARY decimal(6,0) DEFAULT 8000, 
MAX_SALARY decimal(6,0) DEFAULT NULL
);



   Column   |         Type          |                Modifiers
------------+-----------------------+-----------------------------------------
 job_id     | integer               | not null
 job_title  | character varying(35) | not null default ' '::character varying
 min_salary | numeric(6,0)          | default 8000
 max_salary | numeric(6,0)          | default NULL::numeric
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)

## Alter Table

- Write a SQL statement to rename the table countries to country_new. 

- Write a SQL statement to add a column region_id to the table locations.

If you do not have location table create one with this structure

     Column     |         Type          | Modifiers
----------------+-----------------------+-----------
 location_id    | numeric(4,0)          |
 street_address | character varying(40) |
 postal_code    | character varying(12) |
 city           | character varying(30) |
 state_province | character varying(25) |
 country_id     | character varying(2)  |

- Write a SQL statement to change the data type of the column region_id to text in the table locations.

- Write a SQL statement to drop the column city from the table locations.

- Write a SQL statement to change the name of the column state_province to state, keeping the data type and size same.

- Write a SQL statement to add a primary key for the columns location_id in the locations table.

- Write a SQL statement to add a primary key for a combination of columns location_id and country_id.

- Write a SQL statement to drop the existing primary from the table locations on a combination of columns location_id and country_id.

- Write a SQL statement to add a foreign key on job_id column of job_history table referencing to the primary key job_id of jobs table.

Here is the structure of the table jobs and job_history. Create table with the structure if you dont have it in your database

Table jobs

   Column   |         Type          | Modifiers
------------+-----------------------+-----------
 job_id     | character varying(10) | not null
 job_title  | character varying(35) |
 min_salary | numeric(6,0)          |
 max_salary | numeric(6,0)          |
Indexes:
    "jobs_pkey" PRIMARY KEY, btree (job_id)
	

Table job_history

    Column     |         Type          | Modifiers
---------------+-----------------------+-----------
 employee_id   | numeric(6,0)          |
 start_date    | date                  |
 end_date      | date                  |
 job_id        | character varying(10) |
 department_id | numeric(4,0)          |


- Write a SQL statement to add a foreign key constraint named fk_job_id on job_id column of job_history table referencing to the primary key job_id of jobs table.

- Write a SQL statement to drop the existing foreign key fk_job_id from job_history table on job_id column which is referencing to the job_id of jobs table.

- Write a SQL statement to add an index named index_job_id on job_id column in the table job_history.

- Write a SQL statement to drop the index indx_job_id from job_history table.

## Insert into Table

- Write a SQL statement to insert a record with your own value into the table countries against each column.

Here in the following is the structure of the table countries.

    Column    |         Type          | Modifiers
--------------+-----------------------+-----------
 country_id   | character varying(2)  |
 country_name | character varying(40) |
 region_id    | numeric(10,0)         |


- Write a SQL statement to insert one row into the table countries against the column country_id and country_name.

Here in the following is the structure of the table countries.

    Column    |         Type          | Modifiers
--------------+-----------------------+-----------
 country_id   | character varying(2)  |
 country_name | character varying(40) |
 region_id    | numeric(10,0)         |



- Write a SQL statement to create duplicates of countries table named country_new with all structure and data.

Here in the following is the structure of the table countries.

    Column    |         Type          | Modifiers
--------------+-----------------------+-----------
 country_id   | character varying(2)  |
 country_name | character varying(40) |
 region_id    | numeric(10,0)         |


- Write a SQL statement to insert NULL values into region_id column for a row of countries table.

- Write a SQL statement to insert 3 rows by a single insert statement.

- Write a SQL statement insert rows from the country_new table to countries table.

Here are the rows for country_new table. Assume that, the countries table is empty.

 country_id | country_name | region_id
------------+--------------+-----------
 C1         | India        |      1002
 C2         | USA          |
 C3         | UK           |
 C4         | India        |      1001
 C5         | USA          |      1007
 C6         | UK           |      1003
(6 rows)


- Write a SQL statement to insert one row in the jobs table to ensure that no duplicate values will be entered into the job_id column.

Click me to see the solution

- Write a SQL statement to insert a record into the table countries to ensure that, at country_id and the region_id combination will be entered once in the table.


- Write a SQL statement to insert rows into the table countries in which the value of country_id column will be unique and auto incremented.


- Write a SQL statement to insert records into the table countries to ensure that the country_id column will not contain any duplicate data and this will be automatically incremented and the column country_name will be filled up by 'N/A' if no value assigned to that column.


- Write a SQL statement to insert rows into the job_history table in which one column job_id is containing those values which exist in job_id column of jobs table.


- Write a SQL statement to insert rows into the table employees in which a set of columns department_id and manager_id contains a unique value and that combined value must have existed into the table departments.


- Write a SQL statement to insert rows into the table employees in which a set of columns department_id and job_id contains the values which must have existed into the table departments and jobs.

## UPdate Records

- Write a SQL statement to change the email and commission_pct column of the employees table with 'not available' and 0.10 for those employees whose department_id is 110.

-  Write a SQL statement to change the email column of employees table with 'not available' for those employees whose department_id is 80 and gets a commission is less than.20%.

- Write a SQL statement to change the email column of the employees table with 'not available' for those employees who belongs to the 'Accounting' department.

- Write a SQL statement to change the salary of an employee to 8000 whose ID is 105, if the existing salary is less than 5000.

- Write a SQL statement to change the job ID of the employee which ID is 118 to SH_CLERK if the employee belongs to a department which ID is 30 and the existing job ID does not start with SH.

- Write a SQL statement to increase the salary of employees under the department 40, 90 and 110 according to the company rules that, the salary will be increased by 25% of the department 40, 15% for department 90 and 10% of the department 110 and the rest of the department will remain same.







