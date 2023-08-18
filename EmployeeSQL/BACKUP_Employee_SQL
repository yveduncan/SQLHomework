-- Create department table
CREATE TABLE department (
  department_no VARCHAR(10),
  dept_name VARCHAR NOT NULL
);

-- Create dept_emp table
CREATE TABLE dept_emp (
  emp_no INT,
  dept_no VARCHAR(30)
);

-- Create dept_manager table
CREATE TABLE dept_manager (
  dept_no VARCHAR(30),
  emp_no INT
);

-- Create employees table
CREATE TABLE employees (
  emp_no INT,
  emp_title VARCHAR(30) NOT NULL,
  birth_date DATE NOT NULL,
  first_name VARCHAR(30) NOT NULL,
  last_name VARCHAR(30) NOT NULL,
  sex VARCHAR(10) NOT NULL,
  hire_date DATE NOT NULL
);

-- Create salaries table
CREATE TABLE salaries (
  emp_no INT,
  salary INT
);

-- Create titles table
CREATE TABLE titles (
  title_id VARCHAR(10) NOT NULL,
  title VARCHAR(30) NOT NULL
);

-- List the employee number, last name, first name, sex, and salary of each employee.
SELECT employees.emp_no, employees.last_name, employees.first_name, employees.sex, salaries.salary
FROM employees
JOIN salaries ON employees.emp_no = salaries.emp_no;

-- List the first name, last name, and hire date for the employees who were hired in 1986.
SELECT first_name, last_name, hire_date
FROM employees
WHERE hire_date BETWEEN '1986-01-01' AND '1986-12-31';

-- List the manager of each department along with their department number, department name, employee number, last name, and first name.
SELECT department.department_no, department.dept_name, dept_manager.emp_no, employees.last_name, employees.first_name
FROM department
JOIN dept_manager ON department.department_no = dept_manager.dept_no
JOIN employees ON dept_manager.emp_no = employees.emp_no; 

-- List the department number for each employee along with that employee’s employee number, last name, first name, and department name.
SELECT employees.emp_no, employees.last_name, employees.first_name, department.dept_name
FROM employees
JOIN dept_emp ON employees.emp_no = dept_emp.emp_no
JOIN department ON dept_emp.dept_no = department.department_no;