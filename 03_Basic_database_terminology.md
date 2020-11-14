# Relational Database Essentials

**Main Goal** :
organize huge amount of data tat can be quickly retrieve  
**HOW** : relational algebra  
relational data kept in separate tables, relation create by shared id between records

# DB Terminology

**PROCESS**

1. design db entities & relation
   -  Entity-Relationship Diagram
   -  Relational Schema
2. SQL use to set up DB physically
3. DB manipulation

**DB Management = 1 + 2 + 3**  
**DB Administration = maintenance**

# Relational Schema

## Primary Key

a column (or a set of columns), whose value exist & unique for every record in the table (bold, underline - in RS)

-  each table has 1 primary key
-  can't contain null
-  not all tables have a primary key

## Foreign Key

show us where the relations are (FK - in RS)  
identifies the relationships between tables

-  customers_id, primary key in customers table
-  customers_id, foreign key in sale table
-  foreign key **can** be null
-  MySql throw error when f.key contain value not exist as p.key in other table.

## Unique key & Null values

**Unique key** used to specify to not allow duplicate data in specific column, can contain null value.

# Relationships

tell how much data from foreign key field can be seen in the primary key column of the table the data is related to in vice versa.

-  one-to-many :  
   one value "customer_id" (customers table), can by found many times in customer_id column in sales table
-  many-to-one :  
   each sale record associated with on customer_id
