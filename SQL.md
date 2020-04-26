----
> Name: Syed Modassir Ali
> Date: 26.04.2020
> Title: Sql 
----

# On Kali Linux (Access the MariaDb)

### Starting SQL and creating table to insert data into the columns
```
service mysql start
mysql -u root -p
show databases;
create database database_name;
use database_name;
create table table_name(fieldname datatype(size));
show tables;
describe table_name;
or
show columns from table_name;
```
Example
```
create database notebook;
use notebook;
create table employee(empid int primary key, firstname char(20),lastname char(20), email varchar(20-))
show tables;
show columns from employee; 
select * from employee
```

### Creating a user
```
CREATE USER 'user'@'localhost' IDENTIFIED BY 'user_password';
```

### To view the users
```
SELECT User,Host FROM mysql.user;
```

### Password change
```
UPDATE user SET Password=PASSWORD('new password') Where User='root'; FLUSH PRIVILEDGES;
```

### Delete a database
```
DROP DATABASE database_name;
```

### Inserting data
```
insert into table_name value("Value1","Value 2",..);
```

### To display the data inside the table
```
describe table_name;
select * from table_name;
```

### To export the data in a table as .csv
```
mysql -u root -p -e 'select * from databasename.table_name' | sed 's/\t/,/g' > filename.csv
```
### Backing up databases

- Single Database
```
mysqldump database_name > database_name.sql
```

- Multiple Databases
```
mysqldump --databases database_one database_two > two_databases.sql
```

- All Databases
```
mysqldump --all-databases > all_databases.sql
```

- Restoring Single
```
mysql database_name < database_name.sql
```

- Restore single from all backup 
```
mysql --one-database database_name < all_databases.sql
```



