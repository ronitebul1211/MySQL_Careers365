# Data Definition Language (DDL)

set of statements allow data structures definition / modification

-  **CREATE**
   -  creating entire databases, tables
   -  CREATE TABLE sales purchase_number INT;
-  **ALTER**
   -  altering existing objects **ADD**, **REMOVE**, **RENAME**
   -  ALTER TABLE sales  
      ADD COLUMN date_of_purchase DATE;
-  **DROP**
   -  deleting DB object
   -  DROP TABLE customers;
-  **RENAME**
   -  allows you to rename object
   -  RENAME TABLE customers TO customers_data;
-  **TRUNCATE**
   -  remove data from table
   -  TRUNCATE TABLE customers_data;

# Data Manipulation Language (DML)

set of statements allow data manipulation

-  **SELECT ... FROM ...**
   -  retrieve specific data
   -  SELECT \* FROM sales;
-  **INSERT INTO... VALUES...**
   -  insert data into tables
   -  INSERT INTO sales VALUES (1, "2017-10-11");
   -  INSERT INTO sales (INSERT INTO sales (purchase_number, date_of_purchase)  
      VALUES (1, "2017-10-11");
-  **UPDATE ... SET ... WHERE...**
   -  update existing data
   -  UPDATE sales  
      SET date_of_purchase_number = "2017-12-12"  
      WHERE purchase_number = 1;
-  **DELETE ... FROM ...**
   -  specify precisely what data potion should be removed
   -  DELETE FROM sales  
      WHERE purchase_number = 1;

# Data Control Language (DCL)

allow us to manage the rights users have in a database

-  CREATE USER "username’@’localhost" IDENTIFIED BY "pass";

-  **GRANT...TO...**
   -  give permissions to a user
   -  GRANT type_of_permission ON database_name.table_name  
      TO "username’@’localhost"
   -  GRANT SELECT ON sales.customers  
      TO "username’@’localhost"
   -  GRANT ALL ON sales.\*  
      TO "username’@’localhost"
-  **REVOKE**
   -  revoke permissions from user
   -  REVOKE type_of_permission ON database_name.table_name  
      FROM "username’@’localhost"

# Transaction Control Language (TCL)

not every change you make to a database is saved automatically

-  **COMMIT**
   -  related to INSERT, UPDATE, DELETE
   -  will save the changes you’ve made and let other users have access to the modified version of the
      database
   -  add COMMIT to the end of the command
-  **ROLLBACK**
   -  allows you to undo any changes you have made but don’t want to be
      saved permanently (not committed)  
      reverts to the last non committed state.
-  use command separately
