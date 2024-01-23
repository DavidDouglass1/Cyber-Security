# Apply filters to SQL queries


## Project description

Demonstration of my ability to apply filters to SQL queries when searching large databases for information.  SQL queries are a great tool to quickly find information (assuming the database is also kept up to date).


## Retrieve after hours failed login attempts

Due to a potential security incident on 2022-05-09, an investigation was started to assess the situation.  First the failed login attempts that occurred after hours were checked using the SQL query on the login database: 


```
SELECT * FROM log_in_attempts WHERE login_time > '19:00' AND success = 0;
```


The “>” operator after login time will filter only the login attempts that occurred after (non-inclusive) 19:00.  The AND operator will filter out all login attempts that do not match the statement afterwards, i,.e. successful login attempts will not be listed.


## Retrieve login attempts on specific dates

Further logs to investigate were all the login attempts on the day of and day before the incident using the query: 


```
Select * FROM log_in_attempts WHERE login_date = '2022-05-09' AND success = 0 OR login_date = '2022-05-08' AND success = 0;
```



## Retrieve login attempts outside of Mexico

It was determined that the origin of the security was not in Mexico.  Thus the investigation looked at all login attempts outside of Mexico using the query: 


```
Select * FROM log_in_attempts WHERE NOT LIKE 'Mex%';
```


The LIKE operator ensures that both “Mex” and “Mexico” are included.


## Retrieve employees in Marketing

Security updates need to be made on the machines for the marketing employees in the East building.  The list of employees matching this criteria was acquired using the query: 


```
Select * FROM employees WHERE department = 'Marketing' AND office LIKE 'East%';
```


The LIKE operator ensures that every office in the East building are listed.


## Retrieve employees in Finance or Sales

More security updates need to be made for machines in the Finance and Sales departments.  The list of employees matching the criteria was acquired using the following query: 


```
Select * FROM employees WHERE department = 'Finance' OR department = 'Sales';
```


The OR operator will ensure that filter will include outputs that qualify in either argument before and after the OR operator.


## Retrieve all employees not in IT

The IT department already has security updates but all other departments do not.  The following query will list all employees whose machines need updates:


```
Select * FROM employees WHERE department NOT 'Information Technology';
```



## Summary

SQL queries let me quickly find relevant information to match specific scenarios.  It is an essential tool for IT departments to maintain security and to retrieve information.
