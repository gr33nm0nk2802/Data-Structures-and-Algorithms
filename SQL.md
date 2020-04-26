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

### Permissions

- Viewing 
```
SHOW GRANTS FOR 'testuser'@'localhost';
```

- Granting
```
GRANT permission ON database.table TO 'user'@'localhost';
FLUSH PRIVILEGES;
```
common permission are - 
    ALL – Allow complete access to a specific database. If a database is not specified, then allow complete access to the entirety of MySQL.
    CREATE – Allow a user to create databases and tables.
    DELETE – Allow a user to delete rows from a table.
    DROP – Allow a user to drop databases and tables.
    EXECUTE – Allow a user to execute stored routines.
    GRANT OPTION – Allow a user to grant or remove another user’s privileges.
    INSERT – Allow a user to insert rows from a table.
    SELECT – Allow a user to select data from a database.
    SHOW DATABASES- Allow a user to view a list of all databases.
    UPDATE – Allow a user to update rows in a table.

- Removing
```
REVOKE permission ON database.table FROM 'user'@'localhost';
FLUSH PRIVILEGES;
```

### Removing User

Removing testuser
```
DROP USER 'testuser'@'localhost';
```

### Connecting to the database

Inside connect.php

```
$mysql_host = 'localhost'; // 127.0.0.1
$mysql_user = 'root';
$mysql_pass = 'password';

mysqli_connect($mysql_host,$mysql_user,$mysql_pass); // returns boolean
```
To show custom warnings
```
@mysqli_connect($mysql_host,$mysql_user,$mysql_pass); or die('Cannot Connect');
```

Connect to the db
```
@mysqli_select_db(mysqli_connect($mysql_host,$mysql_user,$mysql_pass),'database_name'); 
```

Complete Connection Code
```
if(!@mysqli_connect($mysql_host,$mysql_user,$mysql_pass)){
    die("Connection Unsuccessful");
}
else{
    if(@mysqli_select_db(mysqli_connect($mysql_host,$mysql_user,$mysql_pass),'database_name')){
        echo("Connection Success");
    }
    else{
        echo("Cannot connect to the database");
    }
}
```

### Getting Data

```
require 'connect.php';
$query ="select * from table";
if($is_query_run = mysql_query($query)){

while($query_execute=mysql_fetch_assoc($is_query_run)){

    echo $query_execute['key'];
}
}
```
