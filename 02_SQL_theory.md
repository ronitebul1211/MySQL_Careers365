# Data Definition Language

set of statements allow the user to define / modify data structures & objects

-  **CREATE**
   -  creating entire databases, tables
   -  CREATE TABLE sales purchase_number INT ;
-  **ALTER**
   -  altering existing objects **ADD**, **REMOVE**, **RENAME**
   -  ALTER TABLE sales  
      ADD COLUMN date_of_purchase DATE ;
-  **DROP**
   -  deleting DB object
   -  DROP TABLE customers
-  **RENAME**
   -  allows you to rename object
   -  RENAME TABLE customers TO customers_data
-  **TRUNCATE**
   -  remove data
   -  TRUNCATE TABLE customers_data
