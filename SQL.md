---
> Name: Syed Modassir Ali
> Date: 26.04.2020
> Title: Sql 
---

# On Kali Linux (Access the MariaDb)

```
service mysql start
mysql -u root -p
show databases;
create database database_name;
use database_name;
create table table_name(fieldname datatype(size));
show tables;
show columns form table_name;
```
Example
```
create database notebook;
use notebook;
create table employee(empid int primary key, firstname char(20),lastname char(20), email varchar(20-))
show tables;
show columns form employee; 
select * from employee
```
