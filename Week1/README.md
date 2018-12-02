# Week One Assignments
Figure out the appropiate sql queries for the following operation on the hr dataset and add your answers. For your first week you will be writing queries to query the hr database. The data and the structre of the database are present in the Data floder of this repo. 

## Basic Select
- Write a query to display the names (first_name, last_name) using alias name “First Name", "Last Name".



- Write a query to get unique department ID from employee table.



- Write a query to get all employee details from the employee table order by first name, descending.



- Write a query to get the names (first_name, last_name), salary, PF of all the employees (PF is calculated as 15% of salary).



- Write a query to get the employee ID, names (first_name, last_name), salary in ascending order of salary.




- Write a query to get the total salaries payable to employees.





- Write a query to get the maximum and minimum salary from employees table.





- Write a query to get the average salary and number of employees in the employees table.





- Write a query to get the number of employees working with the company.





- Write a query to get the number of jobs available in the employees table.





- Write a query get all first name from employees table in upper case.




- Write a query to get the first 3 characters of first name from employees table.




- Write a query to get the names (for example Ellen Abel, Sundar Ande etc.) of all the employees from employees table.




- Write a query to get first name from employees table after removing white spaces from both side.




- Write a query to get the length of the employee names (first_name, last_name) from employees table.




- Write a query to check if the first_name fields of the employees table contains numbers.




- Write a query to select first 10 records from a table.




- Write a query to get monthly salary (round 2 decimal places) of each and every employee.
Note : Assume the salary field provides the 'annual salary' information.





## Restriction and Sorting

- Write a query to display the name (first_name, last_name) and salary for all employees whose salary is not in the range $10,000 through $15,000.




- Write a query to display the name (first_name, last_name) and department ID of all employees in departments 30 or 100 in ascending order.





- Write a query to display the name (first_name, last_name) and salary for all employees whose salary is not in the range $10,000 through $15,000 and are in department 30 or 100.





- Write a query to display the name (first_name, last_name) and hire date for all employees who were hired in 1987.





- Write a query to display the first_name of all employees who have both "b" and "c" in their first name.




- Write a query to display the last name, job, and salary for all employees whose job is that of a Programmer or a Shipping Clerk, and whose salary is not equal to $4,500, $10,000, or $15,000.






- Write a query to display the last name of employees whose names have exactly 6 characters.





- Write a query to display the last name of employees having 'e' as the third character.






- Write a query to display the jobs/designations available in the employees table.






- Write a query to display the name (first_name, last_name), salary and PF (15% of salary) of all employees.





- Write a query to select all record from employees where last name in 'BLAKE', 'SCOTT', 'KING' and 'FORD'.





## Aggregate and Group By

- Write a query to list the number of jobs available in the employees table.






- Write a query to get the total salaries payable to employees.






- Write a query to get the minimum salary from employees table.






- Write a query to get the maximum salary of an employee working as a Programmer.






- Write a query to get the average salary and number of employees working the department 90.






- Write a query to get the highest, lowest, sum, and average salary of all employees.






- Write a query to get the number of employees with the same job.






- Write a query to get the difference between the highest and lowest salaries.







- Write a query to find the manager ID and the salary of the lowest-paid employee for that manager.






- Write a query to get the department ID and the total salary payable in each department.






- Write a query to get the average salary for each job ID excluding programmer.






- Write a query to get the total salary, maximum, minimum, average salary of employees (job ID wise), for department ID 90 only.






- Write a query to get the job ID and maximum salary of the employees where maximum salary is greater than or equal to $4000.




- Write a query to get the average salary for all departments employing more than 10 employees.







## Subqueries

- Write a query to find the name (first_name, last_name) and the salary of the employees who have a higher salary than the employee whose last_name='Bull'.





- Write a query to find the name (first_name, last_name) of all employees who works in the IT department.





- Write a query to find the name (first_name, last_name) of the employees who have a manager and worked in a USA based department.
Hint : Write single-row and multiple-row subqueries




- Write a query to find the name (first_name, last_name) of the employees who are managers.






- Write a query to find the name (first_name, last_name), and salary of the employees whose salary is greater than the average salary.






- Write a query to find the name (first_name, last_name), and salary of the employees whose salary is equal to the minimum salary for their job grade.






- Write a query to find the name (first_name, last_name), and salary of the employees who earns more than the average salary and works in any of the IT departments.






- Write a query to find the name (first_name, last_name), and salary of the employees who earns more than the earning of Mr. Bell.





- Write a query to find the name (first_name, last_name), and salary of the employees who earn the same salary as the minimum salary for all departments.





- Write a query to find the name (first_name, last_name), and salary of the employees whose salary is greater than the average salary of all departments.





- Write a query to find the name (first_name, last_name) and salary of the employees who earn a salary that is higher than the salary of all the Shipping Clerk (JOB_ID = 'SH_CLERK'). Sort the results of the salary of the lowest to highest.





- Write a query to find the name (first_name, last_name) of the employees who are not supervisors.





- Write a query to display the employee ID, first name, last name, and department names of all employees.






- Write a query to display the employee ID, first name, last name, salary of all employees whose salary is above average for their departments.






- Write a query to fetch even numbered records from employees table.





- Write a query to find the 5th maximum salary in the employees table.





- Write a query to find the 4th minimum salary in the employees table. 





- Write a query to select last 10 records from a table.





- Write a query to list the department ID and name of all the departments where no employee is working.





- Write a query to get 3 maximum salaries.





- Write a query to get 3 minimum salaries.





- Write a query to get nth max salaries of employees.


## JOINS

- Write a query to find the addresses (location_id, street_address, city, state_province, country_name) of all the departments.
Hint : Use NATURAL JOIN.




- Write a query to find the name (first_name, last name), department ID and name of all the employees. 




- Write a query to find the name (first_name, last_name), job, department ID and name of the employees who works in London.




- Write a query to find the employee id, name (last_name) along with their manager_id and name (last_name).





- Write a query to find the name (first_name, last_name) and hire date of the employees who was hired after 'Jones'.




- Write a query to get the department name and number of employees in the department.




- Write a query to find the employee ID, job title, number of days between ending date and starting date for all jobs in department 90.




- Write a query to display the department ID and name and first name of manager.




- Write a query to display the department name, manager name, and city.




- Write a query to display the job title and average salary of employees.




- Write a query to display job title, employee name, and the difference between salary of the employee and minimum salary for the job.





- Write a query to display the job history that were done by any employee who is currently drawing more than 10000 of salary.




- Write a query to display department name, name (first_name, last_name), hire date, salary of the manager for all managers whose experience is more than 15 years.





