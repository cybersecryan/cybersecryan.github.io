## Apply filters to SQL Queries

### Project Description
SQL filtering allows us as analysts to filter through giant data tables. From identifying usernames to narrowing down certain event ID's, there is a filter for that.

### 1. Retrieve after hours *failed* login attempts
#### Scenario: 
You recently discovered a potential security incident that occurred after business hours. To investigate this, you need to query the log_in_attempts table and review after hours login activity. Use filters in SQL to create a query that identifies all failed login attempts that occurred after 18:00. (The time of the login attempt is found in the login_time column. The success column contains a value of 0 when a login attempt failed; you can use either a value of 0 or FALSE in your query to identify failed login attempts.)

#### SQL query:
SELECT * FROM log_in_attempts WHERE login_time >= '18:00:00' AND success = 0;

### 2. Retrieve login attempts on specific dates
#### Scenario: 
A suspicious event occurred on 2022-05-09. To investigate this event, you want to review all login attempts which occurred on this day and the day before. Use filters in SQL to create a query that identifies all login attempts that occurred on 2022-05-09 or 2022-05-08. (The date of the login attempt is found in the login_date column.)

#### SQL query:
SELECT * FROM log_in_attempts WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';

### 3. Retrieve login attempts outside of Mexico
#### Scenario:
There’s been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. Now, you need to investigate login attempts that occurred outside of Mexico. Use filters in SQL to create a query that identifies all login attempts that occurred outside of Mexico. (When referring to Mexico, the country column contains values of both MEX and MEXICO, and you need to use the LIKE keyword with % to make sure your query reflects this.)

#### SQL query:
SELECT * FROM log_in_attempts WHERE NOT country LIKE 'Mex%';

### 4. Retrieve employees in Marketing
#### Scenario:
Your team wants to perform security updates on specific employee machines in the Marketing department. You’re responsible for getting information on these employee machines and will need to query the employees table. Use filters in SQL to create a query that identifies all employees in the Marketing department for all offices in the East building.

(The department of the employee is found in the department column, which contains values that include Marketing. The office is found in the office column. Some examples of values in this column are East-170, East-320, and North-434. You’ll need to use the LIKE keyword with % to filter for the East building.)

#### SQL query:
SELECT * FROM employees WHERE department = 'Marketing' AND office LIKE 'East%';

### 5. Retrieve employees in Finance or Sales
#### Scenario:
Your team now needs to perform a different security update on machines for employees in the Sales and Finance departments. Use filters in SQL to create a query that identifies all employees in the Sales or Finance departments. (The department of the employee is found in the department column, which contains values that include Sales and Finance.)

#### SQL query:
SELECT * FROM employees WHERE department = 'Sales' OR department = 'Finance';

### 6. Retrieve all employees NOT in IT
#### Scenario:
Your team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it. Use filters in SQL to create a query which identifies all employees not in the IT department. (The department of the employee is found in the department column, which contains values that include Information Technology.)

#### SQL query:
SELECT * employees WHERE NOT department = 'Information Technology';







